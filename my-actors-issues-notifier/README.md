# 🚀 🔔 My Actors Issues Notifier

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the 🔔 My Actors Issues Notifier. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/my-actors-issues-notifier?fpr=cbgdsf)

---

## 🔔 My Actors Issues Notifier

An **Open Source** actor that pulls your Apify Console for **new open**/**reopened** actor issues on your account and writes webhook-ready rows to the **default dataset** - connect [Telegram, Slack, and more](https://docs.apify.com/platform/integrations/webhooks) from Integrations. 

### How it works

1. `POST /public/authentication/resume` — uses console `ApifyRT` cookie → short-lived `uiToken`
2. Socket.IO subscribe to `userOwnedPublicActorsIssuesPub` (paginated)
3. Keeps issues with `status === "OPEN"`
4. Named KV store `apify-console-open-issues`:
   - `firstRunComplete` — `false` until the first successful poll finishes (To not detect already open issues while running this for the first time)
   - `seenIssueIds` — currently open issue IDs (closed IDs are removed each run)
5. **First run** (`firstRunComplete` unset): save open ids + set flag — **no** dataset push
6. **Later runs**: for each new open id, `GET /actor-issues/{issueId}/comments` (last array entry) → dataset row (`type: "new_open_issue"`), then refresh `seenIssueIds`
7. On resume/socket errors: one dataset row (`type: "fetch_failure"`)

### Dataset records

**New issue** (`type: "new_open_issue"`):

| Field | Type | Description |
|--------|------|-------------|
| `type` | `string` | Always `"new_open_issue"` |
| `notifiedAt` | `string` | ISO timestamp when the record was pushed |
| `issueId` | `string` | Issue `_id` from Console |
| `title` | `string` | Issue title |
| `status` | `string` | Issue status (e.g. `"OPEN"`) |
| `objectType` | `string` | e.g. `"PAID_ACTOR"` |
| `objectId` | `string` | Linked object id (often same as actor `_id`) |
| `createdAt` | `string` | Issue creation time (ISO) |
| `url` | `string` | Direct link to the issue in Console |
| `actorTitle` | `string` | Actor display title (fallback: actor name or `objectId`) |
| `reporter` | `string` | Reporter display name or username |
| `lastComment` | `string \| null` | Text of the last entry in `/actor-issues/{issueId}/comments` (HTML stripped) |

Example dataset output:

```json
[
  {
    "type": "new_open_issue",
    "notifiedAt": "2026-06-02T10:33:00.204Z",
    "issueId": "12345678910",
    "title": "test an open issue",
    "status": "OPEN",
    "objectType": "PAID_ACTOR",
    "objectId": "987654321",
    "createdAt": "2026-06-02T10:26:17.375Z",
    "url": "https://console.apify.com/actors/VzKtdb1t0Qnc07X8V/issues/12345678910",
    "actorTitle": "SofaScore scraper PRO⚡",
    "reporter": "dumy_username",
    "lastComment": "This is an open issue with dummy run"
  }
]
````

**Failure** (`type: "fetch_failure"`):

| Field | Description |
|--------|-------------|
| `step` | e.g. `authentication/resume`, `socket.io subscribe` |
| `errorMessage` | Error detail |
| `notifiedAt` | ISO timestamp |

Each new or failed notification is a row in this actor’s **default dataset**. Use that for integrations—no extra code required in this repo.

### Configuration

#### Actor input

| Input | Required | Notes |
|--------|----------|--------|
| `apifyRt` | Yes | `ApifyRT` cookie from console.apify.com |

Copy ApifyRT from DevTools → **Application** → **Cookies** → `https://console.apify.com`.

Create a **scheduled task** and set `apifyRt` in the task input so the actor runs on a interval (e.g. every 10–15 minutes).

#### Webhooks (Telegram, Slack, etc.)

Open the actor’s **Integrations** tab in Apify Console: <https://console.apify.com/actors/u45C6wzQQgsbqaeie/integrations>

There, you can connect your preferred communication app (Slack, Telegram, WhatsApp, etc.) or ticketing system (Jira, Trello, Linear, etc.) using either Apify's native integrations or custom webhooks.

- Trigger on **actor run succeeded**
- Point the integration at this actor’s **default dataset** and map fields such as `title`, `actorTitle`, `reporter`, and `url` etc in your custom message template.

### 📬 Contact & Support

**Have feedback, a question, or just want to say hi?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

***

<center><i>Made with ❤️ for the data community.</i></center>

# Actor input Schema

## `apifyRt` (type: `string`):

Console session cookie (DevTools → Application → Cookie → console.apify.com).

## Actor input object example

```json
{}
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
const run = await client.actor("azzouzana/my-actors-issues-notifier").call(input);

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
run = client.actor("azzouzana/my-actors-issues-notifier").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{}' |
apify call azzouzana/my-actors-issues-notifier --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/my-actors-issues-notifier",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
