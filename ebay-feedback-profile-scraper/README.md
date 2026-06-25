# 🚀 eBay Seller Reviews Scraper, supports +20 markets (By Seller URL or Username) 🚀

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the eBay Seller Reviews Scraper, supports +20 markets (By Seller URL or Username) 🚀. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/ebay-feedback-profile-scraper?fpr=cbgdsf)

---

## eBay Seller Reviews Scraper, supports +20 markets (By Seller URL or Username) 🚀

Paste a seller feedback profile URL or username and get flat JSON: ratings, comments, buyer context, linked items, verified-purchase flags, and more. Useful for seller due diligence, competitor monitoring, and reputation research.

One username works on every eBay site. Export as JSON, CSV, Excel, or Apify API.

### 🤩 Features

- **Filters & sort**: newest or most relevant; positive, neutral, or negative; received as seller, buyer, or both; photos only; exclude automated feedback
- **Worldwide**: same username on any eBay site, no regional setup
- **Review fields**: rating, comment, buyer context, verified purchase, item title/link/ID, photos, seller username & more!
- Up to **50,000 reviews per run** (one seller per run)

### 📚 How to use

1. [Create a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) - no credit card required!
2. Open this Actor in Apify Console.
3. Enter **Seller URL or username** (`seller`).
4. Set **Max reviews** and optional **Filters**.
5. Click **Start** and download reviews from the dataset tab.

Set **Max reviews** up to **50,000**.

#### Supported seller input (`seller`)

| Format | Extracted from | Example |
|--------|----------------|---------|
| Username | as entered | `cocosmartphones` |
| Feedback profile | path | `https://www.ebay.com/fdbk/feedback_profile/adidas_official` |
| Member profile (`/usr/`) | path | `https://www.ebay.com/usr/musicmagpie` |
| eBay Store (`/str/`) | store slug | `https://www.ebay.com/str/yellastore?_tab=feedback` |

Works across +20 markets!

**Sort order (`sortOrder`)**

| In the actor UI | `sortOrder` value |
| :----------------: | :------------------: |
| Most recent | `most_recent` |
| Most relevant | `most_relevant` |

#### Seller, buyer, or both

Under **Filters → Received as** (`receivedAs`):

- **Seller**: feedback from buyers (default, most common for due diligence)
- **Buyer**: feedback they left when buying from others
- **Both**: full profile

### 🤔 Why scrape eBay seller feedback?

- Check a seller before you buy
- Monitor competitor reputation
- Research product quality from buyer comments
- Track negative or positive feedback trends
- Compare sellers in the same niche

### 🤑 Cost / Pricing

**$0.7 per 1,000 reviews** ($0.7/1K) saved to your dataset. No hidden fees.

| Reviews | Cost |
| -------: | ---: |
| 100 | $0.07 |
| 1,000 | $0.7 |
| 5,000 | $3.50 |
| 10,000 | $7.00 |
| 50,000 | $35.00 |

Example: 2,500 reviews → 2,500 × $0.0007 = **$1.75**.

### 📥 Input

| Field | Type | Description | Default |
|-------|------|-------------|---------|
| `seller` | string | Feedback profile (`/fdbk/feedback_profile/`), Member profile (`/usr/`), eBay store (`/str/`), or plain username | `cocosmartphones` |
| `sortOrder` | string | Most recent or most relevant | `most_recent` |
| `maxItems` | integer | Max reviews to collect (up to 50,000) | 100 |
| `rating` | string | All, positive, negative, or neutral | `all` |
| `receivedAs` | string | Seller, buyer, or both | `seller` |
| `imagesOnly` | boolean | Only reviews with photos | `false` |
| `excludeAutomated` | boolean | Hide automated feedback | `false` |

Only `seller` is required.

### What you get back

Each row is one review:

- Positive, neutral, or negative rating
- Full comment text
- When it was left (e.g. "Past month")
- Buyer username (partially hidden by eBay)
- Verified purchase flag
- Item title, link, and ID when available
- Buyer review photo URLs (`reviewImageUrls`)
- Seller username
& much more!

Only reviews go to the dataset. No summary rows.

### Example output (one review)

