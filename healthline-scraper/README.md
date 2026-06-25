# 🚀 🔍Healthline.com Scraper 🔍

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the 🔍Healthline.com Scraper 🔍. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/healthline-scraper?fpr=cbgdsf)

---

## 🔍Healthline.com Scraper 🔍

This Apify actor scrapes search results from [Healthline.com](https://www.healthline.com/). It extracts data such as article titles, URLs, content, authors, reviewers, descriptions, and many other properties. 🚀

### Available Features ✅
The actor scrapes search results from Healthline.com. It extracts the following data:
  - Article titles
  - Article URL
  - Content
  - Article's authors, editors & reviewers details
  - Article's dates (created at, updated at, reviewed at, etc.)
  - Article's descriptions
  - Article's lengths
  - Article's images
  - Headers
  - Keywords
& many others attributes

It also supports limiting the total number of search results

### Input

The actor takes either a searchQuery or searchUrl parameters. Note that you can either use searchQuery or searchUrl but not both in the same run

- `searchQuery` (string, optional): The search terms or keywords that you want to use to perform a search on Healthline.com
- `searchUrl` (string, required): The specific URL to start the search from on Healthline.com. This can be useful if you have a predefined search URL 
- `maxResultsCount` (number, optional): The maximum number of search results that the actor should scrape. The default value is 5.

#### Example Input

```json
{
  "searchQuery": "mental health",
  "searchUrl": "https://www.healthline.com/search?q1=women%20sleep",
  "maxResultsCount": 7
}
````

#### Example Output

![](https://i.ibb.co/wNVcBhDv/image.png)

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

# Actor input Schema

## `searchQuery` (type: `string`):

The query you want to search

## `searchUrl` (type: `string`):

The full search URL

## `maxResultsCount` (type: `integer`):

Number of search results to get

## Actor input object example

```json
{
  "searchUrl": "https://www.healthline.com/search?q1=children%20stress"
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
const input = {
    "searchUrl": "https://www.healthline.com/search?q1=children%20stress"
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/healthline-scraper").call(input);

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
run_input = { "searchUrl": "https://www.healthline.com/search?q1=children%20stress" }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/healthline-scraper").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "searchUrl": "https://www.healthline.com/search?q1=children%20stress"
}' |
apify call azzouzana/healthline-scraper --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/healthline-scraper",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
