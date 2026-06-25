# 🚀 Thomasnet Supplier Directory Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Thomasnet Supplier Directory Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/thomasnet-supplier-directory-scraper?fpr=cbgdsf)

---

## Thomasnet Supplier Directory Scraper (By Search URL)

### 🤩 Overview

**Thomasnet** scraper: paste **suppliers or companies search URLs**, get **company profiles** in your dataset, and export as **JSON, CSV**, or Excel.

- One main field: `startUrl`
- Company profile data: name, phone, website, address, products, news, emails, and more
- Pricing: **$1 per 1,000** results
- One row per supplier, ready for CRM, spreadsheets, or your own tools

### 📚 How to use this actor

1. [Create a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) if you need one.
2. On [thomasnet.com](https://www.thomasnet.com), run a **suppliers or companies search** (keyword, category, location — whatever you need).
3. Copy the **full URL** from your browser’s address bar.
4. Paste it into **`startUrl`**, set **`maxItems`**, and start the run.

Example:

`https://www.thomasnet.com/suppliers/search?searchterm=air&search_type=all&search_ref=search`

Only **`startUrl`** is required.

### 🤔 Why Thomasnet data?

Thomasnet is a go-to directory for **industrial suppliers and manufacturers** in North America. This actor helps you turn a search results page into a structured list you can actually work with.

- Lead generation: build supplier lists by product, region, or keyword
- Sales and sourcing: compare companies, contacts, and capabilities
- Market research: export profiles for analysis in sheets or BI tools
- Repeatable lists: save the same `startUrl` and run again when you need a fresh snapshot

### 🤑 Cost of usage

**$1 per 1,000** supplier profiles.

| Profiles | Cost |
| -------: | ----------------: |
| 100 | $0.10 |
| 1,000 | $1.00 |
| 10,000 | $10.00 |

### 🆓 Free tier limitations

On the **free Apify plan**, trial limits usually apply:

- **Sample data:** up to **5 profiles** per run
- **Daily cap:** **5 runs** per day (UTC)
- **Between runs:** at least **30 minutes** before the next run

[Upgrade to a paid plan](https://apify.com/pricing?fpr=cbgdsf) when you need higher volume.

### 🛠️ Input

| Field | Type | Description | Example |
| ----- | ---- | ----------- | ------- |
| `startUrl` | string | Full Thomasnet suppliers or companies search URL | From the address bar after your search |
| `maxItems` | number | Max supplier profiles to collect | `100` |

### 🧐 Output

One object per supplier in the default dataset. Example (abbreviated arrays):

```json
{
  "__typename": "Company",
  "news": null,
  "additionalInformation": [
    {
      "__typename": "CompanyAdditionalInformation",
      "id": "100001",
      "title": "Industrial Dryers",
      "description": "Example product brochure entry for compressed-air drying equipment.",
      "image": "https://cdn.example.com/thumbs/100001.png",
      "url": "https://cdn.example.com/docs/100001.pdf",
      "section": "PRODUCT",
      "type": "DOCUMENT"
    },
    {
      "__typename": "CompanyAdditionalInformation",
      "id": "100002",
      "title": "Rotary Screw Compressors",
      "description": "Example product image and overview for rotary screw compressor lines.",
      "image": "https://cdn.example.com/thumbs/100002.jpg",
      "url": "https://cdn.example.com/images/100002.jpg",
      "section": "PRODUCT",
      "type": "IMAGE"
    }
  ],
  "brands": [
    { "__typename": "CompanyBrand", "name": "Brand A" },
    { "__typename": "CompanyBrand", "name": "Brand B" }
  ],
  "headingBrands": null,
  "whitepapers": null,
  "products": null,
  "families": [
    { "__typename": "CompanyFamily", "id": "200001", "name": "Compressors" },
    { "__typename": "CompanyFamily", "id": "200002", "name": "Dryers" }
  ],
  "videos": [
    {
      "__typename": "CompanyVideo",
      "id": "abc12345",
      "title": "Acme Industrial Supply Inc. Company Overview",
      "text": null,
      "description": "Example company overview video description.",
      "duration": "PT02M30S",
      "url": "https://cdn.example.com/videos/abc12345.mp4",
      "image": "https://cdn.example.com/thumbs/abc12345.jpg",
      "label": "Company Overview",
      "player": null,
      "type": "COMPANY_OVERVIEW",
      "uploadedDate": "2024-01-15T00:00:00.000Z"
    }
  ],
  "otherHeadings": null,
  "certificationTotals": null,
  "affiliatedMemberOf": null,
  "affiliationFeaturedMembers": null,
  "affiliationContactUrl": null,
  "affiliationCompanyLabel": null,
  "tgramsId": "1234567",
  "name": "Acme Industrial Supply Inc.",
  "logoUrl": null,
  "logoTitle": "Acme Industrial Supply Inc. Company Logo",
  "website": "https://www.acme-industrial-example.com",
  "isClaimed": true,
  "xometryVerified": false,
  "isAdvertiser": true,
  "isTopResponder": false,
  "primaryPhone": "(555) 123-4567",
  "description": "Manufacturer and distributor of industrial components. Custom fabrication, installation, and maintenance services available.",
  "descriptionByCompany": "Acme Industrial Supply Inc. is a full-service supplier established in 1992, serving manufacturers across the Midwest.",
  "annualSales": "$10 - 24.9 Mil",
  "numberEmployees": "10-49",
  "yearFounded": "1992",
  "otherActivities": ["I", "S"],
  "premiums": ["X"],
  "address": {
    "__typename": "CompanyAddress",
    "address1": "100 Industrial Park Dr.",
    "address2": null,
    "address3": null,
    "city": "Springfield",
    "state": "IL",
    "stateName": "Illinois",
    "zip": "62701",
    "zip4": null,
    "country": "USA",
    "county": null,
    "latitude": 39.7817,
    "longitude": -89.6501
  },
  "tier": "VERIFIED",
  "type": "D",
  "isMultiLocation": false,
  "mainLocationTgramsId": "1234567",
  "mainLocationName": "Acme Industrial Supply Inc.",
  "locationTypes": [
    {
      "__typename": "CompanyLocationType",
      "id": 999,
      "name": "No Location Type Found"
    }
  ],
  "heading": null,
  "headings": null,
  "personnel": [
    {
      "__typename": "Personnel",
      "name": "Jane Doe",
      "title": "Sales Director"
    }
  ],
  "catalogType": null,
  "social": [
    {
      "__typename": "CompanySocialMedia",
      "accountId": "https://blog.acme-industrial-example.com/",
      "type": "BLOGS"
    }
  ],
  "isAffiliationPage": false,
  "companyAd": {
    "__typename": "CompanyAd",
    "adurl": "https://www.acme-industrial-example.com/",
    "adimg": "https://cdn.example.com/pad/1234567/ad.jpg"
  },
  "ads": null,
  "profileUrl": "https://www.thomasnet.com/company/acme-industrial-supply-inc-1234567/profile",
  "emails": ["sales@acme-industrial-example.com"]
}
````

### ❓ FAQ

#### How much does a run cost?

About **$1 per 1,000** profiles. Your actual bill depends on how many rows you collect and your Apify plan.

#### Why do I only get 5 results?

On the **free plan**, runs are capped at **5 profiles** so you can check data quality before scaling up.

#### Can I scrape more than one search?

Yes — run the actor again with a different `startUrl`, or increase `maxItems` on a paid plan.

#### Is it legal to scrape Thomasnet?

This actor only collects **publicly visible** supplier information from search and profile pages. It is **not affiliated** with Thomasnet. For general guidance, see Apify’s article on [web scraping legality](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf).

### 📬 Contact

- 💬 **Discord:** `@azzouzana`
- 📧 **Email:** <labs@azzouzana.com>

### ⚠️ Disclaimer

This actor is **not affiliated** with Thomasnet. Trademarks belong to their respective owners.

# Actor input Schema

## `startUrl` (type: `string`):

Full Thomasnet suppliers discovery or companies search URL

## `maxItems` (type: `integer`):

Maximum supplier profiles to scrape

## Actor input object example

```json
{
  "startUrl": "https://www.thomasnet.com/suppliers/search?searchterm=air&search_type=all&search_ref=search",
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
    "startUrl": "https://www.thomasnet.com/suppliers/search?searchterm=air&search_type=all&search_ref=search",
    "maxItems": 10
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/thomasnet-supplier-directory-scraper").call(input);

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
    "startUrl": "https://www.thomasnet.com/suppliers/search?searchterm=air&search_type=all&search_ref=search",
    "maxItems": 10,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/thomasnet-supplier-directory-scraper").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.thomasnet.com/suppliers/search?searchterm=air&search_type=all&search_ref=search",
  "maxItems": 10
}' |
apify call azzouzana/thomasnet-supplier-directory-scraper --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/thomasnet-supplier-directory-scraper",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
