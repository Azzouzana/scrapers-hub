# 🚀 ImmoScout24 Listing Scraper (By Listings URLs)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the ImmoScout24 Listing Scraper (By Listings URLs). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/immobilienscout24-de-properties-pages-scraper?fpr=cbgdsf)

---

## ImmoScout24 Listing Scraper (By Listings URLs)

### 🤩 Features

🚀 Our blazing fast immobilienscout24.de properties details pages scraper lets you extract properties information and
export them to various format (JSON, CSV, HTML etc..)

🔥 Bring your properties URLs, and you're good to go!

👉 It enables you to scrape rich details as title, description, photos, construction date, price, publisher
information (email/phone number included), and a lot more.

### 📚 How to use this actor

1. 👉 [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required!
2. 🎉 Just click the **"Get Started"** button and complete a quick signup.
3. 💰 A free account includes enough credits to test this actor.
4. ⏳ Enjoy scraping for the free trial period, no commitment or upfront payment required.

The scraper has a required `startUrls` parameter which is an array holding a list of direct properties URLs

- Examples of valid URL:
    - `https://www.immobilienscout24.de/expose/149965957`

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

### 🤔 Why scrape immobilienscout24.de?

immobilienscout24.de is the largest real estate website in Germany, with hundreds of thousand of ads, there's definitely
something for you out there!

So what could you do with all these ads?

- Find real estate for sale nearby
- Do market data analysis
- Build a real estate agent email list
- Collect housing data for research or personal purposes
- Compare collected data with home value index
- Use the data for overall real estate data analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

### 🛠️ Input

| Field | Type | Description | Default value / Example |
| ----- | ---- | ----------- | ------------- |
| `startUrls` | `array` | direct properties URLs | `https://www.immobilienscout24.de/expose/149965957`

### 🧐 Output

Output is stored in a dataset. Each item is comprehensive information about a real estate listing:

#### Output examples

An output might look like the below data structure:

```json
{
    "header": {
        "id": "158907289",
        "title": "Description",
        "fraudReportUrl": "https://angebot-melden.immobilienscout24.de/report?realEstateId=158907289&publicationState=live",
        "displayStatusIcon": true,
        "shareMessage": "I found this offer on ImmoScout24:\nhttps://www.immobilienscout24.de/expose/158907289?utm_medium=social&utm_campaign=expose_sharing&utm_content=expose_toolbar&utm_source=other&referrer=taf\n\n        Details\n-------------------------\nBasic rent €30.63/m²: €2,345.33\nRooms:          3\nLiving space:   76.58 m²\nTotal rent:     €2,799.30\n\nPufendorfstraße 3A-3E\n10249 Friedrichshain, Berlin",
        "publicationState": "active",
        "isTenantNetwork": false,
        "realEstateType": "apartmentrent"
    },
    "sections": [
        {
            "type": "MEDIA",
            "featuredBarColor": "#4D4948",
            "featuredRealtorLogoUrl": "https://pictures.immobilienscout24.de/usercontent/5b436368-d6d6-48cb-a54d-b5356279c6a2.PNG/ORIG/resize/%WIDTH%x%HEIGHT%%3E/format/webp/quality/80",
            "media": ["..."]
        },
        {
            "type": "TOP_ATTRIBUTES",
            "attributes": ["..."]
        },
        {
            "type": "TITLE",
            "title": "Neubau Erstbezug * 3 Zimmer Wohnung im 5.OG * Gäste-WC * Balkon * TG Stellplatz"
        },
        {
            "type": "TAG_LIST",
            "tagType": "TAG",
            "tags": [...]
        },
        {
            "type": "RELOCATION",
            "text": "How much would relocation cost?",
            "subText": "Get free offers",
            "reference": {...}
        },
        {
            "type": "MAP",
            "title": "Map",
            "location": {
                "lat": 52.52193,
                "lng": 13.43821
            },
            "addressLine1": "Pufendorfstraße 3A-3E",
            "addressLine2": "10249 Friedrichshain, Berlin",
            "zipCodeShapes": [],
            "enableEnterFullAddressAction": true
        },
        {
            "type": "REFERENCE_LIST",
            "references": [...]
        },
        {
            "type": "TRAVELTIME",
            "isBlocked": false,
            "exposeId": "158907289",
            "address": "Pufendorfstraße 3A-3E, 10249 Friedrichshain, Berlin",
            "location": {
                "lat": 52.52193,
                "lng": 13.43821
            }
        },
        {
            "type": "ATTRIBUTE_LIST",
            "title": "Main criteria",
            "attributes": ["..."]
        },
        {
            "type": "ATTRIBUTE_LIST",
            "title": "Costs",
            "attributes": ["..." ]
        },
        {
            "type": "COST_CHECK",
            "totalRent": 2799.3,
            "expenses": ["..."]
        },
        {
            "type": "PREMIUM_ADDITIONAL_INFO",
            "title": "Plus Members know more",
            "isExposeBuy": false,
            "chancenCheck": {...},
            "competitionAnalysis": {...},
            "quickCartButton": {...},
            "visits": null,
            "contactRequests": null,
            "shortlistAddEvents": null,
            "prospectiveCustomersCount": {...},
            "newExposeHoursThreshold": null,
            "calculated": null,
            "privateOffer": null,
            "onlineSince": null
        },
        {
            "type": "ATTRIBUTE_LIST",
            "title": "Building details & energy certificate",
            "attributes": ["..."]
        },
        {
            "type": "PROJECT_EXPOSE_LIST",
            "title": "Further residential units of this project",
            "items": ["..."],
            "reference": {...}
        },
        {
            "type": "TEXT_AREA",
            "title": "Property Description",
            "collapseAfterLines": 5,
            "text": "PANDION MIDTOWN ist für alle da: für alle Lebensphasen, für alle Familiengrößen, für alle Wohnwünsche – eben einfach für alle Fälle. Größen von 1 bis 4 Zimmern mit ca. 46 m² bis ca. 120 m² freuen sich auf Singles, Paare oder Familien, die in ihnen den Alltag genießen - kochen, essen, schlafen, feiern, spielen. Kurz: die hier glücklich leben wollen."
        },
        {
            "type": "TEXT_AREA",
            "title": "Furnishing",
            "collapseAfterLines": 5,
            "text": "Wohnzimmer mit offener Küche\n- Fensterfronten mit West-/Nordausrichtung\n- Mehrschichtparkett\n- voll ausgestattete moderne Küche mit hochwertigen Elektrogeräten (siehe Visualisierung)\n- Zugang zum Balkon\n- LAN Anschlüsse\n\nSchlafzimmer\n- Mehrschichtparkett\n- LAN Anschluss\n\nweiteres Schlafzimmer nutzbar als Arbeits-/Gäste- bzw. Kinderzimmer\n- Mehrschichtparkett\n- LAN Anschluss\n\nBad\n- bodentiefe Dusche\n- Waschtisch mit Unterschrank\n- Spiegel\n- wandhängendes WC\n- elektrischer Handtuchheizkörper\n- Feinsteinfliesen\n\nGäste-WC\n- Waschtisch mit Unterschrank\n- Spiegel\n- wandhängendes WC\n- elektrischer Handtuchheizkörper\n- Feinsteinfliesen\n- Anschlüsse für Waschmaschine und Trockner\n\nBalkon\n- Holzdielenboden\n- Stromanschluss\n\nZur Wohnung gibt es auch einen Kellerraum.\n\nZur Wohnung gehört ein Tiefgaragenstellplatz, welcher aber erst zu einem späteren Zeitpunkt nutzbar ist (voraussichtlich ab ca. 01.2026 bzw. bis spätestens 08.2026)."
        },
        {
            "type": "TEXT_AREA",
            "title": "Location",
            "collapseAfterLines": 5,
            "text": "Mitten in der Hauptstadt, mitten im Kiez, mitten im Leben: Für PANDION MIDTOWN ist der Name Programm. Denn hier pulsiert das Leben, wohin man auch schaut. Ob mit Freunden grillen im nahegelegenen Volkspark, ein Bummel über den Flohmarkt am Boxhagener Platz oder auf ein Getränk in eines der vielen kleinen Cafés einkehren – Friedrichshain lässt einfach keine Wünsche offen. Und ist dabei auch noch exzellent angebunden. So erreicht man den Alexanderplatz nach zwei U-Bahn- oder vier Tram-Haltestellen, den Hauptbahnhof direkt mit der neuen U5. Und der Flughafen? Liegt in etwa gleicher Entfernung: mit dem Auto sind Sie in 40 Minuten in Schönefeld."
        },
        {
            "type": "TEXT_AREA",
            "title": "Further notes",
            "collapseAfterLines": 5,
            "text": "Wir haben Ihr Interesse geweckt? Dann senden Sie uns bitte eine Anfrage mit einigen Angaben über Ihre Person zu. Wir melden uns im Anschluss zwecks Absprache eines Besichtigungstermins bei Ihnen.\n\nEs wird ein Kündigungsausschluss von 12 Monaten vereinbart und eine Indexmiete p.a..\n\nDie Nebenkosten für den Stellplatz in Höhe von 35,- €/mtl. sind bereits in den Gesamtnebenkosten enthalten. \n\nDie abgebildete Möblierung im Grundriss ist nur Beispielhaft. \n\nAlle Angaben basieren auf Informationen des Vermieters. Eine Haftung für diese Angaben kann nicht übernommen werden.\n\nWeitere Angebote finden Sie auf unserer Homepage www.pandion-service.de"
        },
        {
            "type": "REFERENCE_LIST",
            "title": "Services consistent with the flat",
            "references": ["..."]
        },
        {
            "type": "PRICE_INFO",
            "title": "Information about price and location",
            "attributes": ["..."],
            "priceBar": {...},
            "calculationInformation": {"..."}
        },
        {
            "type": "REFERENCE_LIST",
            "title": "Additional documents",
            "references": ["..."]
        },
        {
            "type": "AGENTS_INFO",
            "title": "Agent's info",
            "company": "PANDION Servicegesellschaft mbH",
            "name": "Mr. Thomas Bernhard",
            "logoUrl": "https://pictures.immobilienscout24.de/usercontent/5b436368-d6d6-48cb-a54d-b5356279c6a2.PNG/ORIG/resize/%WIDTH%x%HEIGHT%%3E/format/webp/quality/80",
            "rating": {...},
            "verifiedBy": ["..."],
            "dsaSelfDeclaration": {...},
            "address": "",
            "references": ["..."],
            "brandBar": {}
        },
        {
            "type": "OBJECT_INFO",
            "text": "Scout-ID: 158907289 | Property ID: 139213"
        },
        {
            "type": "FRAUD_REPORT",
            "text": "Something suspicious about this offer?",
            "reference": {...}
        }
    ],
    "contact": {...},
    "tracking": {...},
    "adTargetingParameters": {...}
}
````

### 🔍 **Looking for something else?**

Feel free to explore [+4,000 pre-built scrapers on Apify Store](https://apify.com/store?fpr=cbgdsf) for more options!

### ⚠️ Disclaimer

This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Immobilien Scout GmbH or any
of its subsidiaries. All trademarks mentioned are the property of their respective owners.

# Actor input Schema

## `startUrls` (type: `array`):

direct properties URLs

## Actor input object example

```json
{
  "startUrls": [
    "https://www.immobilienscout24.de/expose/999999999"
  ]
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
    "startUrls": [
        "https://www.immobilienscout24.de/expose/999999999"
    ]
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/immobilienscout24-de-properties-pages-scraper").call(input);

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
run_input = { "startUrls": ["https://www.immobilienscout24.de/expose/999999999"] }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/immobilienscout24-de-properties-pages-scraper").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrls": [
    "https://www.immobilienscout24.de/expose/999999999"
  ]
}' |
apify call azzouzana/immobilienscout24-de-properties-pages-scraper --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/immobilienscout24-de-properties-pages-scraper",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
