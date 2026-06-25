# 🚀 Marktplaats.nl Scraper — Auto, Goods & Services (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Marktplaats.nl Scraper — Auto, Goods & Services (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/marktplaats-nl-scraper-pro-by-search-url?fpr=cbgdsf)

---

## Marktplaats.nl Scraper — Auto, Goods & Services (By Search URL)

### ✨ Features

**Marktplaats** is the Netherlands’ go-to marketplace for second-hand goods, cars, services, and more. This actor turns any **search or category** results page you care about into structured data you can use in your own tools, spreadsheets, or apps.

- Search the whole site with a **keyword**, URL, or browse by **category** (books, auto, etc.).
- **Transparent, affordable pricing** at $1/1K with no hidden fees.
- **Enterprise-grade reliability**: We extract data for a living; you can rely on us.
- **Super fast**: Thousands of listings extracted in seconds.

Result pages are paged automatically until your **`maxItems`** cap or the end of the list (the site can cap how many pages exist for a very broad search).

### 📚 How to use this actor

1. 👉 [Create a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) (no credit card required).
2. 🎉 Open the actor, set **Input**, and start a run.
3. 🇳🇱 On [marktplaats.nl](https://www.marktplaats.nl), set **location**, **price**, **category**, and any other filters you need, then **copy the full URL** from the address bar into **`startUrl`**.

**Examples of valid `startUrl` values:**

- 🔎 Keyword search: `https://www.marktplaats.nl/q/charvel/`
- 📂 Category: `https://www.marktplaats.nl/l/boeken/geschiedenis-vaderland/`

### 🆓 Free tier

We want you to try the actor before you commit. For **free** accounts, typical limits (your deployment may use vault settings) include:

- **Up to 5 listings** per run—enough to check data quality
- **5 runs** per calendar day (UTC)
- **At least 30 minutes** before starting another run

> Limits can change with platform and vault configuration.

A **paid Apify plan** lifts those trial caps. See [Apify pricing](https://apify.com/pricing?fpr=cbgdsf).

### Cost of usage

**$1.50 per 1,000 listings** scraped. No hidden fees.

| Listings | Cost |
| -------: | ---: |
| 100 | ~$0.15 |
| 1,000 | ~$1.50 |
| 5,000 | ~$7.50 |
| 10,000 | ~$15.00 |

### 📥 Input

| Field | Type | Description | Example |
| ----- | ---- | ----------- | ------- |
| `startUrl` | `string` | Full Marktplaats **search** (`/q/...`) or **category** (`/l/...`) URL, with your filters in the path/query if needed | `https://www.marktplaats.nl/l/boeken/geschiedenis-vaderland/` |
| `maxItems` | `number` | Maximum listings to collect in one run (capped in the actor, e.g. 10,000) | `100` |

### 📦 Output

The dataset is **one row per listing**. Fields depend on what Marktplaats exposes for that category; you typically get things like id, title, price info, link to the ad, and a main picture URL, plus any attribute fields the list includes.
Example:
```json
{
  "itemId": "m2356221854",
  "title": "✅ Renault R-Link SD kaart 11.45 Navigatie update 2025-2026",
  "description": "Renault: r-link sd kaart r link rlink opel vivaro intellilink navi 80 originele europa update renault r link sd kaart, 2024-2025 versie 11.25 Voor 30 euro + 2025-2026 versie 11.45 Voor 45 euro origine",
  "categorySpecificDescription": "Renault: r-link sd kaart r link rlink opel vivaro intellilink navi 80 originele europa update renault r link sd kaart, 2024-2025 versie 11.25 Voor 30 euro + 2025-2026 versie 11.45 Voor 45 euro originele renault rlink1 navigatie update sd kaart voor h...",
  "thinContent": false,
  "priceInfo_priceCents": 3000,
  "priceInfo_priceType": "FIXED",
  "priceInfo_suppressZeroCents": false,
  "location_cityName": "Zwolle",
  "location_countryName": "Nederland",
  "location_countryAbbreviation": "NL",
  "location_distanceMeters": -1000,
  "location_isBuyerLocation": false,
  "location_onCountryLevel": false,
  "location_abroad": false,
  "location_latitude": 52.521745079828,
  "location_longitude": 6.0956700052652,
  "date": "Vandaag",
  "sellerInformation_sellerId": 20949857,
  "sellerInformation_sellerName": "Henk NavSd.",
  "sellerInformation_showSoiUrl": true,
  "sellerInformation_showWebsiteUrl": false,
  "sellerInformation_isVerified": true,
  "categoryId": 1477,
  "priorityProduct": "DAGTOPPER",
  "videoOnVip": false,
  "urgencyFeatureActive": false,
  "napAvailable": false,
  "attributes_condition": "Nieuw",
  "attributes_delivery": "Ophalen of Verzenden",
  "attributes_region": "Heel Europa",
  "extendedAttributes_brand": "Renault R-Link  Opel Vivaro  Opel Monano",
  "extendedAttributes_type": "Update",
  "extendedAttributes_region": "Heel Europa",
  "extendedAttributes_condition": "Nieuw",
  "traits": [
    "DEALER_PACKAGE_BASIC",
    "DAG_TOPPER_7DAYS",
    "DAG_TOPPER",
    "PACKAGE_FREE",
    "URL",
    "DAG_TOPPER_3DAYS",
    "EXTRA_IMAGES_SNIPPET"
  ],
  "verticals": [
    "software_navigations_and_geography",
    "barcode-supported",
    "computers_and_software"
  ],
  "searchType": "TokenMatch",
  "reserved": true,
  "vipUrl": "https://www.marktplaats.nl/v/computers-en-software/navigatiesoftware/m2356221854-renault-r-link-sd-kaart-11-45-navigatie-update-2025-2026",
  "picture": "https://images.marktplaats.com/api/v1/listing-mp-p/images/6c/6cc32b38-a1a7-4fb0-8b95-294d208cac31?rule=ecg_mp_eps$_85.jpg"
}
````

### Looking for more?

Browse [thousands of Actors on Apify](https://apify.com/store?fpr=cbgdsf) for other marketplaces and sources.

### Disclaimer

This tool is **not** affiliated with Marktplaats. Use it in line with the site’s terms and acceptable use. Trademarks belong to their owners.

#### 📞 Contact Us

**Need a custom solution? Have a feature request or just want to chat?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

### SEO keywords

marktplaats scraper, marktplaats.nl listings, Dutch classifieds data, marktplaats to JSON, marktplaats to CSV, Apify marktplaats, Netherlands marketplace scraper, second hand listings Netherlands

# Actor input Schema

## `startUrl` (type: `string`):

Full Marktplaats search or category URL

## `maxItems` (type: `integer`):

Max listings in the datase

## Actor input object example

```json
{
  "startUrl": "https://www.marktplaats.nl/l/boeken/geschiedenis-vaderland/",
  "maxItems": 100
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
    "startUrl": "https://www.marktplaats.nl/l/boeken/geschiedenis-vaderland/",
    "maxItems": 100
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/marktplaats-nl-scraper-pro-by-search-url").call(input);

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
    "startUrl": "https://www.marktplaats.nl/l/boeken/geschiedenis-vaderland/",
    "maxItems": 100,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/marktplaats-nl-scraper-pro-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.marktplaats.nl/l/boeken/geschiedenis-vaderland/",
  "maxItems": 100
}' |
apify call azzouzana/marktplaats-nl-scraper-pro-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/marktplaats-nl-scraper-pro-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