```json
{
  "feedbackModuleId": "2418366557022",
  "feedbackId": "2418366557022",
  "feedbackCardVersion": "FEEDBACK_CARD_V3",
  "sellerUsername": "adidas_official",
  "scrapedAt": "2026-06-22T13:46:32.257Z",
  "rating": "POSITIVE",
  "ratingAccessibilityText": "Positive feedback rating",
  "comment": "GREAT shoes and fast free shipping!!!",
  "hasReadMoreLink": true,
  "contextTime": "Past month",
  "contextText": "b***t (370)",
  "contextAccessibilityText": "Feedback left by buyer.",
  "buyerUsernameMasked": "b***t",
  "buyerFeedbackScore": 370,
  "verifiedPurchase": true,
  "verifiedPurchaseText": "Verified purchase",
  "imageCount": 1,
  "hasImages": true,
  "reviewImageId": "tQIAAeSw5eRpMa7l",
  "reviewImageIdType": "ZOOM_GUID",
  "reviewImageTitle": "Item photo(s) from verified buyer",
  "reviewImageUrls": [
    "https://i.ebayimg.com/00/s/MTQ0MFgxMDgw/z/tQIAAeSw5eRpMa7l/$_1.JPG?set_id=8800005007"
  ],
  "itemId": "157967067512",
  "itemTitle": "adidas men Lite Racer 4.0 Shoes",
  "itemTitleRaw": "adidas men Lite Racer 4.0 Shoes (#157967067512)",
  "itemUrl": "https://www.ebay.it/itm/157967067512",
  "itemDomain": "ebay.it",
  "itemActionType": "VIEW_ITEM",
  "trackingSellerUsername": "adidas_official",
  "trackingItemId": "157967067512",
  "trackingFeedbackTab": "NONE",
  "trackingOperationId": "4364374",
  "trackingModuleDetail": "148133",
  "trackingSid": "p4364374.m148133.l155433"
}
````

### Example input

```json
{
  "seller": "https://www.ebay.com/fdbk/feedback_profile/adidas_official",
  "maxItems": 100,
  "sortOrder": "most_recent",
  "receivedAs": "seller"
}
```

```json
{
  "seller": "musicmagpie",
  "maxItems": 200,
  "receivedAs": "both"
}
```

### Tips

- Start with a small **Max reviews** (50–100) to preview output before a large run.
- Several sellers: one run per seller, or separate scheduled jobs.
- Schedule runs to track the same seller daily or weekly.

### Export & integrations

Dataset download, API, webhooks, Google Sheets, Zapier, Make, and other Apify integrations.

### ❓ FAQ

**How do I find a seller's feedback page?**\
On eBay, open the seller's feedback section and copy the URL from the browser. See [Supported seller input](#supported-seller-input). Plain username works too.

**Can I scrape more than one seller in a single run?**\
No. One seller per run. Run again for another seller or use scheduled jobs.

**What's the difference between seller, buyer, and both?**\
Seller = reviews others left when they sold. Buyer = reviews they left when buying. Both = full profile.

**Which eBay countries are supported?**\
All of them.

**Can I filter only negative reviews?**\
Yes. Set `rating` to `negative` under Filters.

**How many reviews can I get per run?**\
Up to **50,000** via **Max reviews**. eBay may cap how far back public feedback goes; you get everything available in that window.

**How much does it cost?**\
$0.7 per 1,000 reviews ($0.7/1K)

**Do I need an eBay account?**\
No.

**What export formats are available?**\
JSON, CSV, Excel, and API.

### 🔎 SEO Keywords

eBay seller reviews scraper, eBay feedback scraper, eBay seller feedback, scrape eBay reviews, eBay reputation scraper, eBay seller rating data, eBay buyer feedback export, eBay negative feedback monitor, eBay seller due diligence, eBay competitor reviews, eBay feedback profile, eBay reviews API, eBay feedback scraper worldwide, Apify eBay scraper, eBay review dataset, eBay seller trust score, eBay verified purchase reviews

### 🔍 Looking for something else?

[Browse thousands of scrapers on Apify Store](https://apify.com/store?fpr=cbgdsf)

### 📬 Contact us

**Need a custom workflow, higher limits, or help getting started?**

- 💬 **Discord:** `@azzouzana`
- 📧 **Email:** <labs@azzouzana.com>

### ⚠️ Disclaimer

This actor is not affiliated with eBay. Trademarks belong to their respective owners. It only collects publicly visible feedback data and does not access content behind login or private accounts.

# Actor input Schema

## `seller` (type: `string`):

Feedback profile URL (/fdbk/feedback\_profile/…), member URL (/usr/…), store URL (/str/…), mweb URL (?username=…), or plain username. One seller per run.

## `sortOrder` (type: `string`):

Most recent (newest first) or most relevant.

## `maxItems` (type: `integer`):

Maximum reviews to collect for this seller (up to 50,000).

## `rating` (type: `string`):

Filter by feedback rating. Leave as all ratings for every rating.

## `receivedAs` (type: `string`):

Seller = feedback received as seller. Buyer = feedback left as buyer. Both = full profile.

## `imagesOnly` (type: `boolean`):

Only reviews that include photos.

## `excludeAutomated` (type: `boolean`):

Hide auto-generated eBay feedback.

## Actor input object example

```json
{
  "seller": "https://www.ebay.com/fdbk/feedback_profile/adidas_official",
  "sortOrder": "most_recent",
  "maxItems": 100,
  "rating": "all",
  "receivedAs": "seller",
  "imagesOnly": false,
  "excludeAutomated": false
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
    "seller": "https://www.ebay.com/fdbk/feedback_profile/adidas_official",
    "maxItems": 100
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/ebay-feedback-profile-scraper").call(input);

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
    "seller": "https://www.ebay.com/fdbk/feedback_profile/adidas_official",
    "maxItems": 100,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/ebay-feedback-profile-scraper").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "seller": "https://www.ebay.com/fdbk/feedback_profile/adidas_official",
  "maxItems": 100
}' |
apify call azzouzana/ebay-feedback-profile-scraper --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/ebay-feedback-profile-scraper",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
