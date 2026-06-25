# 🚀 Pincali.com Property Listings Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Pincali.com Property Listings Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/pincali-com-scraper-by-search-url?fpr=cbgdsf)

---

## Pincali.com Property Listings Scraper (By Search URL)

### 🤩 Features

🚀 Our blazing-fast Pincali.com search scraper 🏠 lets you extract Mexican real estate listings and export them to various formats (JSON, CSV, HTML, etc.)
🔥 Bring your Pincali search URL and you're good to go!
👉 It extracts rich details including title, description, price, location with GPS coordinates, bedrooms, bathrooms, parking spaces, area, lot size, amenities, financing options, full-resolution photos, agent/publisher info and more.

### 📚 How to use this actor

1. 👉 [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required!
2. 🎉 Just click the **"Get Started"** button and complete a quick signup.
3. 💰 A free account includes enough credits to test this actor.
4. ⏳ Enjoy scraping for the free trial period, no commitment or upfront payment required.

The scraper has a required `startUrl` parameter which is a Pincali search URL (optionally with filters applied).
- Examples of valid URLs:
  - `https://www.pincali.com/en/properties/houses-for-sale`
  - `https://www.pincali.com/en/properties/apartments-for-rent-in-monterrey-nuevo-leon`
  - `https://www.pincali.com/en/properties/land-for-sale-in-cancun-quintana-roo`

### 🤔 Why scrape Pincali.com?

Pincali is a leading Mexican real estate marketplace powered by EasyBroker, listing properties across all of Mexico — houses, apartments, land, offices and more.

So what could you do with all these listings?

- Find real estate for sale or rent across Mexico
- Do market data analysis on Mexican property prices
- Build a real estate agent/broker contact list
- Collect housing data for research or investment purposes
- Track price trends across neighborhoods, cities and states
- Use the data for overall real estate analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

### 🛠️ Input

| Field | Type | Description | Default |
| ----- | ---- | ----------- | ------- |
| `startUrl` | `string` | The Pincali search results URL | *(required)* |
| `maxItems` | `number` | Maximum number of listings to return. Auto-paginates until limit. | `2` (max `15000`) |

### 🤑 Cost of usage

This actor uses **Pay Per Event (PPE)** billing at **$1.5 per 1,000 listings** ($0.001/listing). The actor automatically respects your run budget and stops when the limit is reached.

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

### 🧐 Output

Output is stored in a dataset. Each item is a parsed real estate listing with the following fields:

| Field | Description |
| ----- | ----------- |
| `url` | Listing page URL |
| `propertyId` | Internal property ID (e.g. `EB-VO9662`) |
| `title` | Listing title |
| `description` | Full description text |
| `propertyType` | Type of property (House, Apartment, Land, etc.) |
| `operationType` | Sale or Rent |
| `price` | Numeric price |
| `currency` | Currency code (e.g. `MXN`) |
| `priceText` | Formatted price string (e.g. `$15,800,000 MXN`) |
| `state` | Mexican state |
| `city` | City |
| `neighborhood` | Neighborhood |
| `fullAddress` | Full street address |
| `latitude` / `longitude` | GPS coordinates |
| `bedrooms` | Number of bedrooms |
| `bathrooms` | Number of bathrooms |
| `parkingSpaces` | Number of parking spaces |
| `areaM2` | Total area in m² |
| `lotSizeM2` | Lot size in m² |
| `features` | Array of features (bedrooms, area, year built, condition, etc.) |
| `amenities` | Array of amenities (garden, terrace, security, pool, etc.) |
| `financingOptions` | Array of financing options (Mortgage, INFONAVIT, etc.) |
| `images` | Array of full-resolution image URLs |
| `agent` | Publisher info: name, organization, profile URL, avatar, logo |
| `publishedAt` | Publication date |
| `canonicalUrl` | Canonical URL |
| `alternateUrls` | Alternate language URLs (en, es-MX, pt-BR) |
| `scrapedAt` | Timestamp of when the data was scraped |

#### Output example

```json
{
  "url": "https://www.pincali.com/en/home/espectacular-casa-en-venta-condado-de-sayavedra",
  "propertyId": "EB-VO9662",
  "title": "ESPECTACULAR CASA EN VENTA",
  "description": "Terreno 800 m2, Construcción 425 m2. Jardín, sala, comedor...",
  "propertyType": "House",
  "operationType": "Sale",
  "price": 15800000,
  "currency": "MXN",
  "priceText": "$15,800,000 MXN",
  "state": "Estado de México",
  "city": "Atizapán de Zaragoza",
  "neighborhood": "Condado de Sayavedra",
  "fullAddress": "BUCKINGHAM, Condado de Sayavedra, Atizapán de Zaragoza, Estado de México",
  "latitude": 19.5833078,
  "longitude": -99.3088788,
  "bedrooms": 3,
  "bathrooms": 3,
  "parkingSpaces": 4,
  "areaM2": 425,
  "lotSizeM2": 800,
  "features": ["3 bedrooms", "3 bathrooms, 3 half baths", "4 parking spaces", "425 m² total space", "800 m² Lot Size", "Year Built: 2025", "Condition: New"],
  "amenities": ["Cistern", "Garden", "Terrace", "Equipped Kitchen", "24 Hour Security", "Pets allowed"],
  "financingOptions": ["Mortgage", "FOVISSSTE", "INFONAVIT / COFINAVIT"],
  "images": ["https://assets.easybroker.com/property_images/5879662/103389272/EB-VO9662.jpg?version=1773962465"],
  "agent": {
    "name": "ALEJANDRO WALLE",
    "organization": "Inteligencia Inmobiliaria",
    "profileUrl": "https://www.pincali.com/en/real-estate-agents/alejandrow_2",
    "avatarUrl": "https://assets.easybroker.com/profile_images/588807/...",
    "organizationLogo": "https://assets.easybroker.com/organization_logos/50511/..."
  },
  "publishedAt": "2026-03-19T17:22:01-06:00",
  "scrapedAt": "2026-03-19T23:23:25.179Z"
}
````

### 🔍 **Looking for something else?**

Feel free to explore [+4,000 pre-built scrapers on Apify Store](https://apify.com/store?fpr=cbgdsf) for more options!

#### SEO Keywords

pincali scraper, scrape pincali, Mexico real estate scraper, pincali.com API, real estate data Mexico, Apify pincali, EasyBroker scraper, Mexican property listings, pincali casas en venta, pincali departamentos en renta, pincali terrenos en venta, pincali bienes raíces, pincali inmuebles México, pincali propiedades en venta, scraper inmobiliario México, datos inmobiliarios México, pincali CDMX, pincali Monterrey, pincali Guadalajara, pincali Cancún, pincali vivienda México

#### 📬 Contact & Custom Solutions

Want to chat? Don't hesitate to reach out to us:

- **Discord**: `@azzouzana`
- **Email**: `labs@azzouzana.com`

### ⚠️ Disclaimer

This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Pincali, EasyBroker or any of their subsidiaries. All trademarks mentioned are the property of their respective owners.

# Actor input Schema

## `startUrl` (type: `string`):

The Pincali search URL to scrape.

## `maxItems` (type: `integer`):

Maximum number of listings to scrape

## Actor input object example

```json
{
  "startUrl": "https://www.pincali.com/en/properties/houses-for-sale",
  "maxItems": 10
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
    "startUrl": "https://www.pincali.com/en/properties/houses-for-sale",
    "maxItems": 10
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/pincali-com-scraper-by-search-url").call(input);

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
    "startUrl": "https://www.pincali.com/en/properties/houses-for-sale",
    "maxItems": 10,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/pincali-com-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.pincali.com/en/properties/houses-for-sale",
  "maxItems": 10
}' |
apify call azzouzana/pincali-com-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/pincali-com-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
