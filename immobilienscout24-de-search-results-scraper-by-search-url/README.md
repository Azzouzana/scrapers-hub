# 🚀 ImmoScout24 Property Listings Scraper — Germany, Austria & Switzerland (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the ImmoScout24 Property Listings Scraper — Germany, Austria & Switzerland (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/immobilienscout24-de-search-results-scraper-by-search-url?fpr=cbgdsf)

---

## ImmoScout24 Property Listings Scraper — Germany, Austria & Switzerland (By Search URL)

### 🤩 Features

🚀 Our blazing fast immobilienscout24 search results scraper🏠 lets you extract real estate ads' information and export them to various formats (JSON, CSV, HTML etc..)
🌍 Supports 🇩🇪 **Germany** (immobilienscout24.de), 🇦🇹 **Austria** (immobilienscout24.at), and 🇨🇭 **Switzerland** (immoscout24.ch)!
🔥 Bring your search URL and you're good to go!
👉 It enables you to scrape rich details as title, photos, characteristics, dates publishers info & much more!

### 📚 How to use this actor

1. 👉 [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required!
2. 🎉 Just click the **"Get Started"** button and complete a quick signup.
3. 💰 A free account includes enough credits to test this actor.
4. ⏳ Enjoy scraping for the free trial period, no commitment or upfront payment required.

The scraper has a required `startUrl` parameter which is an immobilienscout24 search URL (optionally with filters applied)
- Examples of valid URLs:
  - 🇩🇪 **Germany:** `https://www.immobilienscout24.de/Suche/radius/wohnung-mieten?centerofsearchaddress=Pforzheim;75181;;;;;&numberofrooms=4.0-5.0&geocoordinates=48.87681;8.73005;5.0&enteredFrom=result_list`
  - 🇦🇹 **Austria:** `https://www.immobilienscout24.at/regional/oesterreich/wohnung-mieten`
  - 🇨🇭 **Switzerland:** `https://www.immoscout24.ch/en/real-estate/rent/city-bern`

### 🤔 Why scrape immobilienscout24?

immobilienscout24 is the largest real estate platform in the German-speaking market, covering 🇩🇪 **Germany** (immobilienscout24.de), 🇦🇹 **Austria** (immobilienscout24.at), and 🇨🇭 **Switzerland** (immoscout24.ch), with hundreds of thousands of ads. There's definitely something for you out there!

So what could you do with all these ads?

- Find real estate for sale nearby
- Do market data analysis
- Build a real estate agent email list
- Collect housing data for research or personal purposes
- Compare collected data with home value index
- Use the data for overall real estate data analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

### 🤑 Cost of usage

This actor uses **Pay Per Event (PPE)** billing at **$1 per 1,000 results**. You pay for each listing pushed to the dataset (see [pricing](https://apify.com/pricing?fpr=cbgdsf)). The actor automatically respects your run budget and stops when the limit is reached.

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

### 🛠️ Input

| Field | Type | Description | Default |
| ----- | ---- | ----------- | ------- |
| `startUrl` | `string` | The search page's result link (supports `.de`, `.at`, and `.ch` domains) | *(required)* |
| `maxItems` | `number` | Maximum number of listings to scrape. (Auto-paginates until limit) | `5000` (max `15000`) |

### 🧐 Output

Output is stored in a dataset. Each item is information about a real estate item:

### 🔍 **Looking for something else?**
Feel free to explore [+4,000 pre-built scrapers on Apify Store](https://apify.com/store?fpr=cbgdsf) for more options!

#### SEO Keywords
immobilienscout24 scraper, scrape immobilienscout24, German real estate scraper, Austrian real estate scraper, Swiss real estate scraper, immobilienscout24.de API, immobilienscout24.at scraper, immoscout24.ch scraper, real estate data Germany, real estate data Austria, real estate data Switzerland, Wohnung mieten scraper, Haus kaufen scraper, Apify immobilienscout24, Immobilien Daten, real estate listings Germany, real estate listings Austria, real estate listings Switzerland

#### 📬 Contact & Custom Solutions
Want to chat? Don't hesitate to reach out to us:
- **Discord**: `@azzouzana`
- **Email**: `labs@azzouzana.com`

### ⚠️ Disclaimer
This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Immobilien Scout GmbH or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

# Actor input Schema

## `startUrl` (type: `string`):

search URLs to start with (Supports .de, .ch & .at)
## `maxItems` (type: `integer`):

Maximum number of items (ads) to return. The actor auto-paginates until this limit is reached.

## Actor input object example

```json
{
  "startUrl": "https://www.immobilienscout24.de/Suche/radius/wohnung-mieten?centerofsearchaddress=Pforzheim;75181;;;;;&geocoordinates=48.87681;8.73005;5.0",
  "maxItems": 500
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
    "startUrl": "https://www.immobilienscout24.de/Suche/radius/wohnung-mieten?centerofsearchaddress=Pforzheim;75181;;;;;&geocoordinates=48.87681;8.73005;5.0",
    "maxItems": 500
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/immobilienscout24-de-search-results-scraper-by-search-url").call(input);

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
    "startUrl": "https://www.immobilienscout24.de/Suche/radius/wohnung-mieten?centerofsearchaddress=Pforzheim;75181;;;;;&geocoordinates=48.87681;8.73005;5.0",
    "maxItems": 500,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/immobilienscout24-de-search-results-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.immobilienscout24.de/Suche/radius/wohnung-mieten?centerofsearchaddress=Pforzheim;75181;;;;;&geocoordinates=48.87681;8.73005;5.0",
  "maxItems": 500
}' |
apify call azzouzana/immobilienscout24-de-search-results-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/immobilienscout24-de-search-results-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
