# 🚀 Propwire Property Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Propwire Property Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/propwire-com-scraper-pro-by-search-url?fpr=cbgdsf)

---

## Propwire Property Scraper (By Search URL)

### 🤩 Features

**Propwire** search scraper: run a search in the browser, get listings in the default **dataset**, and export as **JSON, CSV**, or other Apify formats—solid for **leads**, **deals** (sourcing, screening, follow-up), market snapshots, and research.

- **Very easy to use** — one field (`startUrl`): copy your Propwire search URL and run.
- **Super fast, comprehensive data** — paginated fetching so large searches finish quickly, with full listing fields on every row.
- **Enterprise-grade reliability** - We do this for a living, you can rely on us.
- **AI-friendly output** — one row per listing, flattened for tools, automations, and AI workflows.
- **Transparent pricing** — about $1 per 1,000 listings, no hidden fees.

### 📚 How to use this actor

1. [Create a free Apify account](https://apify.com/sign-up) if you need one.
2. Open the actor, set **input**, start a run.
3. On **propwire.com**, build a search until the URL looks like `https://propwire.com/search?filters=...`. Copy the **full** URL from the address bar into **`startUrl`**. The `filters` query is JSON (URL-encoded).

![Copy the browser URL into the actor startUrl input](https://i.ibb.co/Q358NjtK/image.png)

Only **`startUrl`** is required.

### 🤔 Why Propwire data?

Propwire is built for investors and operators who want **searchable, filterable property data** in one place. This actor gives you the same result set you see in the UI, in a file or pipeline—without copying rows by hand.

- **Leads** — build lists from geography and property types you care about, then enrich, score, or hand off to CRM or dialers. One row per listing, flattened so you can match columns in sheets or your database.
- **Deals** — use Propwire’s filters (e.g. equity, type, area) in the search URL, then screen results in a spreadsheet or internal tools. Re-run the same `startUrl` when you want a new snapshot; compare runs to see what changed.
- **Market views** — export enough rows to see concentration by city, type, or band; use maps and BI off the JSON/CSV instead of the map UI alone.
- **Research and analytics** — feed stable, repeatable pulls into reports, models, or dashboards. `maxItems` controls cost and row count per run.
- **Repeatable searches** — save the `startUrl` and schedule runs (Apify or your stack) to track new listings, inventory shifts, or updated comps over time.

### 🤑 Cost of usage

**Cost is $1 per 1,000** listings, no hidden fees!

| Listings | Approximate cost |
| -------: | ----------------: |
| 100 | ~$0.10 |
| 1,000 | ~$1.00 |
| 10,000 | ~$10.00 |

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).


### 🛠️ Input

| Field | Type | Description | Example |
| ----- | ---- | ----------- | ------- |
| `startUrl` | `string` | Propwire search URL with `?filters=…` | From the address bar after you set the search |
| `maxItems` | `number` | Max listings to collect (cap **10,000** per run) | `100` |

### 🧐 Output

The **dataset** has one object per listing, **flattened** for export.
Example:
```json
{
"days_on_market": null,
"listing_key": null,
"id": 179608774,
"address_address": "508 Main St # 512",
"address_city": "Johnstown",
"address_state": "PA",
"address_zip": "15901",
"auction_date": null,
"auction_time": null,
"bedrooms": 0,
"bathrooms": 0,
"basement_details_basement_finished_percentage": 0,
"basement_details_basement_sf": 0,
"basement_details_basement_sf_finished": null,
"basement_details_basement_sf_unfinished": null,
"basement_details_basement_type": "NO BASEMENT",
"building_area_sf": 0,
"company_owned": true,
"cooling_type": "Unknown",
"estimated_equity": 60600,
"estimated_equity_percentage": 100,
"estimated_value": 60600,
"estimated_ltv": null,
"estimated_price_per_sf": null,
"estimated_zip_price_per_sf": null,
"fireplace": null,
"fireplace_type": "Unknown",
"fireplace_count": 0,
"foreclosure": null,
"garage_details_garage_area_sf": 0,
"garage_details_garage_area_sf_finished": null,
"garage_details_garage_area_sf_unfinished": null,
"garage_details_garage_type": "Unknown",
"geo_location_latitude": "40.324823",
"geo_location_longitude": "-78.917665",
"government_owned": null,
"heating_type": "None",
"heating_fuel": "Unknown",
"individual_owned": false,
"investor_owned": null,
"last_sold_date": "2025-09-10",
"last_sold_price": 60000,
"lead_type_absentee_owner": true,
"lead_type_adjustable_loan": null,
"lead_type_assumable_loan": null,
"lead_type_auction": null,
"lead_type_bank_owned": false,
"lead_type_cash_buyer": true,
"lead_type_empty_nester": false,
"lead_type_flipped_property": false,
"lead_type_free_and_clear": true,
"lead_type_high_equity": true,
"lead_type_low_equity": false,
"lead_type_negative_equity": false,
"lead_type_intrafamily_transfer": false,
"lead_type_mls_active": false,
"lead_type_mls_pending": false,
"lead_type_mls_failed": false,
"lead_type_mls_sold": false,
"lead_type_out_of_state_owner": null,
"lead_type_preforeclosure": null,
"lead_type_preprobate": false,
"lead_type_private_lender": false,
"lead_type_tired_landlord": false,
"lead_type_vacant_home": false,
"lead_type_vacant_lot": false,
"lead_type_zombie_property": false,
"lead_type_code_violation": false,
"lead_type_lien_tax": false,
"lead_type_lien_misc": false,
"lead_type_divorce": false,
"lead_type_bankruptcy": false,
"lead_type_abandoned_homes": false,
"lead_type_tax_dodgers": false,
"lead_type_ultra_liens": false,
"lead_type_ultra_violations": false,
"lead_type_bargain_properties": false,
"lead_type_desperate_landlords": false,
"lead_type_cash_flow_rentals": false,
"lead_type_creative_financing": false,
"lead_type_hidden_gems_mls": false,
"lead_type_sub_to_mls": false,
"lead_type_sub_to_off_market": false,
"living_area_sf": null,
"lot_size_acres": "0.0918274",
"lot_size_sf": 4000,
"mls_attom_last_status": null,
"mls_attom_last_status_date": null,
"mls_attom_price": null,
"mls_attom_price_per_sf": null,
"mls_first_photo_url": null,
"mls_list_date": null,
"mls_list_price": null,
"mls_list_price_per_sf": null,
"mls_sold_date": null,
"mls_sold_price": null,
"mls_sold_price_per_sf": null,
"owner_name_0": "508 512 MAIN ST LLC",
"owner_mailing_address_owners_mailing_address": "111 WALNUT ST",
"owner_mailing_address_owners_mailing_city": "JOHNSTOWN",
"owner_mailing_address_owners_mailing_state": "PA",
"owner_mailing_address_owners_mailing_zip": "15901",
"owner_mailing_address_owners_mailing_zip4": "1653",
"owner_mailing_address_owners_mail_privacy": null,
"owner_occupied": false,
"months_of_ownership": 8,
"years_of_ownership": 1,
"pool": "Unknown",
"pool_area_sf": 0,
"pool_type": "Unknown",
"property_type": "COMMERCIAL",
"tax_assessed_values_year_assessed": 2025,
"tax_assessed_values_total": 23640,
"tax_assessed_values_improvements": 9460,
"tax_assessed_values_land": 14180,
"tax_assessed_values_improvements_percentage": 40,
"tax_assessed_values_previous_total": 23640,
"trust_owned": null,
"units": 0,
"year_built": null,
"listhub": null
}
````

### ⬆️ More than 10,000 rows or missing fields?

Runs are capped at **10,000** listings. For a higher cap or missing fields you need in the output, open an **issue** on the repo (if it’s public) or use the **Apify actor** page to contact the developer.

### 🔍 Looking for something else?

[Thousands of prebuilt tools, scrapers, automations, and more on the Apify Store](https://apify.com/store?fpr=cbgdsf)

### ⚠️ Disclaimer

This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Propwire. All trademarks mentioned are the property of their respective owners. Use the data in line with Propwire’s terms and applicable law.

#### 📞 Contact Me

**Need a custom solution? Have a feature request or just want to chat?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

### 🔎 SEO keywords

propwire scraper, propwire search, propwire.com, scrape propwire, propwire property data, propwire deals, propwire real estate leads, propwire lead list, propwire lead generation, propwire US properties, propwire off market, propwire investor data, propwire dataset export, propwire CSV, propwire JSON, Apify propwire actor, propwire listings scraper, propwire bulk export, propwire search API, propwire automation

# Actor input Schema

## `startUrl` (type: `string`):

Full Propwire search URL including `filters`

## `maxItems` (type: `integer`):

Max listings to push to the dataset (PPE, capped at 10,000).

## Actor input object example

```json
{
  "startUrl": "https://propwire.com/search?filters=%7B%22locations%22%3A%5B%7B%22searchType%22%3A%22C%22%2C%22city%22%3A%22Chicago%20Heights%22%2C%22state%22%3A%22IL%22%2C%22title%22%3A%22Chicago%20Heights%2C%20IL%22%7D%5D%2C%22property_type%22%3A%5B%22mfh_2_to_4%22%5D%7D",
  "maxItems": 1000
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
    "startUrl": "https://propwire.com/search?filters=%7B%22locations%22%3A%5B%7B%22searchType%22%3A%22C%22%2C%22city%22%3A%22Chicago%20Heights%22%2C%22state%22%3A%22IL%22%2C%22title%22%3A%22Chicago%20Heights%2C%20IL%22%7D%5D%2C%22property_type%22%3A%5B%22mfh_2_to_4%22%5D%7D",
    "maxItems": 1000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/propwire-com-scraper-pro-by-search-url").call(input);

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
    "startUrl": "https://propwire.com/search?filters=%7B%22locations%22%3A%5B%7B%22searchType%22%3A%22C%22%2C%22city%22%3A%22Chicago%20Heights%22%2C%22state%22%3A%22IL%22%2C%22title%22%3A%22Chicago%20Heights%2C%20IL%22%7D%5D%2C%22property_type%22%3A%5B%22mfh_2_to_4%22%5D%7D",
    "maxItems": 1000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/propwire-com-scraper-pro-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://propwire.com/search?filters=%7B%22locations%22%3A%5B%7B%22searchType%22%3A%22C%22%2C%22city%22%3A%22Chicago%20Heights%22%2C%22state%22%3A%22IL%22%2C%22title%22%3A%22Chicago%20Heights%2C%20IL%22%7D%5D%2C%22property_type%22%3A%5B%22mfh_2_to_4%22%5D%7D",
  "maxItems": 1000
}' |
apify call azzouzana/propwire-com-scraper-pro-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/propwire-com-scraper-pro-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
