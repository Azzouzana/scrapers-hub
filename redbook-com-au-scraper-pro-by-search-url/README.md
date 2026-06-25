# 🚀 RedBook.com.au Car Research Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the RedBook.com.au Car Research Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/redbook-com-au-scraper-pro-by-search-url?fpr=cbgdsf)

---

## RedBook.com.au Car Research Scraper (By Search URL)

### ⚡ Features

Our **redbook.com.au** car research scraper pulls vehicle listings from a search URL and saves them as JSON, CSV, and more. Bot protection is handled automatically - just paste a URL and go 🚀

✅ Title, price guide, body type, transmission, engine, fuel economy, drive type
✅ ANCAP, VESR & UCSR safety ratings
✅ Main Image and details URL
✅ release date & more

Supports any **redbook.com.au/cars/results/** search URL with filters.

### 🛠️ How to use this actor

1. [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) - no credit card required.
2. Open the actor, add your **Input**, and start a run.
3. Use the free tier to see if the output fits your project before scaling up.

The scraper needs a **`startUrl`**: a search results URL from redbook.com.au with your filters applied in the browser.

- Must start with: `https://www.redbook.com.au/cars/results/`
- Example: `https://www.redbook.com.au/cars/results/?q=(And.ANCAPRating.5+stars+only._.Price.range(..15000).)`

### 💰 Cost of usage

**$1.50 per 1,000 listings** scraped. No hidden fees.

| Listings | Cost |
| -------: | ---: |
| 100 | ~$0.15 |
| 1,000 | ~$1.50 |
| 5,000 | ~$7.50 |

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

A **paid plan** lifts those caps. [Apify pricing](https://apify.com/pricing?fpr=cbgdsf).

### 📥 Input

| Field | Type | Description | Example |
| ----- | ---- | ----------- | ------- |
| `startUrl` | `string` | Search results URL from redbook.com.au | `https://www.redbook.com.au/cars/results/?q=...` |
| `maxItems` | `number` | Listings to collect | `10` |

### 📦 Output

Each dataset row is one car listing. Example:

```json
{
      "id": "SPOT-ITM-528301",
      "ancap_rating_scale": 5,
      "ancap_rating_score": 5,
      "bodyStyle": "Hatch",
      "body_style": "Hatch, 5 door",
      "detailsUrl": "https://www.redbook.com.au/cars/details/2019-mitsubishi-mirage-es-la-manual-my20/SPOT-ITM-528301?Cr=2",
      "drive": "Front Wheel Drive",
      "engine_description": "3cyl 1.2L Aspirated Petrol Engine",
      "gear_type": "5spd Manual",
      "imageUrl": "https://redbook.pxcrush.net/redbookcars/car/spec/S0001VZB.jpg?pxc_method=gravityfill&pxc_bgtype=self&pxc_size=720,480",
      "priceAudMax": 10800,
      "priceAudMin": 7000,
      "priceDisplay": "$7,000 - $10,800",
      "priceGuideUrl": "https://www.redbook.com.au/_details/api/v1/price-guide/redbookcars/SPOT-ITM-528301",
      "priceType": "range",
      "releaseDate": "Jun 2019",
      "section": "standard",
      "title": "2019 Mitsubishi Mirage ES LA Manual MY20",
      "ucsr_rating_scale": 5,
      "ucsr_rating_score": 1,
      "vesr_rating_scale": 6,
      "vesr_rating_score": 3.5
    }
````

### ⚠️ Limitations

Redbook.com.au caps search results at **420 listings** per search URL. This is a website limitation, not an actor limitation.

If your search returns more than 420 results, narrow it down by using more specific filters (e.g. by make, model, year range, price range) so each URL stays within the 420 cap. You can run the actor multiple times with different filtered URLs to cover a larger set.

Need to scrape beyond this limit automatically? Contact us, we can assess interest and consider implementing support for bypassing the 420-result cap.

### 🔍 SEO keywords

redbook scraper, redbook.com.au scraper, redbook API, scrape redbook, car research scraper Australia, car valuation data, redbook to CSV, redbook to JSON, Apify redbook, Australian car data scraper, car price guide scraper

#### 📞 Contact us

**Need a custom solution? Have a feature request or just want to chat?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

### ⚖️ Disclaimer

This actor is an **independent tool**, not affiliated with or endorsed by redbook.com.au, Carsales Network, or related companies. Trademarks belong to their owners.

# Actor input Schema

## `startUrl` (type: `string`):

A redbook.com.au search results URL with your filters applied (must start with https://www.redbook.com.au/cars/results/).

## `maxItems` (type: `integer`):

Maximum car listings to scrape

## Actor input object example

```json
{
  "startUrl": "https://www.redbook.com.au/cars/results/?q=(And.ANCAPRating.5+stars+only._.Price.range(..15000).)",
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
    "startUrl": "https://www.redbook.com.au/cars/results/?q=(And.ANCAPRating.5+stars+only._.Price.range(..15000).)",
    "maxItems": 10
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/redbook-com-au-scraper-pro-by-search-url").call(input);

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
    "startUrl": "https://www.redbook.com.au/cars/results/?q=(And.ANCAPRating.5+stars+only._.Price.range(..15000).)",
    "maxItems": 10,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/redbook-com-au-scraper-pro-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.redbook.com.au/cars/results/?q=(And.ANCAPRating.5+stars+only._.Price.range(..15000).)",
  "maxItems": 10
}' |
apify call azzouzana/redbook-com-au-scraper-pro-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/redbook-com-au-scraper-pro-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
