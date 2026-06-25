# 🚀 Propertyfinder Agents & Brokers Scraper — UAE, KSA, Qatar, Egypt & Bahrain

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Propertyfinder Agents & Brokers Scraper — UAE, KSA, Qatar, Egypt & Bahrain. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/propertyfinder-agents-brokers-search-pages-scraper?fpr=cbgdsf)

---

## Propertyfinder Agents & Brokers Scraper — UAE, KSA, Qatar, Egypt & Bahrain

### 🤩 Features

🚀 Our blazing fast Propertyfinder agents/brokers extractor 🏠 lets you search & extract agents and/or brokers information and export them to various format (JSON, CSV, HTML etc..)
🔥 Bring your search URLs, and you're good to go!
👉 It enables you to scrape rich details as contact information, experience, LinkedIn page, transactions, location, experiences, reviews & a lot more!

The scraper has a required `startUrl` parameter which is an array holding a list of direct real estate links
- Examples of valid URLs:
  - `https://www.propertyfinder.ae/en/find-agent/search?text=dianas&category_id=2`
  - `https://www.propertyfinder.sa/en/find-broker/search?location_id=11`

The actor supports scraping data from Propertyfinder in the following countries: the United Arab Emirates (AE), Saudi Arabia (SA), Qatar (QA), Egypt (EG), and Bahrain (BH)

### Looking for something else?

- If you want to search for & extract real estate ads structured data from search pages like (e.g: `https://www.propertyfinder.qa/en/search?l=9&c=2&fu=0&rp=m&ob=mr`) instead, feel free to check out the [Propertyfinder ads search results pages scraper 🏠](https://apify.com/azzouzana/propertyfinder-ads-search-results-pages-scraper).

### 🤔 Why scrape Propertyfinder?

Propertyfinder is one of the most popular real estate websites in the MENA region, with thousands of agents and brokers.

So what could you do with all these ads?

- Build a database of real estate agents or brokers for targeted outreach, partnership opportunities, or marketing campaigns.
- Analyze agent activity, listings, and specialties to understand trends, competition, and market dynamics.
- Monitor broker networks and their listings to compare services, pricing strategies, or geographical presence.
- Collect reviews, ratings, and feedback to identify top-performing agents, customer preferences, or market demand.
- Enhance existing databases by adding agent contact details, agency affiliations, or performance metrics.
- Automate data collection to save time, reduce manual errors, or scale your operations.

Sky is the limit 🚀

### 🤑 Cost of usage

The usage cost is $1 per 1,000 items.

#### Cost Calculation Example

You want to scrape **2,500 agents/brokers**.
- Total cost: (2,500 / 1,000) * $1 = **$2.50**

> **Note:** This is a Pay-Per-Event actor. You are only charged for successfully scraped items.

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).


### 🛠️ Input

| Field | Type | Description | Default value / Example |
| ----- | ---- | ----------- | ------------- |
| `startUrl` | `array` | the search page's result link | `https://www.propertyfinder.ae/en/find-agent/search?text=diana&category_id=2`
| `maxItems` | `integer` | Maximum number of items to scrape | `100`

### 🧐 Output

Output is stored in a dataset. Each item is information about an agent or a broker:

#### Output examples

The scraping result may look like this

Agent output:

![channel screenshot](https://i.ibb.co/mNPdpc7/image.png)

Broker output:

![channel screenshot](https://i.ibb.co/qRMmJjb/image.png)


### ⚠️ Disclaimer
This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Propertyfinder FZ LLC or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

#### 📬 Contact & Custom Solutions
Want to chat? Don't hesitate to reach out to us:
- **Discord**: `@azzouzana`
- **Email**: `labs@azzouzana.com`

#### Keywords
Propertyfinder, Propertyfinder scraper, Propertyfinder agents scraper, Propertyfinder brokers scraper, Real estate agents, Real estate brokers, Real estate data, Real estate scraping, Propertyfinder API, Propertyfinder data extraction, Propertyfinder agents email, Propertyfinder brokers phone number, Lead generation, Real estate leads, Dubai real estate, UAE real estate, Saudi Arabia real estate, Qatar real estate, Egypt real estate, Bahrain real estate.

# Actor input Schema

## `startUrl` (type: `string`):

Agents or brokers Search results page URL
## `maxItems` (type: `integer`):

Maximum number of items to scrape.

## Actor input object example

```json
{
  "startUrl": "https://www.propertyfinder.ae/en/find-agent/search?text=diana",
  "maxItems": 2000
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
    "startUrl": "https://www.propertyfinder.ae/en/find-agent/search?text=diana"
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/propertyfinder-agents-brokers-search-pages-scraper").call(input);

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
run_input = { "startUrl": "https://www.propertyfinder.ae/en/find-agent/search?text=diana" }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/propertyfinder-agents-brokers-search-pages-scraper").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.propertyfinder.ae/en/find-agent/search?text=diana"
}' |
apify call azzouzana/propertyfinder-agents-brokers-search-pages-scraper --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/propertyfinder-agents-brokers-search-pages-scraper",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
