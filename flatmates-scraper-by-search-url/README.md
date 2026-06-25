# 🚀 🏠 Flatmates.com.au Scraper

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the 🏠 Flatmates.com.au Scraper. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/flatmates-scraper-by-search-url?fpr=cbgdsf)

---

## 🏠 Flatmates.com.au Scraper

**Unlock the potential of Australia's #1 share accommodation site!** 🚀

This powerful actor scrapes data from [Flatmates.com.au](https://flatmates.com.au/), extracting detailed information about **rooms** 🛏️, **people** 👤, and **teamups** 🤝.

---

### ⚙️ Input Configuration

The actor accepts the following input options:

- `startUrl` 🔗: The URL to start scraping from (e.g., search results page). This should be either a people, rooms, or teamups search results page URL.
Example of these are
    - `https://flatmates.com.au/rooms/campsie-2194?search_source=search_function`
    - `https://flatmates.com.au/people/sydney/max-8-weeks?search_source=search_function`
    - `https://flatmates.com.au/teamups/campsie-2194?search_source=search_function`
- `maxItems` 📄: Maximum number of items to scrape (default 1000).

### 📤 Output

The result is stored in the default dataset containing detailed listing data, ready for your analysis! 📊

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

#### 🗝️ SEO Keywords
Flatmates Scraper, Real Estate Australia, Room Share Data, Flatshare Listings, Australia Accommodation Scraper, Apify Flatmates Actor, Housing Data Australia, Roommate Finder Australia.

#### 📬 Contact & Custom Solutions
**Need something specific?** Want to chat? Don't hesitate to reach out to us! 💬

- **Discord**: `@azzouzana` 🎮
- **Email**: `labs@azzouzana.com` 📧

# Actor input Schema

## `startUrl` (type: `string`):

Search results page URL
## `maxItems` (type: `integer`):

Maximum number of listings to scrape

## Actor input object example

```json
{
  "startUrl": "https://flatmates.com.au/rooms/campsie-2194/1-week?search_source=search_function",
  "maxItems": 1000
}
````

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
    "startUrl": "https://flatmates.com.au/rooms/campsie-2194/1-week?search_source=search_function",
    "maxItems": 1000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/flatmates-scraper-by-search-url").call(input);

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
run_input = {
    "startUrl": "https://flatmates.com.au/rooms/campsie-2194/1-week?search_source=search_function",
    "maxItems": 1000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/flatmates-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://flatmates.com.au/rooms/campsie-2194/1-week?search_source=search_function",
  "maxItems": 1000
}' |
apify call azzouzana/flatmates-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/flatmates-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
