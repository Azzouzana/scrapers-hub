# 🚀 Subito.it Classifieds Scraper — Motori, Market, Immobili & Lavoro (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Subito.it Classifieds Scraper — Motori, Market, Immobili & Lavoro (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/subito-scraper-pro-by-search-url?fpr=cbgdsf)

---

## Subito.it Classifieds Scraper — Motori, Market, Immobili & Lavoro (By Search URL)

### 🤩 Features

🚀 Our blazing fast Subito.it scraper 🇮🇹 lets you extract classified ads' information and export them to various formats (JSON, CSV, HTML etc..)
🔥 Bring your search URL, and you're good to go! **All categories supported**: Motori, Market, Immobili, Lavoro and more.
👉 It enables you to scrape rich details as title, descriptions, photos, locations, features, price, seller contact information (emails and phone numbers included if available) and a lot more.

### 📚 How to use this actor

1. 👉 [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required!
2. 🎉 Just click the **"Get Started"** button and complete a quick signup.
3. 💰 A free account includes enough credits to test this actor.
4. ⏳ Enjoy scraping for the free trial period, no commitment or upfront payment required.

The scraper has a required `searchUrl` parameter which is a valid Subito.it search URL (optionally with filters applied). All categories are supported:
- 🚗 **Motori / Motors** — `https://www.subito.it/annunci-italia/vendita/accessori-moto/?q=piaggio`
- 🛒 **Market / Marketplace** — `https://www.subito.it/annunci-italia/vendita/informatica/?q=iphone+7&shp=true`
- 🏠 **Immobili / Real Estate** — `https://www.subito.it/annunci-italia/vendita/ville-singole-e-a-schiera/?q=villa`
- 💼 **Lavoro / Jobs** — `https://www.subito.it/annunci-italia/vendita/lavoro/?q=java`
- Any other Subito.it search URL with filters applied

### 🤔 Why scrape Subito.it?

Subito.it is Italy's largest classified ads platform, with hundreds of thousands of active listings across all categories — there's definitely something for you out there!

So what could you do with all these ads?

- Find deals on used goods, cars, or real estate
- Do market data analysis and price tracking
- Build seller or agent contact lists (emails and phone numbers)
- Collect listing data for research or personal purposes
- Identify trends across categories and regions
- Compare prices across different sellers and locations

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

### 🤑 Cost of usage

The average cost of using this scraper is $1.5 per 1,000 listings scraped, no hidden fees.

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

Emails are partially masked for free users. Subscribe to a paid plan to reveal them.

### 🛠️ Input

| Field | Type | Description | Default value / Example |
| ----- | ---- | ----------- | ------------- |
| `searchUrl` | `string` | The Subito.it search URL to scrape | `https://www.subito.it/annunci-italia/vendita/usato/?q=iphone` |
| `maxItems` | `number` | Maximum number of listings to scrape | `100` |

### 🧐 Output

Output is stored in a dataset. THe data structure varies by category ( Motors / Marketplace / Real Estate / Jobs ). but the golden rule is that everything you see in the Subito.it would be extracted.

### 🔎 SEO Keywords

Subito.it scraper, Subito scraper API, scrape Subito.it listings, Subito.it data extraction, Subito.it crawler, Italy classifieds scraper, Subito annunci scraper, Subito auto scraper, Subito immobili scraper, Subito lavoro scraper, Subito market scraper, Subito.it phone number extractor, Subito.it email extractor, Subito.it price tracker, Italian marketplace scraper, Subito.it API alternative, web scraping Subito.it, Subito.it dataset, extract Subito listings, Subito.it lead generation, scrape Italian classifieds, Subito motori scraper, Subito real estate scraper, Subito job listings scraper, Apify Subito actor, Subito.it automation, Subito vendita scraper, annunci Italia scraper, Italian used goods scraper, Subito.it contact scraper, scraper Subito.it, estrarre dati Subito.it, scraping annunci Subito, Subito.it estrazione dati, scraper annunci Italia, estrarre numeri di telefono Subito.it, estrarre email Subito.it, Subito.it raccolta dati, scraper auto usate Italia, scraper immobili Italia, scraper offerte lavoro Subito, Subito.it automazione, annunci usato scraper, mercatino Subito scraper, estrazione contatti Subito.it, scraper case in vendita Italia, Subito.it esportazione dati, cercare annunci Subito automaticamente, lista email venditori Subito, scraper moto Subito.it

### 🔍 **Looking for something else?**
Feel free to explore [+4,000 pre-built scrapers on Apify Store](https://apify.com/store?fpr=cbgdsf) for more options!

### ⚠️ Disclaimer
This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Subito.it S.r.l. or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

#### 📞 Contact Me

**Need a custom solution? Have a feature request or just want to chat?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: [labs@azzouzana.com](mailto:labs@azzouzana.com)

# Actor input Schema

## `searchUrl` (type: `string`):

The Subito.it search URL to scrape.
## `maxItems` (type: `integer`):

Maximum number of items to scrape.

## Actor input object example

```json
{
  "searchUrl": "https://www.subito.it/annunci-italia/vendita/usato/?q=iphone",
  "maxItems": 100
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
const input = {};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/subito-scraper-pro-by-search-url").call(input);

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
run = client.actor("azzouzana/subito-scraper-pro-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{}' |
apify call azzouzana/subito-scraper-pro-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/subito-scraper-pro-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
