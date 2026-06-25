# 🚀 Actor input object example

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Actor input object example. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/real-estate-au-scraper-pro?fpr=cbgdsf)

---

#### What's about
Scrape real estate.

#### 📞 Contact Me

**Need a custom solution? Have a feature request or just want to chat?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: [labs@azzouzana.com](mailto:labs@azzouzana.com)

# Actor input Schema

## `startUrl` (type: `string`):

Start URL
## `maxItems` (type: `integer`):

Maximum number of listings to scrape (Free users capped at 5).

## Actor input object example

```json
{
  "maxItems": 3000
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
    "maxItems": 3000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/real-estate-au-scraper-pro").call(input);

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
run_input = { "maxItems": 3000 }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/real-estate-au-scraper-pro").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "maxItems": 3000
}' |
apify call azzouzana/real-estate-au-scraper-pro --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/real-estate-au-scraper-pro",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
