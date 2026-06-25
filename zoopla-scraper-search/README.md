# 🚀 Zoopla.co.uk Scraper — Buy, Rent, New Homes & Agents (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Zoopla.co.uk Scraper — Buy, Rent, New Homes & Agents (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/zoopla-scraper-search?fpr=cbgdsf)

---

## Zoopla.co.uk Scraper — Buy, Rent, New Homes & Agents (By Search URL)

Your one-stop scraper for Zoopla **properties** and **estate agents**. Paste a search URL from your browser and get clean, flat JSON — ready for spreadsheets, CRMs, dashboards, or AI workflows.

Works with **for-sale**, **to-rent**, **new homes**, and **find-agents** searches.

### 🤩 Features

#### Property searches (buy, rent, new homes)

- **Full listing details** — price, price history, beds, baths, sqft, description, tenure
- **Address & map** — display address, postcodes, coordinates
- **Features & flags** — key bullets, furnished state, chain-free, and more
- **Photos, floor plans & EPC** — gallery, floor plan images, energy ratings and documents
- **NTS info** — council tax, service charge, ground rent, utilities, parking
- **Nearby & transport** — schools, parks, stations with distances
- **Agent on the listing** — branch name, phone, branch page link
- **Optional agent emails** — add the branch email to every listing when you need leads
- **Smart pagination** — works past Zoopla’s ~1,000-result cap on property searches
- **Speed and reliability** are built into our DNA 😉

#### Find-agents searches (estate agent directory)

- **Branch overview** — name, logo, address, postcode, description
- **Full profile** — about text and team members (name, role, photo)
- **Opening hours** — day-by-day open/close times
- **Contact & social** — phone, website, Facebook, Twitter, LinkedIn, Instagram
- **Professional memberships** — ARLA, TPO, RICS, and similar affiliations
- **Market stats** — listings for sale/rent, average prices, weeks on market
- **Optional agent emails** — same email add-on as property searches

#### For everyone

- One row per result — easy **CSV, Excel, or API** export
- **$1 per 1,000 results** (+ **$1 per 1,000** when emails are enabled)
- **No hidden fees**
- Built for **market research**, **lead gen**, and **property data pipelines**

### 📚 How to use

1. [Create a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) - no credit card required.
2. Open this Actor in Apify Console.
3. On Zoopla, run the search you want (properties or agents), then copy the URL from your address bar.
4. Paste it into **Start URL**.
5. Set **Max items** to how many results you want.
6. Turn on **Fetch agent emails** only if you need branch email addresses (+$1 per 1,000 results).
7. Click **Start** and download your data as soon as it's ready

**Example URLs**

- Buy: `https://www.zoopla.co.uk/for-sale/property/london-fields/?q=London%20Fields%2C%20London`
- Rent: `https://www.zoopla.co.uk/to-rent/property/manchester/?q=Manchester%2C%20Greater%20Manchester`
- New homes: `https://www.zoopla.co.uk/new-homes/property/london/?q=London`
- Find agents: `https://www.zoopla.co.uk/find-agents/manchester/?q=Manchester%2C+Greater+Manchester&geo_autocomplete_identifier=manchester&section=find-agents%2Festate-agents&radius=0&search_source=find-agents-triage`

### 🤔 Why scrape Zoopla?

- **Investors & analysts** — track prices, sizes, and trends by area
- **Lead generation** — agent branches, phones, websites, and optional emails
- **Agency research** — compare branches, stock levels, and time on market
- **Data teams** — feed warehouses, sheets, or internal tools with UK listing data

### 🤑 Cost / Pricing

**$1 per 1,000 results** saved to your dataset.

Enable **Fetch agent emails** to add branch emails — **+$1 per 1,000 results** (charged per row where emails are enriched).

| Results | Without emails | With emails |
| -------: | -------------: | ----------: |
| 100 | $0.10 | $0.20 |
| 1,000 | $1.00 | $2.00 |
| 10,000 | $10.00 | $20.00 |

### 🆓 Free tier limitations

On the **free Apify plan**:

- Up to **5 results** per run
- **5 runs** per day (UTC)
- At least **30 minutes** between runs
- **Emails are partially masked** when email fetching is on (e.g. `ab*****@az**.com`). Upgrade for full addresses.

