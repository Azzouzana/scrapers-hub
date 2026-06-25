# 🚀 Local.ch Business Directory Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Local.ch Business Directory Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/local-ch-search-results-scraper-ppr?fpr=cbgdsf)

---

## Local.ch Business Directory Scraper (By Search URL)

### 🤩 Features

🚀 Our **blazing-fast local.ch scraper** 🏠 lets you extract public information of business search results from `local.ch` and export them in various formats (JSON, CSV, HTML, etc.).  
🔥 Simply provide your search URLs (optionally with filters applied), and you're all set!  
👉 It allows you to extract detailed business information, including company name, category, phone number, email, address, website, opening hours, reviews and much more.

### 📚 How to use this actor

1. 👉 [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required!
2. 🎉 Just click the **"Get Started"** button and complete a quick signup.
3. 💰 A free account includes enough credits to test this actor.

The scraper has a required `startUrl` parameter which is a URL to a search page with filters applied.

- Examples of valid URLs:
  - `https://www.local.ch/en/q/zurich/general-internal-medicine`
  - `https://www.local.ch/de/s/Mechanische%20Werkstatt%2C%20Deutsch?sorting=alphanum&filter_facet=attr_conversion_modifications%3Aaccessory`
  - `https://www.local.ch/fr/s/Restaurant%20Basel?filter_facet=attr_services_offer%3Aaperitif`
  - `https://www.local.ch/it/s/dentista?filter_facet=attr_general_geo%3Aclose_to_publictransport`
  - `https://www.local.ch/en/s/restaurant?bookingFilters.dateTime=2025-09-04T11%3A00%3A00.000Z&bookingFilters.persons=2&bookingFilters.slotType=RESTO`

### 🤔 Why scrape local.ch?

local.ch is Switzerland's leading online business directory and local search platform. It provides detailed information about companies across all industries, including contact info, reviews, and operating hours.

So what could you do with all this business data?

- **Build business lead lists** for sales & marketing
- **Enrich your CRM** with up-to-date contact details
- **Analyze competitors** in any Swiss city or industry
- **Power local apps or directories** with structured business data
- **Track trends** in business categories and regions

### 🤑 Cost of usage

You are only charged for what you get: **$2 per 1,000 listings extracted scraped**. No hidden fees.

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

### 🛠️ Input

| Field      | Type      | Required | Description                                          | Example |
|------------|-----------|----------|------------------------------------------------------|---------| 
| `startUrl` | `string`  | Yes       | The search results page link                         | `https://www.local.ch/en/q/zurich/general-internal-medicine` |
| `maxItems` | `integer` | No       | Max number of businesses to scrape (within budget)   | `5000` |

### 🧐 Output

Output is stored in a dataset. Each item contains extracted business information, cleaned and flattened for easy use.

Example of the extracted data:

```json
{
  "...",
  "attributes": [
    "Terrace",
    "Wifi",
    "Vegan"
  ],
  "bookingChannels_email": "reservations@example.com",
  "bookingChannels_link": "https://www.example.com/book",
  "bookingChannels_phone": "044 123 45 67",
  "categories": [
    "Restaurant",
    "Italian",
    "Pizzeria"
  ],
  "city": "Zurich",
  "email": "contact@example.com",
  "id": "abc-123",
  "images": [
    "https://bin.staticlocal.ch/...",
    "https://images.services.local.ch/..."
  ],
  "phone": "+41 44 123 45 67",
  "rating_summary_average": 4.5,
  "street": "Bahnhofstrasse 1",
  "title": "Restaurant Example",
  "website": "https://www.example.com",
  "zipCode": "8001",
  "..."
}
````

### ⚠️ Disclaimer

This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Localsearch Group PTY LTD or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

### 🔍 SEO Keywords

local.ch scraper, local.ch API, Switzerland business directory scraper, Swiss business data extraction, local.ch crawler, local.ch data scraper, Swiss company scraper, local.ch business listings, Switzerland yellow pages scraper, local.ch email scraper, local.ch phone number extractor, Swiss business leads, local.ch reviews scraper, Apify local.ch actor, scrape local.ch, extract local.ch data, Swiss business search, local.ch contact extractor

***

**Need a custom solution? Have a feature request or just want to chat?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

# Actor input Schema

## `startUrl` (type: `string`):

local.ch search results page URL

## `maxItems` (type: `integer`):

Maximum number of business details to scrape. Leave empty to scrape all results (within budget).

## Actor input object example

```json
{
  "startUrl": "https://www.local.ch/en/s/Restaurant?rid=61f378&keid=371112",
  "maxItems": 5000
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
    "startUrl": "https://www.local.ch/en/s/Restaurant?rid=61f378&keid=371112",
    "maxItems": 5000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/local-ch-search-results-scraper-ppr").call(input);

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
    "startUrl": "https://www.local.ch/en/s/Restaurant?rid=61f378&keid=371112",
    "maxItems": 5000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/local-ch-search-results-scraper-ppr").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.local.ch/en/s/Restaurant?rid=61f378&keid=371112",
  "maxItems": 5000
}' |
apify call azzouzana/local-ch-search-results-scraper-ppr --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/local-ch-search-results-scraper-ppr",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
