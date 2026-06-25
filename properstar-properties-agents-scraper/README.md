# 🚀 Properstar Scraper — Property Listings & Agents (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Properstar Scraper — Property Listings & Agents (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/properstar-properties-agents-scraper?fpr=cbgdsf)

---

## Properstar Scraper — Property Listings & Agents (By Search URL)

### 🤩 Features

**One actor, two modes** — paste a Properstar **property search URL** or **agent directory URL** and get structured rows in the default dataset. Export as **JSON, CSV, Excel**, or via Apify API.

- **All Properstar domains** — `properstar.com`, `.fr`, `.de`, `.es`, `.ch`, and more; one `startUrl` field, no coding.
- **Rich property data** — price (with full `priceValues` breakdown), multilingual titles, rooms, areas, geo, photos, amenities, listing contacts (**emails & phones**), and direct listing URLs.
- **Rich agent & agency data** — agent **emails**, **phones**, office address, logos, listing statistics, ranking metrics, parent franchise/office, and place context for lead gen.
- **Automatic pagination** — collects results page by page until your `maxItems` limit is reached.
- **Large listing searches** — need more than ~2,000 properties from one search? The actor can go beyond Properstar’s usual result cap (up to your `maxItems`).
- **You control volume** — set `maxItems` to match your budget; only saved rows count toward usage.
- **Clean, export-ready rows** — one listing or agent per line, ready for CRM, spreadsheets, and automations.

#### Supported URL types

| Mode | Example URL |
|------|-------------|
| Property search | `https://www.properstar.com/germany/buy?price.max=640000&preferredAmenities=Balcony` |
| Agent directory (query) | `https://www.properstar.fr/agents?placeId=ChIJZwDTqCNu5kcRuHqnfKluXDU` |
| Agent directory (localized path) | `https://www.properstar.es/espana/madrid/agentes-inmobiliarios` |

The actor detects the mode automatically from your URL.

### 📚 How to use

1. 👉 [Create a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) — no credit card required.
2. Open this actor and click **Start**.
3. Paste your **Properstar URL** into `startUrl`.
4. Set `maxItems` and run.

**How to get the URL**

- **Listings:** run a property search with your filters on any Properstar site, then copy the full URL from the browser address bar.
- **Agents:** open an agent/agency directory (by city, district, or place) and copy that page URL.

### 🤔 Why scrape Properstar?

Properstar (ListGlobally) covers international buy/rent inventory and agent networks in one platform — useful when you need **cross-border property data** or **B2B lead lists** without manual copy-paste.

- **Market intelligence** — track prices, new listings, and inventory by search filters across countries.
- **Lead generation** — export agent emails, phones, agency names, and listing volumes for outreach.
- **CRM & enrichment** — flat JSON rows map cleanly to HubSpot, Salesforce, Airtable, or internal databases.
- **Monitoring** — re-run the same `startUrl` on a schedule to spot new listings or agents in a market.
- **Research & analytics** — feed repeatable datasets into dashboards, maps, and valuation models.

### 🤑 Cost

**$0.7 per 1,000 results** (each listing or agent saved to your dataset). Transparent pricing, no hidden fees.

### 🆓 Free tier limitations

- **Sample:** up to **5 items** per run (listings or agents)
- **Daily quota:** **5 runs** per day (UTC)
- **Gap:** at least **30 minutes** between runs

