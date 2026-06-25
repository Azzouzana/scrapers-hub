# 🚀 Immobiliare.it Agencies Scraper

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Immobiliare.it Agencies Scraper. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/immobiliare-agencies-scraper-by-search-url?fpr=cbgdsf)

---

## Immobiliare.it Agencies Scraper

### 🤩 Features

- **Scrape agency listings** from Immobiliare.it, paste an agencies search page url and get structured agency data.
- **Automatic pagination** : follows all pages of the listing so you can collect many agencies in one run.
- **Rich agency details** : name, address, description, image, phones, opening hours, listings count, and more.
- **Optional social & email extraction** : turn on `Extract socials` to get Facebook, Instagram, Twitter, LinkedIn, WhatsApp and emails when available, to the best of our efforts.
- **Export** results to JSON, CSV, and other formats.
- **Enterprise-grade resilience**for reliable runs at scale.

### 📚 How to use

1. [Sign up for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf).
2. Open the actor, click **Start** and enter a **Start URL** (e.g. an agencies list page from immobiliare.it).
3. Results are written to the run’s default dataset.

Use the same URL you see in the browser when you open an agencies list on immobiliare.it (e.g. `https://www.immobiliare.it/agenzie-immobiliari/milano`).

### Input

| Field | Type | Description | Default/Example |
| ----- | ---- | ----------- | ------- |
| Start URL | string (required) | Agencies listing URL. | `https://www.immobiliare.it/agenzie-immobiliari/roma/?contractId=2` |
| Max items | integer | Maximum number of agencies to scrape. | `500` |
| Extract socials | boolean | Extract social links and emails when available, to the best of our efforts. | `false` |

### Output

One dataset item per agency: name, address, description, image, phones, opening hours, listing counts, and (if “Extract socials” is on) Facebook, Instagram, Twitter, LinkedIn, WhatsApp and emails when found.

### Cost

**Billing** is pay-per-event (PPE):

1. **Dataset item** : You pay for each agency pushed to the dataset at **$1 per 1,000 agencies**.
2. **Extract socials** (optional) : If enabled, each agency where we find at least one social link or email incurs one extra event (**extracted-socials**), currently $0.001 per event ($1 per 1,000 such agencies).

**Examples:**

| Scenario | Calculation | Approximate cost |
| -------- | ----------- | ----------------- |
| 500 agencies, **Extract socials off** | 500 × × $0.001 (default) | $0.5 |
| 500 agencies, **Extract socials on**, 200 with socials/emails | 500 × $0.001 (default) + 200 × $0.001 (socials) | $0.7 |
| 1,000 agencies, **Extract socials on**, all 1,000 with socials | 1,000 × $0.001 (default) + 1,000 × $0.001 (socials) | $2.0 |

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 agencies** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

### 📬 Contact us

**Need a custom solution, a feature request, or just want to chat?**
We'd love to hear from you.

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: [labs@azzouzana.com](mailto:labs@azzouzana.com)

### SEO

immobiliare.it agencies scraper, scrape immobiliare.it agencies, agenzie immobiliari scraper, Italian real estate agencies data, immobiliare.it API agencies, real estate agency scraper Italy, export agenzie immobiliari, Apify immobiliare agencies, agenzie immobiliari Italia, real estate contacts Italy

### Disclaimer

This actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Immobiliare.it Group or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

# Actor input Schema

## `startUrl` (type: `string`):

Agencies search URL (e.g. https://www.immobiliare.it/agenzie-immobiliari/roma/?contractId=2)
## `maxItems` (type: `integer`):

Maximum number of agencies to scrape
## `extractSocials` (type: `boolean`):

Try to extracts email addresses & social media profiles (Facebook, Instagram, Twitter, LinkedIn), WhatsApp numbers for agencies to the best of our effort

## Actor input object example

```json
{
  "startUrl": "https://www.immobiliare.it/agenzie-immobiliari/roma/",
  "maxItems": 100,
  "extractSocials": false
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
    "startUrl": "https://www.immobiliare.it/agenzie-immobiliari/roma/",
    "maxItems": 100
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/immobiliare-agencies-scraper-by-search-url").call(input);

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
    "startUrl": "https://www.immobiliare.it/agenzie-immobiliari/roma/",
    "maxItems": 100,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/immobiliare-agencies-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.immobiliare.it/agenzie-immobiliari/roma/",
  "maxItems": 100
}' |
apify call azzouzana/immobiliare-agencies-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/immobiliare-agencies-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
