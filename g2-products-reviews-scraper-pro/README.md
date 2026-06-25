# 🚀 G2 Product Reviews Scraper PRO

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the G2 Product Reviews Scraper PRO. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/g2-products-reviews-scraper-pro?fpr=cbgdsf)

---

## 🚀 G2 Product Reviews Scraper PRO

**⚡ Super fast • 💰 Low-cost • 📊 Structured • 📈 Built for scale**  
Collect published product reviews from [G2](https://www.g2.com) for competitive intelligence, sentiment pipelines, or dashboards. Point the actor at a product, choose how results should be ordered, and cap how many reviews you need - sky is the limit!

---

#### ✅ What you get

Pull detailed review rows aligned with what analysts expect from G2: scores, prose responses, reviewer context, categories with direct links, optional video flags, and stable review URLs. Use **any public product URL** you would open in the browser - or just paste the **product slug**.

The actor is built with engineering excellence in mind:

- **Flexible product input:** Full `g2.com` product URLs (reviews tab, compare pages, single-review pages, regional sites) **or** a bare slug such as `hubspot-marketing-hub`.
- **Comprehensive, rich output:** 40+ data points per review - more than you’d typically need.
- **Multiple sort options:** Most recent, most helpful, highest / lowest rated, and G2 default.
- **Volume control:** Set how many reviews to collect per product (up to **30,000** per run, within plan limits).
- **Optional filters:** Star rating condition (`minimum` / `maximum`) + star value (1–5), and “published within the last N days” to narrow the window.
- **Lightning fast:** Give it a spin & see!

> More features are coming soon: category's products scraping, G2 search pages scraping & much more. Stay tuned!
---

### 🛠️ How to use this actor

1. [Create a free Apify account](https://apify.com/sign-up) if you do not have one.  
2. Open the actor, fill in **Input**, and start a run.  
3. Download results from the **Dataset** tab (JSON, CSV, or via API).  

**🔗 Product URL or slug**

- Full URLs, for example:  
  `https://www.g2.com/products/slack/reviews`  
  `https://www.g2.com/products/hubspot-marketing-hub/reviews/12345678`  
  `https://fr.g2.com/products/clickup`  
- Or **slug only:** `slack`, `zendesk-for-customer-service`, etc.

**🔀 Sort order (`sortOrder`)**

| In the actor UI | `sortOrder` value |
| :--------------: | :----------------: |
| G2 default | `g2_default` |
| Most recent | `most_recent` |
| Most helpful | `most_helpful` |
| Highest rated | `highest_rated` |
| Lowest rated | `lowest_rated` |

Default: **`most_recent`**.

**🎚️ Limits & filters**

- **`maxItems`** - Maximum reviews to collect for the product (minimum **5**, maximum **30,000** on input; effective cap may be lower on free plans).  
- **`starFilterCondition`** (optional) - Choose `minimum` (at or above) or `maximum` (at or below).  
- **`starFilterValue`** (optional) - Star value used by the selected condition (1–5).  
- Set **both** `starFilterCondition` and `starFilterValue` to apply a star filter; if one is missing, star filtering is skipped.
- **`lookbackDays`** (optional) - Only reviews published within the last *N* days.

**Star filter examples**

- `starFilterCondition=minimum` + `starFilterValue=4` → include 4-star and 5-star reviews.
- `starFilterCondition=maximum` + `starFilterValue=2` → include 1-star and 2-star reviews.

---

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 reviews** per run - enough to check data quality.  
- **Daily cap:** **5 runs** per calendar day (UTC).  
- **Between runs:** at least **30 minutes** before you can start another run.

> Free-user limits can change with platform load and your intended usage. [**Upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf) for unlimited extraction!

---

### 📥 Input

| Field | Type | Description |
| :-----: | :----: | :-----------: |
| `productUrl` | `string` | Any `g2.com` product URL that contains `/products/{slug}/`, or the product slug alone. |
| `sortOrder` | `string` | How reviews are ordered (see table above). |
| `maxItems` | `integer` | Max reviews to collect (up to 30,000 per run). |
| `starFilterCondition` | `string` | Optional. `minimum` or `maximum`. Must be paired with `starFilterValue` to apply star filtering. |
| `starFilterValue` | `integer` | Optional. Star threshold 1–5 used with `starFilterCondition`. |
| `lookbackDays` | `integer` | Optional. Only reviews published within the last N days. |

---

### 📦 Output

Each **dataset item** is one review, and has this format:

```json
{
	"reviewId": "7083825",
	"categories": [
		{
			"id": 36,
			"name": "Marketing Automation",
			"url": "https://www.g2.com/categories/36"
		}
	],
	"company_segment": 179,
	"company_segment_label": "Small-Business",
	"contract_length": "1 Year",
	"contract_length_weight": 12,
	"country": "United States",
	"discount": null,
	"discount_weight": null,
	"ease_of_admin": 7,
	"ease_of_doing_business_with": 6,
	"ease_of_setup": 7,
	"ease_of_use": 7,
	"hate_theme_humanized": "Uiux",
	"helpful": 0,
	"love_theme_humanized": "Usability",
	"meets_requirements": 7,
	"nps": 9,
	"nps_score": 5,
	"price": 6,
	"product_id": 364,
	"product_name": "HubSpot Marketing Hub",
	"productSlug": "hubspot-marketing-hub",
	"published": true,
	"published_at": "2026-04-16T16:12:41.189-05:00",
	"quality_of_support": 3,
	"rating": 4.5,
	"response_type": "text",
	"review_source": "g2gives",
	"reviewUrl": "https://www.g2.com/products/hubspot-marketing-hub/reviews/7083825",
	"security_confidence": 7,
	"security_importance": 7,
	"service_location": null,
	"source_type": "g2gives",
	"status": "approved",
	"submitted_at": "2022-09-08T10:23:10.031-05:00",
	"switched_from_other_product": false,
	"switched_from_products": [],
	"switched_reason": null,
	"switching_theme": null,
	"switching_theme_humanized": null,
	"switching_themes": null,
	"title": "Best marketing automation platform out there ",
	"user_name": "Anna Kate M.",
	"video_review_submitted_at": null,
	"videoIncluded": false,
	"whatDoYouDislike": "The customer support has seriously gone downhill.",
	"whatDoYouLike": "The AI tools have been a great addition and the email marketing analytics and email health is top tier.",
	"whatProblemsOrBenefits": "They allow our clients to gain valuable insights and analytics while also streamlining their processes. Best marketing automation platform out there"
}
````

### 📬 Contact & Support

**Need a custom solution? Have a feature request?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

***

### 🔍 SEO keywords

G2 scraper, G2 reviews scraper, G2 product reviews, scrape G2 reviews, software reviews data, B2B reviews API, G2 dataset, Apify G2, competitor reviews, review sentiment data, G2 CSV export, G2 JSON export

***

### ⚖️ Disclaimer

This actor is an **independent tool**, not affiliated with, endorsed by, or sponsored by G2 or its affiliates. All trademarks belong to their respective owners.

# Actor input Schema

## `productUrl` (type: `string`):

Any g2.com product page whose path includes /products/{slug}/ (reviews, compare, single review, etc.), or the product slug alone (e.g. hubspot-marketing-hub).

## `sortOrder` (type: `string`):

Same options as the G2 site “G2 Sort” menu: Most recent, Most helpful, Highest rated, Lowest rated. Optional mapping reference samples are saved in the run Key-value store under G2\_MAPPING\_REFERENCES.

## `maxItems` (type: `integer`):

Maximum reviews to collect (capped at 30000).

## `starFilterCondition` (type: `string`):

Choose whether to include reviews with ratings at or above (minimum) or at or below (maximum) a selected star value.

## `starFilterValue` (type: `integer`):

Star value used with the selected condition (1–5). Example: minimum + 4 means 4 stars and above.

## `lookbackDays` (type: `integer`):

Only reviews with published\_at within this many days. Omit or 0 for all time.

## Actor input object example

```json
{
  "productUrl": "https://www.g2.com/products/hubspot-marketing-hub/reviews",
  "sortOrder": "most_recent",
  "maxItems": 2000
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
    "productUrl": "https://www.g2.com/products/hubspot-marketing-hub/reviews",
    "maxItems": 2000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/g2-products-reviews-scraper-pro").call(input);

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
    "productUrl": "https://www.g2.com/products/hubspot-marketing-hub/reviews",
    "maxItems": 2000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/g2-products-reviews-scraper-pro").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "productUrl": "https://www.g2.com/products/hubspot-marketing-hub/reviews",
  "maxItems": 2000
}' |
apify call azzouzana/g2-products-reviews-scraper-pro --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/g2-products-reviews-scraper-pro",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