[Upgrade your Apify plan](https://apify.com/pricing?fpr=cbgdsf) to remove these limits.

### 🛠️ Input

| Field | Type | Description | Default / Example |
|-------|------|-------------|-------------------|
| `startUrl` | string | Properstar property search or agent directory URL | `https://www.properstar.com/germany/buy?price.max=640000` |
| `maxItems` | integer | Maximum listings **or** agents to scrape | `100` |

### 🧐 Output

Each dataset row includes `recordType`: **`listing`** (property search) or **`agent`** (agent directory).

#### Property listings — data fields

| Group | Fields |
|-------|--------|
| **Identity** | `listingId`, `originalId`, `reference`, `hash`, `listingUrl`, `searchUrl`, `page`, `scrapedAt` |
| **Title** | `title` (primary), `title_en`, `title_fr`, `title_de`, … (`title_{lang}`), `automaticTitle` |
| **Price** | `price`, `currency`, `priceShow`, `priceValues` (array: type, currency, value), `priceLastChange`, `isPriceChangeBoosted` |
| **Property** | `transactionType`, `transactionTypeName`, `propertyType`, `propertyTypeName`, `propertySubType`, `propertySubTypeName`, `categoryId`, `constructionYear`, `state`, `timeZone` |
| **Size & rooms** | `numberOf_rooms`, `numberOf_bedrooms`, `numberOf_bathrooms`, … (`numberOf_*`), `livingArea`, `totalArea`, `plotArea`, `areaUnit`, `area` |
| **Location** | `city`, `postcode`, `country`, `latitude`, `longitude`, `location` |
| **Media** | `imageUrl`, `imageCount`, `images` (all photo URLs) |
| **Contacts** | `contactUsers` (name, **email**, **phone**), `contactAccountId`, `showContact` |
| **Amenities** | `missingAmenities`, `replacedAmenities` |
| **Ranking** | `relevanceScore` |

#### Agents — data fields

| Group | Fields |
|-------|--------|
| **Identity** | `agentAccountId`, `topAccountId`, `userId`, `agentSlug`, `searchUrl`, `page`, `origin`, `scrapedAt`, `rankScore` |
| **Contact** | `email`, `phone`, `fullName`, `avatar`, `userStatus`, `profileCompleted`, `registrationType`, `userUpdateDate` |
| **Account / agency** | `accountName`, `accountName_{lang}`, `accountType`, `accountAddress`, `accountLocality`, `accountPostCode`, `accountPhone`, `accountMobile`, `accountWebsiteUrl`, `accountLogo`, `accountOriginalId`, `isGlobalAgent`, `internalRating` |
| **Parent office / franchise** | `topAccountName`, `topAccountName_{lang}`, `topAccountType`, `topAccountLogo` |
| **Agency link** | `agencyName`, `agencyAccountId`, `userIsAgent` |
| **Listing stats** | `listingsStat_numberOfListings`, `listingsStat_numberOfListingsSell`, `listingsStat_numberOfListingsRent`, `listingsStat_numberOfListingsLuxury`, `listingsStat_medianPrice`, … |
| **Profile metrics** | `metric_HasNameAndPicture`, `metric_NumListingsGlobal`, `metric_ListingsCountInSearchArea`, `metric_LastLoginDate`, `metric_IsGlobalAgent`, … (`metric_*` and `metric_*_score`) |
| **Place context** | `placeId`, `placeLocality`, `placeCountry`, `placeLatitude`, `placeLongitude` |
| **Profile** | `countryISO`, `mainLanguage`, `spokenLanguages`, `userOriginalId` |

Contact fields (email, phone) are included when they appear on the Properstar page.

#### Listing example

```json
{
  "recordType": "listing",
  "listingId": 115513496,
  "originalId": "11827-58978",
  "reference": "58978",
  "title": "Stylish 2-Room Apartment with Balcony, Underfloor Heating & Lift",
  "title_en": "Stylish 2-Room Apartment with Balcony, Underfloor Heating & Lift",
  "title_de": "Stilvolle 2-Zimmer-Wohnung mit Balkon, Fußbodenheizung & Aufzug",
  "automaticTitle": "Condo for sale in Berlin, Germany",
  "price": 335000,
  "currency": "EUR",
  "priceShow": true,
  "priceValues": [{ "currencyId": "EUR", "type": "Original", "value": 335000 }],
  "priceLastChange": null,
  "transactionType": "Sell",
  "propertyType": "Apartment",
  "numberOf_rooms": 2,
  "numberOf_bedrooms": 1,
  "numberOf_bathrooms": 1,
  "city": "Berlin",
  "postcode": "12167",
  "country": "DE",
  "latitude": 52.520007,
  "longitude": 13.404954,
  "state": "Published",
  "timeZone": "Europe/Berlin",
  "imageUrl": "https://files-api.properstar.com/api/v2/files/…/2",
  "imageCount": 8,
  "images": ["https://files-api.properstar.com/api/v2/files/…/2", "…"],
  "contactUsers": [{ "firstName": "Buy Berlin Investments GmbH", "email": "info@buyberlin.co.uk", "phone": "+49 30 240 356 68" }],
  "listingUrl": "https://www.properstar.com/listing/115513496",
  "searchUrl": "https://www.properstar.com/germany/buy?price.max=640000",
  "page": 1,
  "scrapedAt": "2026-06-19T16:00:00.000Z"
}
````

#### Agent example

```json
{
  "recordType": "agent",
  "agentAccountId": 6180118,
  "topAccountId": 26282,
  "userId": 1420298,
  "rankScore": 108.99,
  "email": "cgensollen@junot.fr",
  "phone": "+33142736230",
  "fullName": "Charles GENSOLLEN",
  "accountName": "Charles GENSOLLEN",
  "accountName_fr": "Charles GENSOLLEN",
  "accountType": "Agent",
  "accountAddress": "11, rue de Tournon",
  "accountLocality": "Paris 6ème",
  "accountPostCode": "75006",
  "accountLogo": "https://files-api.properstar.com/api/v2/files/…/1",
  "listingsStat_numberOfListings": 11,
  "listingsStat_numberOfListingsSell": 11,
  "listingsStat_medianPrice": 2120000,
  "metric_NumListingsGlobal": 7,
  "metric_IsGlobalAgent": true,
  "topAccountName": "Junot",
  "topAccountName_fr": "Junot",
  "topAccountType": "Franchise",
  "placeId": "ChIJZwDTqCNu5kcRuHqnfKluXDU",
  "placeLocality": "Paris",
  "placeCountry": "France",
  "agentSlug": "charles-gensollen",
  "searchUrl": "https://www.properstar.fr/agents?placeId=ChIJZwDTqCNu5kcRuHqnfKluXDU",
  "page": 1,
  "scrapedAt": "2026-06-19T16:00:00.000Z"
}
```

### ❓ FAQ

#### How much does it cost to run this actor?

**$0.7 per 1,000 results** — No hidden fees.

#### Why am I only getting 5 results?

On the **free Apify plan**, each run is limited to **5 items** so you can verify data quality before upgrading. Subscribe to any **paid Apify plan** to remove that cap and use your full `maxItems` setting.

#### Can I scrape all Properstar country sites?

Yes — any Properstar domain works for **property searches** and **agent directories** (including paths like `agentes-inmobiliarios`). Use **one mode per run**: a search URL for listings, or an agent directory URL for agents. The actor detects the mode automatically and paginates until `maxItems` or no further results.

#### Why did my run stop before reaching `maxItems`?

Common reasons: (1) **no further results** for that URL, (2) **free-tier** item cap, (3) **daily rate limit** (5 runs/day, 30-minute gap for free users), or (4) you reached your **`maxItems`** limit.

### 🔎 SEO Keywords

Properstar scraper, Properstar listings scraper, Properstar agents scraper, scrape Properstar agents, Properstar agent emails, Properstar.com scraper, Properstar.fr scraper, international real estate scraper, property search scraper, real estate agent directory scraper, Apify Properstar actor, Properstar API alternative, web scraping Properstar, export Properstar listings JSON, immobilier scraper Properstar, agentes inmobiliarios scraper, scrape property prices Properstar, ListGlobally scraper, worldwide property listings scraper, real estate lead generation scraper

### 🔍 Looking for something else?

[Browse thousands of scrapers on Apify Store](https://apify.com/store?fpr=cbgdsf)

### 📬 Contact

- 💬 **Discord:** `@azzouzana`
- 📧 **Email:** <labs@azzouzana.com>

### ⚠️ Disclaimer

This actor is **not affiliated** with Properstar or ListGlobally. Trademarks belong to their respective owners.

# Actor input Schema

## `startUrl` (type: `string`):

Full Properstar search results URL from any Properstar domain (properstar.com, properstar.fr, etc.).

## `maxItems` (type: `integer`):

Maximum property listings to scrape. (Effective limit also respects run budget and free-tier cap)

## Actor input object example

```json
{
  "startUrl": "https://www.properstar.ca/canada/montreal/rent/apartment-house/1p-bedroom?preferredAmenities=AirConditioning",
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
    "startUrl": "https://www.properstar.ca/canada/montreal/rent/apartment-house/1p-bedroom?preferredAmenities=AirConditioning",
    "maxItems": 100
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/properstar-properties-agents-scraper").call(input);

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
    "startUrl": "https://www.properstar.ca/canada/montreal/rent/apartment-house/1p-bedroom?preferredAmenities=AirConditioning",
    "maxItems": 100,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/properstar-properties-agents-scraper").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.properstar.ca/canada/montreal/rent/apartment-house/1p-bedroom?preferredAmenities=AirConditioning",
  "maxItems": 100
}' |
apify call azzouzana/properstar-properties-agents-scraper --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/properstar-properties-agents-scraper",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