[Upgrade for higher limits](https://apify.com/pricing?fpr=cbgdsf).

### 🛠️ Input

| Field | What it does | Default |
|-------|----------------|---------|
| **Start URL** | Your Zoopla property or find-agents search URL | London Fields buy example |
| **Max items** | How many listings or agent branches to collect (min 5) | 100 |
| **Fetch agent emails** | Add estate agent email to each row (+$1 per 1,000; masked on free plan) | Off |

### 🧐 What you get back

#### Property listings

Each row is one property with pricing, specs, location, features, photos, EPC, NTS details, nearby places, transport links, and the listing agent’s name and phone. Enable **Fetch agent emails** to also get the agent’s email on each row.

#### Find-agents results

Each row is one estate agent branch with description, team, opening hours, phone, email, website, social links, professional memberships, and sale/rent market stats. Enable **Fetch agent emails** to also get the branch email.

#### Example — property listing

```json
{
  "listingId": "12345678",
  "title": "2 bed flat for sale",
  "category": "residential",
  "publicationStatus": "Live",
  "detailedDescription": "Riverside Apartments, E8. Modern two-bedroom flat with open-plan living…",
  "tenure": "leasehold",
  "listingUris_detail": "https://www.zoopla.co.uk/for-sale/details/12345678/",
  "listingUris_contact": "https://www.zoopla.co.uk/for-sale/contact/12345678/",
  "counts_numBedrooms": 2,
  "counts_numBathrooms": 1,
  "counts_numLivingRooms": 1,
  "ingested_sizeSqft": 803,
  "floorArea_label": "803 sq. ft",
  "floorArea_value": 803,
  "pricing_valueLabel": "£425,000",
  "pricing_internalValue": 425000,
  "pricing_priceQualifierLabel": "Guide price",
  "pricing_pricePerFloorAreaUnit_valueLabel": "£529",
  "priceHistory_firstPublished_firstPublishedDate": "2026-01-15T10:00:00",
  "priceHistory_firstPublished_priceLabel": "£450,000",
  "priceHistory_priceChanges": [
    {
      "priceLabel": "£425,000",
      "priceChangeDate": "2026-03-01",
      "isPriceDrop": true,
      "isPriceIncrease": false,
      "percentageChangeLabel": "-5.6%"
    }
  ],
  "analyticsTaxonomy_displayAddress": "Riverside Apartments, Flat 4, Example Street, London E8",
  "analyticsTaxonomy_propertyType": "flat",
  "analyticsTaxonomy_postTownName": "London",
  "analyticsTaxonomy_outcode": "E8",
  "analyticsTaxonomy_incode": "3SE",
  "analyticsTaxonomy_numBeds": 2,
  "analyticsTaxonomy_numBaths": 1,
  "analyticsTaxonomy_chainFree": true,
  "location_coordinates_latitude": 51.5401,
  "location_coordinates_longitude": -0.0572,
  "location_postalCode": "E8 3SE",
  "location_streetName": "Example Street",
  "location_townOrCity": "London",
  "features_bullets": [
    "Two double bedrooms",
    "..."
  ],
  "features_flags_tenure_label": "Leasehold",
  "features_flags_studentFriendly": false,
  "ntsInfo": [
    { "title": "Tenure", "key": "tenure", "value": "Leasehold (125 years)" },
    "..."
  ],
  "additionalNtsInfo": [
    { "title": "Water", "key": "water", "value": "Mains" },
    "..."
  ],
  "derivedEPC_efficiencyRating": "C",
  "epc_image": null,
  "epc_pdf": null,
  "floorPlan_image": [{ "filename": "floorplan-example.jpg", "caption": "Floorplan" }],
  "propertyImage": [
    { "original": "https://example.com/listings/12345678/living-room.jpg", "caption": "Living room" },
    "..."
  ],
  "pointsOfInterest": [
    { "title": "Example Primary School", "address": "Sample Road", "type": "uk_school_primary", "distanceMiles": 0.2 },
    "..."
  ],
  "transports": [
    { "title": "Example Overground", "poiType": "national_rail_station", "distanceInMiles": 0.3 },
    "..."
  ],
  "agent_office_id": 67453,
  "agent_office_name": "Acme Estates — East London",
  "agent_profile_url": "https://www.zoopla.co.uk/find-agents/branch/acme-estates-east-london-67453/",
  "agent_phone": "020 7123 4567",
  "agent_logo_url": "https://example.com/agents/acme-logo.png",
  "agent_email": "enquiries@acme-estates.example",
  "viewCount_viewCount30day": 42,
  "scrapedAt": "2026-06-20T12:00:00.000Z"
}
````

#### Example — find-agents search output sample:

Full branch row(dummy data):

```json
{
  "agent_office_id": 16212,
  "agent_office_name": "Stirling Ackroyd - Hackney",
  "agent_slug": "stirling-ackroyd-hackney-london-16212",
  "agent_area_code": "E8",
  "agent_logo_url": "https://st.zoocdn.com/zoopla_static_agent_logo_example.png",
  "agent_profile_url": "https://www.zoopla.co.uk/find-agents/branch/stirling-ackroyd-hackney-london-16212/",
  "agent_summary": "Local estate agent branch serving Hackney and East London.",
  "agent_highlighted": false,
  "agent_address": "338 Mare Street, Kingsland, London",
  "agent_postcode": "E8 1HA",
  "agent_phone": "020 8022 5555",
  "agent_website": "https://www.stirlingackroyd.com/our-branches/hackney/",
  "agent_facebook": "https://www.facebook.com/pages/Stirling-Ackroyd-Ltd",
  "agent_twitter": "https://twitter.com/Stirling_London",
  "agent_linkedin": "https://www.linkedin.com/company/stirling-ackroyd",
  "agent_instagram": "https://www.instagram.com/stirling_ackroyd",
  "agent_about": "The Hallmark of Quality and Experience Our story began in 1873…",
  "agent_team": [
    {
      "first_name": "Jane",
      "last_name": "Smith",
      "role": "Branch Manager",
      "photo_url": "https://example.com/staff/jane-smith.jpg"
    },
    "..."
  ],
  "agent_hours": [
    { "weekday": "monday", "opens_at": "0900", "closes_at": "1800" },
    "..."
  ],
  "agent_market_stats": {
    "sale_listing_count": 16,
    "sale_avg_price": 664063,
    "sale_avg_weeks": 19,
    "rent_listing_count": 6,
    "rent_avg_price": 759,
    "rent_avg_weeks": 2
  },
  "agent_accreditations": [
    { "body": "arla", "link": "https://www.zoopla.co.uk/tips/agent-affiliation-arla/" },
    "..."
  ],
  "agent_email": "hackneysalesleads@stirlingackroyd.example",
  "scrapedAt": "2026-06-20T12:00:00.000Z"
}
```

### ❓ FAQ

**How do I get a search URL?**\
Go to zoopla.co.uk, run a property or agent search, apply your filters, then copy the URL from the address bar.

**Can I scrape both properties and agents?**\
Yes — use a property search URL or a find-agents URL. One URL per run.

**Do I always get emails?**\
No. Emails are only enriched when you turn on **Fetch agent emails**

**What’s the result limit?**\
Set **Max items** to your target. We do our best to get as much data as we realistically can.

### 🔎 SEO Keywords

Zoopla scraper, Zoopla estate agents scraper, Zoopla find agents, UK property scraper, Zoopla price history, estate agent leads, Zoopla for sale, Zoopla to rent, UK real estate data, London property listings, Apify Zoopla

### 🔍 Looking for something else?

[Browse thousands of scrapers on Apify Store](https://apify.com/store?fpr=cbgdsf)

### 📬 Contact

- 💬 **Discord:** `@azzouzana`
- 📧 **Email:** <labs@azzouzana.com>

### ⚠️ Disclaimer

This actor is not affiliated with Zoopla. Trademarks belong to their respective owners. It only collects publicly visible data and does not access content behind login or paywalls.

# Actor input Schema

## `startUrl` (type: `string`):

Paste a Zoopla search URL from your browser — for-sale, to-rent, new homes, or find-agents. Example buy: https://www.zoopla.co.uk/for-sale/property/london-fields/?q=London%20Fields%2C%20London — Example rent: https://www.zoopla.co.uk/to-rent/property/manchester/?q=Manchester%2C%20Greater%20Manchester — Example agents: https://www.zoopla.co.uk/find-agents/manchester/?q=Manchester%2C+Greater+Manchester

## `maxItems` (type: `integer`):

Maximum listings or agents to collect

## `fetchEmails` (type: `boolean`):

Fetch agents email address

## Actor input object example

```json
{
  "startUrl": "https://www.zoopla.co.uk/for-sale/property/london-fields/?q=London%20Fields%2C%20London",
  "maxItems": 100,
  "fetchEmails": false
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
    "startUrl": "https://www.zoopla.co.uk/for-sale/property/london-fields/?q=London%20Fields%2C%20London",
    "maxItems": 100,
    "fetchEmails": false
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/zoopla-scraper-search").call(input);

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
    "startUrl": "https://www.zoopla.co.uk/for-sale/property/london-fields/?q=London%20Fields%2C%20London",
    "maxItems": 100,
    "fetchEmails": False,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/zoopla-scraper-search").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.zoopla.co.uk/for-sale/property/london-fields/?q=London%20Fields%2C%20London",
  "maxItems": 100,
  "fetchEmails": false
}' |
apify call azzouzana/zoopla-scraper-search --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/zoopla-scraper-search",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
