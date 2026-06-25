# 🚀 Autoscout24 vehicle Scraper — All domains (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Autoscout24 vehicle Scraper — All domains (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/autoscout24-scraper-pro-1-1k-by-search-url?fpr=cbgdsf)

---

## Autoscout24 vehicle Scraper — All domains (By Search URL)

Automatically extract vehicle listings from **[Autoscout24](https://www.autoscout24.com)**. This actor allows you to scrape search results pages, monitor price changes, and detect sold/new listings with enterprise-grade reliability.

### 🌟 Key Features
- **🏎️ Blazing fast (Faster than Ferrari)**
- **🌎 Multi-Domain Support**: Works for all major Autoscout24 domains based on the search URL provided:
    -   `.com` (Europe/Global)
    -   `.de` (Germany)
    -   `.it` (Italy)
    -   `.es` (Spain)
    -   `.fr` (France)
    -   `.be` (Belgium)
    -   `.nl` (Netherlands)
    -   `.at` (Austria)
    -   `.lu` (Luxembourg)
    -   `.ch` (Switzerland)
- **📊 Rich, Flattened Data**: Structured, easy to import data to your CRM, automation and/or AI/LLMs workflows (no nested JSON hell).

### 🚀 How It Works

1.  **🔎 Enter Search URL**: Perform a search on Autoscout24 (.com, .de, etc.) and copy the URL.

    *   **Examples**:
        *   **🇩🇪 Germany (.de)**:
            ```text
            https://www.autoscout24.de/lst/bmw/320?sort=standard&desc=0&ustate=N%2CU&cy=D&atype=C
            ```
        *   **🇮🇹 Italy (.it)**:
            ```text
            https://www.autoscout24.it/lst/fiat/500?sort=standard&desc=0&ustate=N%2CU&cy=I&atype=C
            ```
        *   **🇳🇱 Netherlands (.nl)**:
            ```text
            https://www.autoscout24.nl/lst/volkswagen/golf?sort=standard&desc=0&ustate=N%2CU&cy=NL&atype=C
            ```
        *   **🇪🇸 Spain (.es)**:
            ```text
            https://www.autoscout24.es/lst/seat/ibiza?sort=standard&desc=0&ustate=N%2CU&cy=E&atype=C
            ```
        *   **🇫🇷 France (.fr)**:
            ```text
            https://www.autoscout24.fr/lst/peugeot/208?sort=standard&desc=0&ustate=N%2CU&cy=F&atype=C
            ```
        *   **🇨🇭 Switzerland (.ch)**:
            ```text
            https://www.autoscout24.ch/en/s?priceTo=45000
            ```

2.  **⚙️ Configure**: Set your maximums items.
3.  **🏃 Run**: Click run, and get **fresh, structured data**.

### ⚠️ Limitations
-   **🆓 Free Users**: Limited to up to **5 items per run** and **5 runs per day** with a **30-minute cooldown** between runs. Upgrade to the paid plan to lift the limitation.

### 🛠️ Input Parameters

| Parameter | Type | Default Value | Description |
| :--- | :--- | :--- | :--- |
| `searchUrl` | String | - | **Required**. The URL of the search results (e.g. autoscout24.de, .com, .it, .ch). |
| `maxItems` | Integer | `100` | Maximum number of items to scrape. |

### 💰 Pricing

This actor costs $1.00 per 1,000 results ($0.001 per item), no hidden fees!

#### Example

**Scrape (1,500 items)**  
1,500 × $0.001 = **$1.50**

### 📦 Data Output

Flattened JSON structure tailored for easy analysis.

```json
{
	"adTier": "T40",
	"appliedAdTier": "T40",
	"availableNow": true,
	"coverImageAttractiveness": 0.15,
	"id": "12345678-abcd-1234-abcd-1234567890ab",
	"identifier_crossReferenceId": null,
	"identifier_legacyId": null,
	"images": ["..."],
	"isListingBoost": false,
	"isOcs": false,
	"location_city": "Berlin",
	"location_countryCode": "DE",
	"location_street": "Example Street 123",
	"location_zip": "10115",
	"ocsImagesA": ["..."],
	"price_amount": 15990,
	"price_isVatLabelLegallyRequired": false,
	"price_priceFormatted": "€ 15,990",
	"ratings_ratingsCount": 658,
	"ratings_ratingsEnabled": true,
	"ratings_ratingsStars": 4.5,
	"scrapedAt": "2026-02-01T12:00:00Z",
	"searchResultSection": "Main",
	"searchResultType": "Organic",
	"seller_companyName": "Auto Dealer GmbH",
	"seller_contactName": "Sales Team",
	"seller_dealer_isFreespeeCallTrackingEnabled": true,
	"seller_dealer_maxImages": 30,
	"seller_id": "12345678",
	"seller_links_imprint": "https://www.autoscout24.com/dealer/example/imprint",
	"seller_links_infoPage": "https://www.autoscout24.com/lst?atype=C&cid=12345678",
	"seller_logo_small_href": "https://prod.pictures.autoscout24.net/dealer-info/sample-logo.jpg",
	"seller_phones_office": "+493012345678",
	"seller_type": "Dealer",
	"specialConditions": ["..."],
	"statistics_leadsRange": "Some",
	"superDeal_isEligible": false,
	"superDeal_oldPriceFormatted": "",
	"tracking_firstRegistration": "05-2019",
	"tracking_fuelType": "d",
	"tracking_imageContent": "no-placeholder|0.15",
	"tracking_isSmyleEligible": "false",
	"tracking_mileage": "45000",
	"tracking_modelTaxonomy": "[make_id:37, model_group_id:200705, variant_id:, generation_id:1931, motortype_id:, trim_id:];",
	"tracking_orderBucket": "0",
	"tracking_price": "15990",
	"tracking_priceLabel": "fair-price",
	"url": "https://www.autoscout24.com/offers/sample-car-url-12345678-abcd-1234-abcd-1234567890ab",
	"vehicleDetails_firstRegistration": "05/2019",
	"vehicleDetails_fuelType": "Diesel",
	"vehicleDetails_gear": "Automatic",
	"vehicleDetails_mileage": "45,000 km",
	"vehicleDetails_power": "110 kW (150 hp)",
	"vehicle_articleType": "Car",
	"vehicle_fuel": "Diesel",
	"vehicle_make": "Volkswagen",
	"vehicle_mileageInKm": "45,000 km",
	"vehicle_model": "Golf",
	"vehicle_modelGroup": "Golf",
	"vehicle_modelId": 2084,
	"vehicle_modelVersionInput": "2.0 TDI Highline",
	"vehicle_offerType": "U",
	"vehicle_subtitle": null,
	"vehicle_transmission": "Automatic",
	"vehicle_type": "Car",
	"vehicle_variant": null,
	"wltpValues": ["..."]
}
````

#### Switzerland (.ch) example (.ch domain belong to a different underlying company, hence the different data structure)

```json
{
	"availability": "InStock",
	"badges": ["Inspected", "Warranty", "No accident vehicle"],
	"brand": "BMW",
	"city": "Volketswil",
	"consumption": null,
	"dealer": "Auto Salon Volketswil AG",
	"dealerType": "AutoDealer",
	"description": "Werksgarantie* Head Up Display* 360° Kamera* Abstandsregler* Parking Assistant Plus*",
	"financingUrl": "https://kredit.financescout24.ch/de/inquiry/amount?vehicleId=20553024&amount=41980.00",
	"firstRegistration": "11/2024",
	"fuel": "Diesel",
	"id": "20553024",
	"imageAlt": "BMW 320d xDrive 48V Steptronic M Sport *360° Kamera*Abstandsregler*Parking Assistant Plus*",
	"imageUrl": "https://listing-images.autoscout24.ch/listing/24/20553024/1298217632.png?w=1920&q=90",
	"imageUrls": [
		"https://listing-images.autoscout24.ch/listing/24/20553024/1298217632.png",
		"https://listing-images.autoscout24.ch/listing/24/20553024/875038105.jpg"
	],
	"insuranceUrl": "https://www.financescout24.ch/de/lp/autoversicherung-finden?vehicleId=20553024",
	"isTop": true,
	"listingId": "20553024",
	"location": "8604 Volketswil",
	"mileage": 29000,
	"mileageFormatted": "29'000 km",
	"model": "320",
	"monthlyPayment": "Ab 647.- pro Monat ohne Anzahlung",
	"postalCode": "8604",
	"power": 190,
	"powerFormatted": "190 PS (140 kW)",
	"powerKw": 140,
	"powerUnit": "PS",
	"price": 41980,
	"priceFormatted": "CHF 41'980.–",
	"priceValidUntil": "2027-06-16",
	"price_amount": 41980,
	"priceCurrency": "CHF",
	"schemaDescription": "BMW 320d xDrive 48V Steptronic M Sport *360° Kamera*Abstandsregler*Parking Assistant Plus*, Diesel, Automatic, 190 PS, 29'000 km",
	"scrapedAt": "2026-06-16T12:00:00.000Z",
	"sellerId": "2606197",
	"sellerUrl": "https://www.autoscout24.ch/en/s/seller-2606197",
	"slug": "bmw-320d-xdrive-48v-steptronic-m-sport-360-kamera-abstandsregler-parking-assistant-plus",
	"title": "BMW 320d xDrive 48V Steptronic M Sport *360° Kamera*Abstandsregler*Parking Assistant Plus*",
	"transmission": "Automatic",
	"url": "https://www.autoscout24.ch/en/d/bmw-320d-xdrive-48v-steptronic-m-sport-360-kamera-abstandsregler-parking-assistant-plus-20553024"
}
```

### 🔍 SEO Keywords

autoscout24 scraper, autoscout24 api, european car market data, vehicle data extraction, autoscout24 python, apify autoscout24.

***

**Need a custom solution? Have a feature request or just want to chat?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

# Actor input Schema

## `searchUrl` (type: `string`):

The URL of the search results page on Autoscout24.

## `maxItems` (type: `integer`):

Maximum number of items to scrape.

## Actor input object example

```json
{
  "searchUrl": "https://www.autoscout24.it/lst-moto?sort=standard&desc=0&ustate=N%2CU&atype=B&cy=I&priceto=17500&damaged_listing=exclude&source=homepage_search-mask",
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
    "searchUrl": "https://www.autoscout24.it/lst-moto?sort=standard&desc=0&ustate=N%2CU&atype=B&cy=I&priceto=17500&damaged_listing=exclude&source=homepage_search-mask",
    "maxItems": 1000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/autoscout24-scraper-pro-1-1k-by-search-url").call(input);

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
    "searchUrl": "https://www.autoscout24.it/lst-moto?sort=standard&desc=0&ustate=N%2CU&atype=B&cy=I&priceto=17500&damaged_listing=exclude&source=homepage_search-mask",
    "maxItems": 1000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/autoscout24-scraper-pro-1-1k-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "searchUrl": "https://www.autoscout24.it/lst-moto?sort=standard&desc=0&ustate=N%2CU&atype=B&cy=I&priceto=17500&damaged_listing=exclude&source=homepage_search-mask",
  "maxItems": 1000
}' |
apify call azzouzana/autoscout24-scraper-pro-1-1k-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/autoscout24-scraper-pro-1-1k-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
