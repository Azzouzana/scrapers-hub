# 🚀 ⚽ World Cup 2026 — Real-Time Events Notifications

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the ⚽ World Cup 2026 — Real-Time Events Notifications. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/world-cup-2026-real-time-events-notifications?fpr=cbgdsf)

---

## ⚽ World Cup 2026 — Real-Time Events Notifications

Hook up your app, bot, or automation to **live match pings** for World Cup 2026. This setup actor is the one-time “where should we send stuff?” step.

### What you get 🔔

Once you’re in, your webhook gets **instant POST notifications** when the action hits the pitch:

- ⚽ Goals (scorer + assist when available)
- 🟨🟥 Cards (Red/Yellow)
- 🔄 Substitutions
- ⏱️ Match phases — kickoff, HT, 2nd half, FT, stoppage time

No polling. No F5 spam. Events land on your URL as they happen.

**Discord?** Paste a channel webhook URL — the stream actor formats each update as a ready-to-post `content` message (goals, cards, subs, HT/FT).

### Live examples on Webhook.site

Real POSTs from the delivery service during live WC26 — open the inbox to inspect full JSONs:
https://webhook.site/#!/view/01b18b65-2625-4129-88f1-3ca2cdfe0615

Each notification is a separate POST.

### How it works (5 seconds setup)

