# 🚀 ⚽ SofaScore Scraper PRO 🔥

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the ⚽ SofaScore Scraper PRO 🔥. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/sofascore-scraper-pro?fpr=cbgdsf)

---

## ⚽ SofaScore Scraper PRO 🔥


> **The ultimate tool to extract lightning-fast data from ANY SofaScore page!** 🚀

**SofaScore Scraper PRO** is built for speed, reliability, and ease of use. Whether you need match stats, player profiles, or live scores, teams details, we've got you covered.

---

### ✨ Key Features

- **⚡ Blazing Fast Performance**  
  Optimized for speed using advanced scraping techniques. faster than you can say "Goal!"
  
- **🌍 Multi-Language Ready**  
  Seamlessly handles data in any language supported by SofaScore 

- **🌐 Universal Support**  
  Scrape **ANYTHING** on SofaScore (accross different sports):
  - 🏆 **Leagues & Tournaments**
  - ⚽ **Teams & Clubs**
  - 🏃 **Player Profiles**
  - 🔴 **Live Scores & Fixtures**

---

### 🛠️ How to Use

It's as simple as 1-2-3. Just provide the URLs you want to scrape!

#### Input Configuration

| Field | Type | Description |
| :--- | :--- | :--- |
| `startUrls` | `Array` | List of SofaScore URLs (Strings) |

#### Example Input

```json
{
    "startUrls": [
        "https://www.sofascore.com/football/match/atletico-madrid-real-madrid/EgbsLgb",
        "https://www.sofascore.com/tennis/player/djokovic-novak/14882",
        "https://www.sofascore.com/football/team/barcelona/2817"
    ]
}
````

***

### �🔎 SEO Keywords

`SofaScore Scraper`, `Football Data Extraction`, `Sports Stats Crawler`, `Live Score API`, `Betting Odds Data`, `Match Statistics`, `Player Performance Data`, `Sports Analytics`, `Tennis Data Scraper`.

***

### 📬 Contact & Support

**Need a custom solution? Have a feature request?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

***

<center><i>Made with ❤️ for the data community.</i></center>

# Actor input Schema

## `startUrls` (type: `array`):

List of SofaScore URLs to scrape

## Actor input object example

```json
{
  "startUrls": [
    "https://www.sofascore.com/football/match/atletico-madrid-real-madrid/EgbsLgb",
    "https://www.sofascore.com/tennis/player/djokovic-novak/14882"
  ]
}
```

# Actor output Schema

## `results` (type: `string`):

No description

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
const input = {
    "startUrls": [
        "https://www.sofascore.com/football/match/atletico-madrid-real-madrid/EgbsLgb",
        "https://www.sofascore.com/tennis/player/djokovic-novak/14882"
    ]
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/sofascore-scraper-pro").call(input);

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
run_input = { "startUrls": [
        "https://www.sofascore.com/football/match/atletico-madrid-real-madrid/EgbsLgb",
        "https://www.sofascore.com/tennis/player/djokovic-novak/14882",
    ] }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/sofascore-scraper-pro").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrls": [
    "https://www.sofascore.com/football/match/atletico-madrid-real-madrid/EgbsLgb",
    "https://www.sofascore.com/tennis/player/djokovic-novak/14882"
  ]
}' |
apify call azzouzana/sofascore-scraper-pro --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/sofascore-scraper-pro",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
