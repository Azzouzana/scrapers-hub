# 🚀 Mobile.de Scraper — Cars, Motorbikes, Trucks & Boats (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Mobile.de Scraper — Cars, Motorbikes, Trucks & Boats (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/mobile-de-scraper-pro-by-search-URL?fpr=cbgdsf)

---

## Mobile.de Scraper — Cars, Motorbikes, Trucks & Boats (By Search URL)

[Deutsche Version](#deutsche-version) | [English Version](#english-version)

---

### Deutsche Version

[Deutsche Version](#deutsche-version) | [English Version](#english-version)

Extrahieren Sie automatisch Fahrzeuginserate von **[Mobile.de](https://www.mobile.de)**, Deutschlands größtem Fahrzeugmarkt. Dieser Actor scrapt Suchergebnisseiten (Autos, Motorräder, LKWs, Boote usw.) und liefert strukturierte Daten.

#### 🌟 Hauptfunktionen
- **🏎️ Unglaublich schnell (Schneller als ein Ferrari)**
- **Zuverlässigkeit auf Enterprise-Niveau**: Wir machen das beruflich – Sie können sich auf uns verlassen.
- **📊 Strukturierte, flache Daten** einfach zu importierende Daten (kein kompliziertes verschachteltes JSON).
- **🌍 Mehrsprachige URLs**: Englisch (en), Deutsch (de), Spanisch (es), Französisch (fr), Polnisch (pl), Russisch (ru), Türkisch (tr), Niederländisch (nl), Tschechisch (cz), Rumänisch (ro).
#### 🚀 Wie es funktioniert

1.  **🔎 Such-URL eingeben**: Führen Sie eine Suche auf [Mobile.de](https://www.mobile.de) durch und kopieren Sie die URL. Hier sind einige Beispiele:
    *   **🛵 Blaue Motorräder mit ABS, max. 5000 km**:
        ```text
        https://suchen.mobile.de/fahrzeuge/search.html?ecol=BLUE&fe=ABS&isSearchRequest=true&ml=%3A5000&od=up&s=Motorbike&sb=rel&vc=Motorbike
        ```
    *   **🚗 VW Golf ab 2020**:
        ```text
        https://suchen.mobile.de/fahrzeuge/search.html?isSearchRequest=true&ms=25200%3B14%3B%3B&fr=2020%3A&sb=rel&vc=Car
        ```

2.  **⚙️ Konfigurieren**: Legen Sie die maximale Anzahl an Elementen fest.
3.  **🏃 Ausführen**: Klicken Sie auf "Run". Der Actor durchsucht Mobile.de und liefert Ihnen **frische, strukturierte Daten bereit zur Analyse**.

#### 💰 Kostenschätzung

Die Preisgestaltung ist einfach und transparent:
-   **🕷️ Scraping-Kosten**: 1,00 $ pro 1.000 Artikel.

| Szenario | Artikel | Geschätzte Kosten |
| :--- | :--- | :--- |
| **⚡ Schneller Check** | 100 | **0,10 $** |
| **🏎️ Standard-Lauf** | 1.000 | **1,00 $** |
| **🏭 Großer Lauf** | 3.000 | **3,00 $** |

#### ⚠️ Einschränkungen

-   **🆓 Kostenlose Nutzer**: Begrenzt auf bis zu **5 Artikel pro Lauf** und **5 Läufe pro Tag** mit einer **30-minütigen Wartezeit** zwischen den Läufen. Upgrade auf den kostenpflichtigen Plan, um die Begrenzung aufzuheben.

#### 🛠️ Eingabeparameter

| Parameter | Typ | Standardwert | Beschreibung |
| :--- | :--- | :--- | :--- |
| `searchUrl` | String | - | **Erforderlich**. Die URL der Suchergebnisse von Mobile.de. |
| `maxItems` | Integer | `100` | Maximale Anzahl der zu scrapenden Artikel. |

##### 💡 Beispiel-Eingabe
```json
{
    "searchUrl": "https://suchen.mobile.de/fahrzeuge/search.html?isSearchRequest=true&s=Car&vc=Car",
    "maxItems": 50
}
````

#### 📦 Datenausgabe

Der Actor speichert die Ergebnisse in einem Dataset. Jedes Element ist flach und einfach zu analysieren:

```json
{
    "attr_c": "Limousine",
    "attr_cc": "1,997 ccm",
    "attr_cn": "DE",
    "attr_door": "4/5",
    "attr_ecol": "Blue",
    "attr_emc": "Euro6",
    "attr_fr": "10/2013",
    "attr_ft": "Petrol",
    "attr_gi": "New",
    "attr_loc": "Magdeburg",
    "attr_ml": "72,273 km",
    "attr_pvo": "2",
    "attr_pw": "180 kW (245 hp)",
    "attr_sc": "5",
    "attr_tr": "Automatic",
    "attr_z": "39112",
    "category": "Saloon",
    "created": 1745930164,
    "created_human": "2025-04-29 12:36:04",
    "customDimensions": {
      "10": "platinum"
    },
    "hasDamage": false,
    "id": 423885827,
    "images": ["..."],
    "isEyeCatcher": false,
    "isVideoEnabled": false,
    "kba_hsn": "0005",
    "kba_tsn": "BOJ",
    "mainImage": "https://img.classistatic.de/api/v1/mo-prod/images/7d/7d34d3d6-b15f-4e5d-9d5b-ec4edf7f29e1?rule=mo-360w",
    "make": "BMW",
    "makeId": 3500,
    "model": "328 Gran Turismo",
    "modelId": 77,
    "modified": 1768932117,
    "modified_human": "2026-01-20 18:01:57",
    "numImages": 33,
    "price": "€20,950",
    "priceRating_label": "No rating",
    "priceRating_rating": "NO_RATING",
    "price_amount": 20950,
    "price_currency": "EUR",
    "readyToDrive": true,
    "renewed": 1768932109,
    "renewed_human": "2026-01-20 18:01:49",
    "scrapedAt": "2026-01-24T17:46:20.871Z",
    "scrapedAt_human": "2026-01-24 17:46:20",
    "segment": "Car",
    "sellerId": 14232991,
    "seller_address": "Blankenburgerstr. 56",
    "seller_country": "DE",
    "seller_lat": 52.1041018,
    "seller_lon": 11.6004269,
    "seller_messenger_number": "+49 (0)172 5434298",
    "seller_messenger_type": "WHATS_APP",
    "seller_messenger_uri": "https://wa.me/491725434298",
    "seller_name": "Auto Zentrum Magdeburg",
    "seller_phone": "+49 (0)391 81069505",
    "seller_phone_uri": "tel:+4939181069505",
    "seller_type": "Dealer",
    "shortTitle": "BMW 328 Gran Turismo",
    "siteId": "GERMANY",
    "st": "Dealer",
    "subTitle": "328iA Gran Turismo *NAVI PROF*HUD*AHK*KAMERA*SH*",
    "title": "BMW 328iA Gran Turismo *NAVI PROF*HUD*AHK*KAMERA*SH*",
    "url": "https://suchen.mobile.de/auto-inserat/bmw-328ia-gran-turismo-navi-prof-hud-ahk-kamera-sh-magdeburg/423885827.html",
    "vc": "Car",
    "version": 105
  }
```

#### 🔍 SEO Keywords

mobile.de scraper, mobile.de api, deutschland auto scraper, auto marktdaten, kfz daten extraktion, fahrzeugdaten api, autohändler inventar scraper, mobile.de python, apify mobile.de, auto inserate daten.

***

**Benötigen Sie eine individuelle Lösung? Haben Sie einen Funktionswunsch oder wollen Sie einfach nur chatten?**\
Wir würden uns freuen, von Ihnen zu hören!

- 💬 **Discord**: `@azzouzana`
- 📧 **E-Mail**: <labs@azzouzana.com>

***

***

### English Version

[Deutsche Version](#deutsche-version) | [English Version](#english-version)

Automatically extract vehicle listings from **[Mobile.de](https://www.mobile.de)**, Germany's largest vehicle marketplace. This actor scrapes search results pages (cars, motos, bikes, boats, etc.) and returns structured data.

#### 🌟 Key Features

- **🏎️ Blazing fast, (Faster than Ferrari)**
- **Enterprise-grade reliability**  We do this for a living, you can rely on us
- **📊 Rich, Flattened Data** easy to import data (no ugly nested JSON)
- **🌍 Multi-language URLs**: English (en), German (de), Spanish (es), French (fr), Polish (pl), Russian (ru), Turkish (tr), Dutch (nl), Czech (cz), Romanian (ro).

#### 🚀 How It Works

1. **🔎 Enter Search URL**: Perform a search on [Mobile.de](https://www.mobile.de) and copy the URL. Here are some examples:
   - **🛵 Blue Motorbikes with ABS, max 5000km**:
     ```text
     https://suchen.mobile.de/fahrzeuge/search.html?ecol=BLUE&fe=ABS&isSearchRequest=true&ml=%3A5000&od=up&s=Motorbike&sb=rel&vc=Motorbike
     ```
   - **🚗 VW Golf from 2020**:
     ```text
     https://suchen.mobile.de/fahrzeuge/search.html?isSearchRequest=true&ms=25200%3B14%3B%3B&fr=2020%3A&sb=rel&vc=Car
     ```

2. **⚙️ Configure**: Set your maximum items.

3. **🏃 Run**: Click run, the actor sneaks into mobile.de warehouse and gets back to you with **fresh, structured data ready for analysis**.

#### 💰 Cost Estimation

Pricing is simple and transparent:

- **🕷️ Scraping Cost**: $1.00 per 1,000 items.

| Scenario | Items | Estimated Cost |
| :--- | :--- | :--- |
| **⚡ Quick check** | 100 | **$0.10** |
| **🏎️ Standard Run** | 1,000 | **$1.00** |
| **🏭 Large run** | 3,000 | **$3.00** |

#### ⚠️ Limitations

- **🆓 Free Users**: Limited to up to **5 items per run** and **5 runs per day** with a **30-minute cooldown** between runs. Upgrade to the paid plan to lift the limitation.

#### 🛠️ Input Parameters

| Parameter | Type | Default Value | Description |
| :--- | :--- | :--- | :--- |
| `searchUrl` | String | - | **Required**. The URL of the search results from Mobile.de. |
| `maxItems` | Integer | `100` | Maximum number of items to scrape. |

##### 💡 Example Input

```json
{
    "searchUrl": "https://suchen.mobile.de/fahrzeuge/search.html?isSearchRequest=true&s=Car&vc=Car",
    "maxItems": 50
}
```

#### 📦 Data Output

The actor stores results in a dataset. Each item is flat and easy to analyze:

```json
{
	"attr_c": "EstateCar",
	"attr_cc": "1,991 ccm",
	"attr_cn": "DE",
	"attr_door": "4/5",
	"attr_ecol": "Brown",
	"attr_emc": "Euro6",
	"attr_fr": "05/2014",
	"attr_ft": "Petrol",
	"attr_gi": "New",
	"attr_loc": "Magdeburg",
	"attr_ml": "112,205 km",
	"attr_nw": "1,785 kg",
	"attr_pw": "155 kW (211 hp)",
	"attr_sc": "7",
	"attr_tr": "Automatic",
	"attr_z": "39112",
	"category": "Estate car",
	"created": 1762422621,
	"created_human": "2025-11-06 09:50:21",
	"customDimensions": {
      "10": "platinum"
	},
	"hasDamage": false,
	"id": 440753711,
	"images": ["..."],
	"isEyeCatcher": false,
	"isVideoEnabled": false,
	"kba_hsn": "1313",
	"kba_tsn": "DDW",
	"mainImage": "https://img.classistatic.de/api/v1/mo-prod/images/9b/9b62bb60-d021-426a-bff7-953a6f7cdd94?rule=mo-360w",
	"make": "Mercedes-Benz",
	"makeId": 17200,
	"model": "E 250",
	"modelId": 51,
	"modified": 1768932862,
	"modified_human": "2026-01-20 18:14:22",
	"numImages": 26,
	"price": "€21,300",
	"priceRating_label": "Fair price",
	"priceRating_rating": "REASONABLE_PRICE",
	"price_amount": 21300,
	"price_currency": "EUR",
	"readyToDrive": true,
	"renewed": 1768932859,
	"renewed_human": "2026-01-20 18:14:19",
	"scrapedAt": "2026-01-24T15:38:53.902Z",
	"scrapedAt_human": "2026-01-24 15:38:53",
	"segment": "Car",
	"sellerId": 14232991,
	"seller_address": "Blankenburgerstr. 56",
	"seller_country": "DE",
	"seller_lat": 52.1041018,
	"seller_lon": 11.6004269,
	"seller_name": "Auto Zentrum Magdeburg",
	"seller_type": "Dealer",
	"shortTitle": "Mercedes-Benz E 250",
	"siteId": "GERMANY",
	"st": "Dealer",
	"subTitle": "AVANTGARDE *STANDH.*AHK*LED*NAVI*7 SITZE",
	"title": "Mercedes-Benz E 250 AVANTGARDE *STANDH.*AHK*LED*NAVI*7 SITZE",
	"url": "https://suchen.mobile.de/auto-inserat/mercedes-benz-e-250-avantgarde-standh-ahk-led-navi-7-sitze-magdeburg/440753711.html",
	"vc": "Car",
	"version": 32
}
```

#### 🔍 SEO Keywords

mobile.de scraper, mobile.de api, scrape germany cars, german car market data, automotive data extraction, monitor used car prices, vehicle data api, car dealer inventory scraper, mobile.de python, apify mobile.de, cars listing tracking.

***

**Need a custom solution? Have a feature request or just want to chat?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

# Actor input Schema

## `searchUrl` (type: `string`):

The URL of the search results page on mobile.de

## `maxItems` (type: `integer`):

Maximum number of items to scrape.

## Actor input object example

```json
{
  "searchUrl": "https://suchen.mobile.de/fahrzeuge/search.html?dam=false&isSearchRequest=true&ml=%3A10000&p=%3A500&ref=quickSearch&s=Car&vc=Car",
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
    "searchUrl": "https://suchen.mobile.de/fahrzeuge/search.html?dam=false&isSearchRequest=true&ml=%3A10000&p=%3A500&ref=quickSearch&s=Car&vc=Car"
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/mobile-de-scraper-pro-by-search-url").call(input);

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
run_input = { "searchUrl": "https://suchen.mobile.de/fahrzeuge/search.html?dam=false&isSearchRequest=true&ml=%3A10000&p=%3A500&ref=quickSearch&s=Car&vc=Car" }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/mobile-de-scraper-pro-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "searchUrl": "https://suchen.mobile.de/fahrzeuge/search.html?dam=false&isSearchRequest=true&ml=%3A10000&p=%3A500&ref=quickSearch&s=Car&vc=Car"
}' |
apify call azzouzana/mobile-de-scraper-pro-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/mobile-de-scraper-pro-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
