# 🚀 Flatfox.ch Property Listings Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Flatfox.ch Property Listings Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/flatfox-search-pages-scraper?fpr=cbgdsf)

---

## Flatfox.ch Property Listings Scraper (By Search URL)

### 🤩 Features

🚀 Our **blazing-fast, non-official Flatfox.ch search scraper** 🏠 lets you extract real estate public information from `https://flatfox.ch/` and export them in various formats (JSON, CSV, HTML, API etc.).  
🔥 Simply provide your search URL (optionally with filters applied), and you're all set!
👉 It allows you to extract rich listings' information, including the price, images, location, description, attributes, and much more.  

### 📚 How to use this actor

1. 👉 [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required!
2. 🎉 Just click the **"Get Started"** button and complete a quick signup.
3. 💰 A free account includes enough credits to test this actor.
4. ⏳ Enjoy scraping for the free trial period, no commitment or upfront payment required.

The scraper has a required `startUrl` parameter which is a URL to a search page with filters applied.
- Examples of valid URLs:
  - `https://flatfox.ch/en/search/?east=10.816612&max_price=1250&min_rooms=5&north=48.698673&south=44.878282&take=48&west=5.631808`
  - `https://flatfox.ch/de/search/?east=10.816612&max_price=1250&min_price=750&min_rooms=4&north=48.698673&south=44.878282&take=48&west=5.631808`

### 🤔 Why scrape flatfox.ch?

Flatfox.ch is a popular real estate platform in Switzerland, offering a wide range of property listings for rent and sale. However, it does not provide an official API for accessing its data. This scraper allows users to extract valuable information from Flatfox.ch, enabling them to:

- **Gather data for market analysis**
- **Automate property searches** based on specific criteria
- **Integrate Flatfox.ch data** into their own applications or services
- **Save time and effort** by automating the data extraction process

### 🤑 Cost of usage

The average cost of using this scraper is **$1 per 1000 ads scraped**, no hidden fees.

#### 💰 Cost Example

**Regular Mode:**
- You scrape **500 listings**.
- Cost: `(1.00 / 1,000) * 500 = $0.5`

### 🛠️ Input

| Field | Type | Description | Default value / Example |
| ----- | ---- | ----------- |-------------------------|
| `startUrl` | `URL` | the search page's result link | `https://flatfox.ch/en/search/?...` |
| `maxItems` | `integer` | Maximum number of items to scrape | `5000` (or limited by budget) |


###  Output Structure
The output is simplified for ease of use:
```json
{
  "agency": {
    "name": "Euro Estates GmbH",
    "name_2": null,
    "street": "Räffelstrasse 10",
    "zipcode": "8045",
    "city": "Zürich",
    "country": "CH",
    "logo": "https://flatfox.ch/thumb/org/2025/05/7cexyh2gdfj5dl3pjbrb277rfz7i52as4elqlbzglvacxhzznf.jpg?signature=YrJQHqPLREZT8w13fN38PRNloMW1IRwhiBG87wMOwTU"
  },
  "alternative_reference": null,
  "balconygarden": true,
  "city": "La Chaux-de-Fonds",
  "country": "CH",
  "cover_image": "https://flatfox.ch/thumb/ff/2025/09/dh268828sy6m6cowgrquv40s7krdzhbi6n51nudgs275v25cy9.jpg?signature=INymnVdlMWlyKSyT8R7AMuSrOu9GNoQb5U-fNdquvQE",
  "created": "2025-09-08T17:03:16.402550+02:00",
  "description": "Ce bel appartement est disposé de la manière suivante :   \n\\- Bel espace salon-salle à manger avec grand balcon   \n\\- Cuisine habitable moderne avec tout confort et beaucoup de rangements   \n\\- Deuxième balcon de la cuisine avec vue sur la verdure   \n\\- 3 chambres de nuit avec parquet et armoires encastrées   \n\\- Salle de bain/WC   \n  \nPour compléter l'ensemble.   \n\\- Divers commerces et commodités se situent à proximité   \n\\- Verdure et terrain de jeux pour les enfants   \n\\- Buanderie commune   \n\\- Local à vélos   \n\\- Une cave   \n  \nLoyer 990.- + 250 charges   \n  \nA visiter sans tarder !   \nContact :   \nLevana Fink - l.fink@euro-estates.ch / 043 960 79 82",
  "description_title": "B a l c o n , C e n t r a l - et -  S u p e r  L o y e r !",
  "documents": [],
  "extracted_emails": [
    "l.fink@euro-estates.ch"
  ],
  "flatfox_priority_exclusive_until": null,
  "floor": 3,
  "garage": true,
  "images": [
    "https://flatfox.ch/thumb/ff/2025/09/dh268828sy6m6cowgrquv40s7krdzhbi6n51nudgs275v25cy9.jpg?signature=INymnVdlMWlyKSyT8R7AMuSrOu9GNoQb5U-fNdquvQE",
    "https://flatfox.ch/thumb/ff/2025/09/8dfw3taktp4fa5sjf1lzeq86iekrqp5ljs93uzjibcr3k8s72q.jpg?signature=6TqLPGzzUVKcFZCNwUtursK693JBOwYFn7wSUX__cQM",
    "https://flatfox.ch/thumb/ff/2025/09/qgv6iuetpwxbyhy5i00fwczuad6sj7sda72o1onb6sdkw01m7o.jpg?signature=xV7VyrRH6h1mRzm6oWKL82I-IyCCK4UVpi1lydv3ez8",
    "https://flatfox.ch/thumb/ff/2025/09/63zbx5039etynkeml3yx2hkxsk6l1uhy4zc4f5rnfsx25l3kcr.jpg?signature=HH1nBOu_hd2eStPJu4cRZSH2lNc-2SDgZo_GGuXnlH0",
    "https://flatfox.ch/thumb/ff/2025/09/8cq8qjdlvr35hdj59nunlwjnqwnad6ncvngnzdbmnqcsja6pj2.jpg?signature=B5ijb8-rNSS7474T4I4ol_9HRd7O04uQii0nJuMcBSA",
    "https://flatfox.ch/thumb/ff/2025/09/obfe6himrmlue3umgil6xftr0d27idbuszfxm60wwm3nsd2b87.jpg?signature=4B_e-3LxzrLs4oyTBaWVonqMHXPAz2WCNncvrc5jep0",
    "https://flatfox.ch/thumb/ff/2025/09/jurbsjnznwwaqltwv49usxlwyj4elrxoremogl7hi73f83cepc.jpg?signature=1FUAmI-xqLdqKyo2ywu1xbhhgDyOtLevPlqllX0dmUg",
    "https://flatfox.ch/thumb/ff/2025/09/diqmlb0k9yb00ha7fgqhspc7px9yvn7aaxwbfry35996ijh7oz.jpg?signature=W1pKD9xzDx_kOb6zthAn12qBtpRmlbFoFxQB2v_FaS8",
    "https://flatfox.ch/thumb/ff/2025/09/h58i9bifecr4o0r77b8p201vn571tlfdl338c992fkau1o7i7n.jpg?signature=gkXOkBnSugKgXv8gqyceo5DCAf9UJ5Rs2o_hD0qnVq8",
    "https://flatfox.ch/thumb/ff/2025/09/2amd33ej8fbt5l03b4v6r37bpxsy0p79mu7b0errvzbp1o5xdc.jpg?signature=t4J_hyrAR9Dt5S6ni8MEFDL41zffQqlqjzMBE5m4O0k"
  ],
  "is_disliked": false,
  "is_furnished": false,
  "is_liked": false,
  "is_selling_furniture": false,
  "is_subscribed": false,
  "is_swap": false,
  "is_temporary": false,
  "latitude": 47.11767829999999,
  "live_viewing_url": null,
  "livingspace": 76,
  "longitude": 6.8405667,
  "moving_date": null,
  "moving_date_type": "imm",
  "number_of_rooms": "4.0",
  "object_category": "APARTMENT",
  "object_type": "APARTMENT",
  "offer_type": "RENT",
  "parkingspace": true,
  "petsallowed": true,
  "pitch_title": "Rent a 4 rooms apartment in La Chaux-de-Fonds",
  "pk": 85287880,
  "price_display": 990,
  "price_display_type": "TOTAL",
  "price_unit": "monthly",
  "public_address": "Arc-en-Ciel 30, 2300 La Chaux-de-Fonds",
  "public_title": "Arc-en-Ciel 30, 2300 La Chaux-de-Fonds - CHF 990",
  "published": "2025-09-08T17:03:16.486220+02:00",
  "ref_house": "10309",
  "ref_object": "1531",
  "ref_property": "10309",
  "reference": "10309.10309.1531",
  "rent_charges": 0,
  "rent_gross": 990,
  "rent_net": 990,
  "rent_title": "Rent a 4 rooms apartment in La Chaux-de-Fonds",
  "reserved": false,
  "short_title": "4 rooms apartment",
  "short_url": "https://flatfox.ch/85287880/",
  "slug": "arc-en-ciel-30-2300-la-chaux-de-fonds",
  "smg_id": "4002505252",
  "space_display": 76,
  "state": "NE",
  "status": "act",
  "street": "Arc-en-Ciel 30",
  "submit_url": "https://flatfox.ch/en/listing/85287880/submit/",
  "surface_living": 76,
  "surface_property": null,
  "surface_usable": null,
  "surface_usable_minimum": null,
  "tour_url": null,
  "url": "https://flatfox.ch/en/flat/arc-en-ciel-30-2300-la-chaux-de-fonds/85287880/",
  "video_url": null,
  "view": true,
  "volume": null,
  "website_url": null,
  "year_built": null,
  "year_renovated": null,
  "zipcode": 2300
}
````

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

### ⚠️ Disclaimer

This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Flatfox AG or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

***

**Need a custom solution? Have a feature request or just want to chat?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

# Actor input Schema

## `startUrl` (type: `string`):

Search results page URL

## `maxItems` (type: `integer`):

Maximum number of items to scrape.

## Actor input object example

```json
{
  "startUrl": "https://flatfox.ch/en/search/?east=10.492340&max_price=750&min_rooms=4&north=48.467679&south=45.125183&take=96&west=5.956080",
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
    "startUrl": "https://flatfox.ch/en/search/?east=10.492340&max_price=750&min_rooms=4&north=48.467679&south=45.125183&take=96&west=5.956080",
    "maxItems": 2000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/flatfox-search-pages-scraper").call(input);

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
    "startUrl": "https://flatfox.ch/en/search/?east=10.492340&max_price=750&min_rooms=4&north=48.467679&south=45.125183&take=96&west=5.956080",
    "maxItems": 2000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/flatfox-search-pages-scraper").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://flatfox.ch/en/search/?east=10.492340&max_price=750&min_rooms=4&north=48.467679&south=45.125183&take=96&west=5.956080",
  "maxItems": 2000
}' |
apify call azzouzana/flatfox-search-pages-scraper --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/flatfox-search-pages-scraper",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