1. **Create a free [Apify account](https://apify.com/sign-up?fpr=cbgdsf)**
2. **Run this actor** with your webhook URL
3. **Optional:** check **Send test payload** — dummy goal POST to confirm delivery
4. **We save it** next to your Apify account
5. **Our delivery service** fires live JSON during live matches

One setup run → notifications in the background all tournament long. Free. Easy.

### Input

The Apify form has two sections: **Webhook delivery** (URL + test ping) and **Notification events** (what to send).

| Field | Default | Description |
|-------|---------|-------------|
| `webhookUrl` | — | HTTPS endpoint — Discord, Webhook.site, or your API (required) |
| `testWebhook` | `true` | Send a dummy goal POST now to verify whether your endpoint is reachable |
| `subscribeGoals` | `true` | Goals (scorer + assist when available) |
| `subscribeYellowCards` | `false` | Yellow cards |
| `subscribeRedCards` | `false` | Red cards |
| `subscribePeriods` | `false` | Match phases — kickoff, HT, 2nd half, FT, stoppage time |
| `subscribeSubstitutions` | `false` | Substitutions |

```json
{
  "webhookUrl": "https://your-server.com/notifications/wc26",
  "testWebhook": true,
  "subscribeGoals": true,
  "subscribeYellowCards": false,
  "subscribeRedCards": true,
  "subscribePeriods": false,
  "subscribeSubstitutions": true
}
````

Node, Python, Zapier, Make, n8n — if it accepts POST, you’re good. **Discord** works too — paste a channel webhook URL and the stream actor formats messages for you.

#### Setup test ping

When **`testWebhook`** is checked (default **on**), the setup actor POSTs one dummy notification — A similar shape to a real goal, marked `test: true`:

```json
{
  "test": true,
  "message": "Ready to receive World Cup chaos!",
  "channel": "test",
  "match": "Test Home FC vs Test Away FC",
  "summary": {
    "kind": "test",
    "type": "goal",
    "text": "Ready to receive World Cup chaos! — Test Player 0' (assist Test Assist) (1-0)",
    "score": { "home": 1, "away": 0 }
  }
}
```

Discord receives `{ "content": "⚽ Ready to receive World Cup chaos! — …" }`. Setup still succeeds if the ping fails — check run output `testWebhook.ok`.

### Output (dataset)

Successful run = one confirmation row:

```json
{
  "subscriptionId": "uuid",
  "apifyUserId": "your-apify-user-id",
  "webhookUrl": "https://your-server.com/notifications/wc26",
  "eventTypes": {
    "goals": true,
    "yellowCards": false,
    "redCards": true,
    "periods": false,
    "substitutions": true
  },
  "updatedAt": "2026-06-11T12:00:00.000Z",
  "testWebhook": {
    "sent": true,
    "ok": true,
    "status": 200
  }
}
```

### Changing your URL

- One slot per Apify user
- Run again with a **new URL** → we swap it in
- No duplicate subscriptions cluttering things

### What a notification looks like 📬

During live World Cup matches, the delivery service **POSTs to your `webhookUrl`**.

- **Discord** (`discord.com/api/webhooks/...`) → `{ "content": "..." }` — formatted.
- **Everything else** → full JSON payload below

#### HTTP request

```http
POST /notifications/wc26 HTTP/1.1
Host: your-server.com
Content-Type: application/json

{ ... body below ... }
```

You only receive event types you enabled at setup (`subscribeGoals`, `subscribeYellowCards`, etc.). If you left only **Goals** checked, you will not get cards or subs.

Below: JSON shapes from live delivery. For raw POSTs with timestamps, see the [Webhook.site inbox](https://webhook.site/#!/view/01b18b65-2625-4129-88f1-3ca2cdfe0615).

#### Goal (with scorer + assist)

Live delivery — **Canada vs Bosnia & Herzegovina** (event `15186836`):

```json
{
  "ts": "2026-06-12T20:59:02.379Z",
  "eventId": 15186836,
  "subject": "event.15186836",
  "channel": "incidents",
  "incidentId": 351558696,
  "homeTeam": "Canada",
  "awayTeam": "Bosnia & Herzegovina",
  "match": "Canada vs Bosnia & Herzegovina",
  "summary": {
    "kind": "goal",
    "type": "goal",
    "class": "regular",
    "side": "away",
    "team": "Bosnia & Herzegovina",
    "minute": 21,
    "player": "J. Lukić",
    "assist": "S. Kolašinac",
    "text": "Goal — J. Lukić 21' (assist S. Kolašinac) (0-1)",
    "score": { "home": 0, "away": 1 }
  },
  "team": "Bosnia & Herzegovina",
  "player": "J. Lukić",
  "assist": "S. Kolašinac"
}
```

Earlier WC26 example — **Mexico vs South Africa** (event `15186710`):

```json
{
  "ts": "2026-06-11T19:14:50.813Z",
  "eventId": 15186710,
  "subject": "event.15186710",
  "channel": "score",
  "homeTeam": "Mexico",
  "awayTeam": "South Africa",
  "match": "Mexico vs South Africa",
  "summary": {
    "kind": "goal",
    "side": "home",
    "team": "Mexico",
    "score": "1-0",
    "player": "J. Quiñones",
    "assist": "E. Lira",
    "minute": 9,
    "text": "Goal — J. Quiñones 9' (assist E. Lira) (1-0)"
  },
  "patch": {
    "homeScore.current": 1,
    "awayScore.current": 0
  },
  "incidentId": 351455858,
  "player": "J. Quiñones",
  "assist": "E. Lira"
}
```

`summary.text` is ready to forward to Discord, Slack, or SMS as-is.

#### Red card

```json
{
  "ts": "2026-06-11T20:16:38.921Z",
  "eventId": 15186710,
  "subject": "event.15186710",
  "channel": "incidents",
  "incidentId": 125277734,
  "homeTeam": "Mexico",
  "awayTeam": "South Africa",
  "match": "Mexico vs South Africa",
  "summary": {
    "kind": "red",
    "type": "card",
    "class": "red",
    "side": "away",
    "team": "South Africa",
    "minute": 49,
    "player": "S. Sithole",
    "text": "red — S. Sithole 49'"
  },
  "team": "South Africa",
  "player": "S. Sithole"
}
```

#### Yellow card

Live delivery — **Canada vs Bosnia & Herzegovina**:

```json
{
  "ts": "2026-06-12T19:46:42.144Z",
  "eventId": 15186836,
  "subject": "event.15186836",
  "channel": "incidents",
  "incidentId": 125279344,
  "homeTeam": "Canada",
  "awayTeam": "Bosnia & Herzegovina",
  "match": "Canada vs Bosnia & Herzegovina",
  "summary": {
    "kind": "yellow",
    "type": "card",
    "class": "yellow",
    "side": "away",
    "team": "Bosnia & Herzegovina",
    "minute": 45,
    "player": "E. Demirović",
    "text": "yellow — E. Demirović 45'"
  },
  "team": "Bosnia & Herzegovina",
  "player": "E. Demirović"
}
```

#### Substitution

`playerIn` / `playerOut` appear **only** on substitutions. Live delivery — **Canada vs Bosnia & Herzegovina**:

```json
{
  "ts": "2026-06-12T20:22:12.251Z",
  "eventId": 15186836,
  "subject": "event.15186836",
  "channel": "incidents",
  "incidentId": 126397427,
  "homeTeam": "Canada",
  "awayTeam": "Bosnia & Herzegovina",
  "match": "Canada vs Bosnia & Herzegovina",
  "summary": {
    "kind": "substitution",
    "type": "substitution",
    "class": "regular",
    "side": "home",
    "team": "Canada",
    "minute": 61,
    "text": "Sub — L. Millar → J. Shaffelburg 61'",
    "playerIn": "J. Shaffelburg",
    "playerOut": "L. Millar"
  },
  "team": "Canada",
  "playerIn": "J. Shaffelburg",
  "playerOut": "L. Millar"
}
```

#### Match phases (kickoff → HT → 2H → FT)

Enable **`subscribePeriods`** for whistle-to-whistle milestones. One POST per phase change. Same top-level shape as goals and cards: `homeTeam`, `awayTeam`, `match`, and a readable `summary.text`.

| Moment | `summary.phase` | `summary.text` example |
|--------|-----------------|------------------------|
| First half | `first_half` | `First half — Mexico vs South Africa (0-0)` |
| Halftime | `halftime` | `Halftime — Mexico vs South Africa (1-0)` |
| Second half | `second_half` | `Second half — Mexico vs South Africa (1-0)` |

Full time — webhook JSON sample:

```json
{
  "ts": "2026-06-17T22:00:37.794Z",
  "eventId": 15186504,
  "subject": "event.15186504",
  "channel": "score",
  "summary": {
    "kind": "status",
    "type": "period",
    "phase": "full_time",
    "text": "Full time — England vs Croatia (4-2)",
    "score": {
      "home": 4,
      "away": 2
    },
    "status": {
      "code": 100,
      "description": "Ended"
    }
  },
  "homeTeam": "England",
  "awayTeam": "Croatia",
  "match": "England vs Croatia"
}
```

Halftime — webhook JSON sample:

```json
{
  "ts": "2026-06-11T19:55:00.676Z",
  "eventId": 15186710,
  "subject": "sport.football",
  "channel": "score",
  "homeTeam": "Mexico",
  "awayTeam": "South Africa",
  "match": "Mexico vs South Africa",
  "summary": {
    "kind": "status",
    "type": "period",
    "phase": "halftime",
    "text": "Halftime — Mexico vs South Africa (1-0)",
    "score": { "home": 1, "away": 0 },
    "status": { "code": 31, "description": "Halftime" }
  }
}
```

Stoppage time uses `summary.kind: "stoppage_time"` with `minutes` and `period` (1 or 2).

Other phases use the same shape: **`first_half`**, **`second_half`**, **`extra_time`**, **`penalties`**.

#### Field cheat sheet

| Field | Meaning |
|-------|---------|
| `ts` | When we sent the notification (ISO 8601) |
| `eventId` | Match id — stable for the whole game |
| `channel` | `score` (live socket) or `incidents` (API enrich for cards/subs) |
| `summary.kind` | `goal`, `yellow`, `red`, `substitution`, `status`, `stoppage_time`, … |
| `summary.type` | `goal`, `card`, `substitution`, or `period` for match phases |
| `summary.phase` | Period only: `first_half`, `halftime`, `second_half`, `full_time`, `stoppage_time`, … |
| `summary.text` | Human-readable one-liner |
| `summary.score` | `{ "home": 1, "away": 0 }` on goals and periods |
| `player` / `assist` | Scorer and assist on goals; player on cards |
| `playerIn` / `playerOut` | Substitution only |

### You’re live when…

Delivery kicks in once your URL is on the notification service. Changed URL or event toggles? Picked up within about **5 minutes** (no restart needed).

**Want to try it?** Plug in your webhook, open your logs, and wait for the beautiful chaos of live World Cup football. 🏆

***

### 📬 Contact & Support

**Need a custom solution? Have a feature request, a collaboration beyond the FIFA 2026 World Cup or just want to chat?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

***

# Actor input Schema

## `webhookUrl` (type: `string`):

HTTPS endpoint that receives WC26 live events JSON

## `testWebhook` (type: `boolean`):

POST a dummy goal notification to your webhook now to confirm it works.

## `subscribeGoals` (type: `boolean`):

Notify when a team scores (scorer & assister included when available).

## `subscribeYellowCards` (type: `boolean`):

Notify on yellow cards.

## `subscribeRedCards` (type: `boolean`):

Notify on red cards.

## `subscribePeriods` (type: `boolean`):

Notify on kickoff, halftime, second half, full time, and stoppage time.

## `subscribeSubstitutions` (type: `boolean`):

Notify when players are subbed on or off.

## Actor input object example

```json
{
  "webhookUrl": "YOUR_WEBHOOK_URL",
  "testWebhook": true,
  "subscribeGoals": true,
  "subscribeYellowCards": false,
  "subscribeRedCards": false,
  "subscribePeriods": false,
  "subscribeSubstitutions": false
}
```

# API

You can run this Actor programmatically using our API. Below are code examples in JavaScript, Python, and CLI, as well as MCP server setup.

## JavaScript example

```javascript
import { ApifyClient } from 'apify-client';

// Initialize the ApifyClient with your Apify API token
// Replace the '<YOUR_API_TOKEN>' with your token
const client = new ApifyClient({
    token: '<YOUR_API_TOKEN>',
});

// Prepare Actor input
const input = {};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/world-cup-2026-real-time-events-notifications").call(input);

// Fetch and print Actor results from the run's dataset (if any)
console.log('Results from dataset');
console.log(`💾 Check your data here: https://console.apify.com/storage/datasets/${run.defaultDatasetId}`);
const { items } = await client.dataset(run.defaultDatasetId).listItems();
items.forEach((item) => {
    console.dir(item);
});

// 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/js/docs

```

## Python example

```python
from apify_client import ApifyClient

# Initialize the ApifyClient with your Apify API token
# Replace '<YOUR_API_TOKEN>' with your token.
client = ApifyClient("<YOUR_API_TOKEN>")

# Prepare the Actor input
run_input = {}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/world-cup-2026-real-time-events-notifications").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{}' |
apify call azzouzana/world-cup-2026-real-time-events-notifications --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/world-cup-2026-real-time-events-notifications",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
