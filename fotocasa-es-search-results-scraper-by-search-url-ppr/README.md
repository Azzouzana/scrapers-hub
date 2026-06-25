# 🚀 Fotocasa.es Property Listings Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Fotocasa.es Property Listings Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/fotocasa-es-search-results-scraper-by-search-url-ppr?fpr=cbgdsf)

---

## Fotocasa.es Property Listings Scraper (By Search URL)

### 🤩 Features

🚀 Our blazing fast fotocasa.es search results scraper & monitor🏠 lets you extract real estate ads' information and export them to various format (JSON, CSV, HTML etc..)
🔥 Bring your search URL and you're good to go!
👉 It enables you to scrape rich details as title, descriptions, photos, energy information, construction date, price, publisher information (email/phone number included) nearby transaportations and a lot more.

The scraper has a required `startUrl` parameter which is an array holding a list of direct real estate links
- Examples of valid URL:
  - `https://www.fotocasa.es/en/buy/homes/madrid-capital/all-zones/l?maxPrice=50000`

### 🤔 Why scrape fotocasa.es?

fotocasa.es is the largest real estate website in Spain, with hundreds of thousand of ads, there's definitely something for you out there!

So what could you do with all these ads?

- Find real estate for sale nearby
- Do market data analysis
- Build a real estate agent email list
- Collect housing data for research or personal purposes
- Compare collected data with home value index
- Use the data for overall real estate data analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

### 🤑 Cost of usage

This actor uses a pay-per-result pricing model. You only pay for what you get. The usage cost is $1 per 1,000 items.

#### Cost Calculation Example

You want to scrape **2,000 listings**.
- Total cost: (2,000 / 1,000) * $1 = **$2.00**

> **Note:** This is a Pay-Per-Event actor. You are only charged for successfully scraped items.

### 🛠️ Input

| Field | Type | Description | Default value / Example |
| ----- | ----- | ----------- | ----------------------- |
| `startUrl` | `url` | The search page's result link | `https://www.fotocasa.es/en/buy/homes/madrid-capital/all-zones/l?maxPrice=50000` |
| `maxItems` | `integer` | Maximum number of listings to scrape | `100` |

### 🧐 Output

Output is stored in a dataset. Each item is information about a real estate item.

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

#### Output examples

Output is stored in a dataset. Each item is information about a real estate item:

An output might look like this:

```json
{
	"accuracy": false,
	"address": {
		"country": "España",
		"district": "Sant Martí",
		"neighborhood": "El Poblenou",
		"zipCode": "08005",
		"municipality": " Barcelona Capital",
		"province": "Barcelona",
		"city": " Barcelona Capital",
		"cityZone": null,
		"county": "Barcelonès",
		"regionLevel1": "Cataluña",
		"regionLevel2": "Barcelona",
		"upperLevel": "El Poblenou"
	},
	"brandInfo": {
		"barColor": "#F03A4E",
		"logo": null,
		"textColor": "#FFFFFF"
	},
	"buildingSubtype": "Apartment",
	"buildingType": "Flat",
	"clientAlias": "ENGEL & VOELKERS",
	"clientId": 9202758116439,
	"clientType": "professional",
	"clientTypeId": 3,
	"clientUrl": "/es/inmobiliaria-engel-voelkers/comprar/inmuebles/espana/todas-las-zonas/l?clientId=9202758116439",
	"coordinates": {
		"latitude": 41.404611047192674,
		"longitude": 2.2062628054871825,
		"accuracy": 0
	},
	"date": {
		"diff": 0,
		"unit": "NOW"
	},
	"dateOriginal": {
		"diff": 114,
		"unit": "DAYS",
		"timestamp": 1744299137323
	},
	"description": "Encantador piso, con acabados de alta gama, que combina encanto clásico y modernidad. Ubicado en una finca con ascensor del 1930 en la calle Espronceda, esta propiedad ha sido cuidadosamente restaurada realzando sus elementos originales, como la bóveda catalana y los suelos de mosaico hidráulico, creando un ambiente único y con carácter. El piso se compone de un espacio abierto que integra sala de estar, comedor y una moderna cocina; de una amplia galería, ideal como estudio; de una habitación matrimonial y un elegante baño. Recibe sol de mañana.\nExclusiva cocina de diseño danés, equipada con electrodomésticos Bosch (nevera, lavavajillas, horno, microondas e inducción); grifería Maier; las ventanas son de doble acristalamiento 6/12/4 y con rotura de puente térmico; el sistema de aire acondicionado y calefacción es por Split. \n\nPerfecto para una pareja o para quien quiera tener un pied á terre en Barcelona, muy buena opción también para quien busca un piso para poner en alquiler.\nLa propiedad dispone de una excelente ubicación al encontrarse a 7 minutos caminando de la playa y cerca de la Rambla de Poblenou donde se puede encontrar todo tipo de oferta gastronómica y comercial. Muy bien comunicada (buses y metro a 2 cuadras) y cerca de varios parques.",
	"detail": {
		"es-ES": "/es/comprar/vivienda/barcelona-capital/aire-acondicionado-calefaccion-ascensor-no-amueblado/186181599/d"
	},
	"externalContactUrl": null,
	"features": {
		"antiquity": 9,
		"bathrooms": 1,
		"conservationStatus": 2,
		"floor": 0,
		"heating": 0,
		"hotWater": 0,
		"orientation": 0,
		"rooms": 2,
		"surface": 45
	},
	"hasListLogo": true,
	"hasSubsidies": false,
	"hasVideo": 0,
	"hasStamp": true,
	"hasVgo": false,
	"hasFloorPlans": false,
	"id": "1_186181599",
	"isDiscarded": false,
	"isExternalContact": false,
	"isCompleted": null,
	"isFaved": false,
	"isHighlighted": false,
	"isPackAdvancePriority": false,
	"isPackBasicPriority": false,
	"isPackMinimalPriority": false,
	"isPackPremiumPriority": true,
	"isMainTypology": false,
	"isNew": false,
	"isNewConstruction": false,
	"hasOpenHouse": false,
	"isOpportunity": false,
	"isPremium": false,
	"isPromotion": false,
	"isTrackedPhone": true,
	"isTop": true,
	"isTopPlus": true,
	"isVisited": false,
	"isVirtualTour": false,
	"location": {
		"address": "Sant Martí",
		"zone": " Barcelona Capital, Barcelona",
		"municipality": "Sant Martí",
		"locality": " Barcelona Capital"
	},
	"minPrice": 0,
	"multimedia": [
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/e6012ad1-dc96-486f-935e-f58a4eb37af3?rule=original",
			"roomType": "exterior"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/e9b750e7-f6d1-4231-857d-b686d713180d?rule=original",
			"roomType": "kitchen"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/5bd667a7-1d06-4a5c-b67e-0e353e52d546?rule=original",
			"roomType": "living room"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/33ae5899-076b-457b-81cc-32a12a8f51f9?rule=original",
			"roomType": "other"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/7d860425-63bd-402a-b1e0-f163b92915d0?rule=original",
			"roomType": "kitchen"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/c77a7054-9932-4645-96fe-87ba6ec41d0a?rule=original",
			"roomType": "dining room"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/9ef679e8-5fdd-462f-b51f-daf6f8cb1a67?rule=original",
			"roomType": "dining room"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/6d781051-f94f-48fc-9b43-54c1fb0366b3?rule=original",
			"roomType": "living room"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/4eb73365-0dee-41ac-8dbc-206a64a3f749?rule=original",
			"roomType": "other"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/1b12c870-f1e3-4829-8583-6dacc2015810?rule=original",
			"roomType": "bathroom"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/1da2bb77-597b-42cd-bb9d-deb0137ab231?rule=original",
			"roomType": "bathroom"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/4e888966-abf9-4737-bfbc-158c17aeda64?rule=original",
			"roomType": "kitchen"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/da25a4ea-e337-467a-b550-3ecb6b615b2b?rule=original",
			"roomType": "other"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/8d1c60d5-94e9-49b6-830d-60a21730b5e0?rule=original",
			"roomType": "other"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/2464b2bc-ccba-4d9b-ae22-cbe8d3356223?rule=original",
			"roomType": "other"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/7772f7f1-9518-4ab9-b4ef-5d97541bfd89?rule=original",
			"roomType": "living room"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/03ccdd51-d4c4-4495-80bb-78b387cd738f?rule=original",
			"roomType": "other"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/0835ab61-1ab2-43e4-b884-446c58c8de31?rule=original",
			"roomType": "other"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/e3197428-089a-48e9-a79f-4867a9f99333?rule=original",
			"roomType": "balcony"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/0ef35479-3556-4d2a-8700-901c8b586b1f?rule=original",
			"roomType": "balcony"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/ac50b770-d4e2-439b-8375-b8a3a6b20089?rule=original",
			"roomType": "bedroom"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/00fff67b-16e2-420d-a34c-8fe28a4accdd?rule=original",
			"roomType": "bedroom"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/64f4d5b3-1c24-4f33-ad17-5ddb9f19cf29?rule=original",
			"roomType": "other"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/377cc4b9-f706-4c16-8f99-360650212f9b?rule=original",
			"roomType": "garden"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/f7c58c42-641f-414c-b56c-fdde9e1c9759?rule=original",
			"roomType": "terrace"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/8c87429b-371c-48b4-be9e-b1109c6be99d?rule=original",
			"roomType": "exterior"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/e5dc334f-f0ce-42e4-b874-872f1c83e13f?rule=original",
			"roomType": "terrace"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/face456d-bc55-44d2-ab87-af66de638b8c?rule=original",
			"roomType": "terrace"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/245aea58-7052-4012-a9ca-3892a2d5e31a?rule=original",
			"roomType": "other"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/847cfda8-f265-42ab-8b3e-f98ce9300019?rule=original",
			"roomType": "other"
		},
		{
			"type": "image",
			"src": "https://static.fotocasa.es/images/ads/1f3675b0-ee8c-405b-8b28-734708374a06?rule=original",
			"roomType": "exterior"
		}
	],
	"otherFeaturesCount": 0,
	"periodicityId": 0,
	"phone": "935433386",
	"price": {
		"amount": 338000,
		"amountDrop": 17000
	},
	"promotionId": 0,
	"promotionLogo": "https://static.fotocasa.es/images/client/fbf9f07f-f160-44e0-adbc-0ba48ef41f10/20250519081942?rule=original",
	"promotionUrl": null,
	"promotionTitle": null,
	"promotionTypologiesCounter": null,
	"promotionTypologies": [],
	"publisherId": "fbf9f07f-f160-44e0-adbc-0ba48ef41f10",
	"rawPrice": 338000,
	"realEstateAdId": "41dd455f-8317-4bca-a622-846a1865b6fa",
	"reducedPrice": "17.000 €",
	"subtypeId": 2,
	"transactionTypeId": 1,
	"typeId": 2,
	"userId": null,
	"detailUrl": "/es/comprar/vivienda/barcelona-capital/aire-acondicionado-calefaccion-ascensor-no-amueblado/186181599/d",
	"multimedias": [
		{
			"classification": "exterior",
			"position": 1,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/e6012ad1-dc96-486f-935e-f58a4eb37af3?rule=original"
		},
		{
			"classification": "kitchen",
			"position": 2,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/e9b750e7-f6d1-4231-857d-b686d713180d?rule=original"
		},
		{
			"classification": "living room",
			"position": 3,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/5bd667a7-1d06-4a5c-b67e-0e353e52d546?rule=original"
		},
		{
			"classification": "other",
			"position": 4,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/33ae5899-076b-457b-81cc-32a12a8f51f9?rule=original"
		},
		{
			"classification": "kitchen",
			"position": 5,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/7d860425-63bd-402a-b1e0-f163b92915d0?rule=original"
		},
		{
			"classification": "dining room",
			"position": 6,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/c77a7054-9932-4645-96fe-87ba6ec41d0a?rule=original"
		},
		{
			"classification": "dining room",
			"position": 7,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/9ef679e8-5fdd-462f-b51f-daf6f8cb1a67?rule=original"
		},
		{
			"classification": "living room",
			"position": 8,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/6d781051-f94f-48fc-9b43-54c1fb0366b3?rule=original"
		},
		{
			"classification": "other",
			"position": 9,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/4eb73365-0dee-41ac-8dbc-206a64a3f749?rule=original"
		},
		{
			"classification": "bathroom",
			"position": 10,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/1b12c870-f1e3-4829-8583-6dacc2015810?rule=original"
		},
		{
			"classification": "bathroom",
			"position": 11,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/1da2bb77-597b-42cd-bb9d-deb0137ab231?rule=original"
		},
		{
			"classification": "kitchen",
			"position": 12,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/4e888966-abf9-4737-bfbc-158c17aeda64?rule=original"
		},
		{
			"classification": "other",
			"position": 13,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/da25a4ea-e337-467a-b550-3ecb6b615b2b?rule=original"
		},
		{
			"classification": "other",
			"position": 14,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/8d1c60d5-94e9-49b6-830d-60a21730b5e0?rule=original"
		},
		{
			"classification": "other",
			"position": 15,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/2464b2bc-ccba-4d9b-ae22-cbe8d3356223?rule=original"
		},
		{
			"classification": "living room",
			"position": 16,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/7772f7f1-9518-4ab9-b4ef-5d97541bfd89?rule=original"
		},
		{
			"classification": "other",
			"position": 17,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/03ccdd51-d4c4-4495-80bb-78b387cd738f?rule=original"
		},
		{
			"classification": "other",
			"position": 18,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/0835ab61-1ab2-43e4-b884-446c58c8de31?rule=original"
		},
		{
			"classification": "balcony",
			"position": 19,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/e3197428-089a-48e9-a79f-4867a9f99333?rule=original"
		},
		{
			"classification": "balcony",
			"position": 20,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/0ef35479-3556-4d2a-8700-901c8b586b1f?rule=original"
		},
		{
			"classification": "bedroom",
			"position": 21,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/ac50b770-d4e2-439b-8375-b8a3a6b20089?rule=original"
		},
		{
			"classification": "bedroom",
			"position": 22,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/00fff67b-16e2-420d-a34c-8fe28a4accdd?rule=original"
		},
		{
			"classification": "other",
			"position": 23,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/64f4d5b3-1c24-4f33-ad17-5ddb9f19cf29?rule=original"
		},
		{
			"classification": "garden",
			"position": 24,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/377cc4b9-f706-4c16-8f99-360650212f9b?rule=original"
		},
		{
			"classification": "terrace",
			"position": 25,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/f7c58c42-641f-414c-b56c-fdde9e1c9759?rule=original"
		},
		{
			"classification": "exterior",
			"position": 26,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/8c87429b-371c-48b4-be9e-b1109c6be99d?rule=original"
		},
		{
			"classification": "terrace",
			"position": 27,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/e5dc334f-f0ce-42e4-b874-872f1c83e13f?rule=original"
		},
		{
			"classification": "terrace",
			"position": 28,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/face456d-bc55-44d2-ab87-af66de638b8c?rule=original"
		},
		{
			"classification": "other",
			"position": 29,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/245aea58-7052-4012-a9ca-3892a2d5e31a?rule=original"
		},
		{
			"classification": "other",
			"position": 30,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/847cfda8-f265-42ab-8b3e-f98ce9300019?rule=original"
		},
		{
			"classification": "exterior",
			"position": 31,
			"type": "IMAGE",
			"url": "https://static.fotocasa.es/images/ads/1f3675b0-ee8c-405b-8b28-734708374a06?rule=original"
		}
	],
	"publisher": {
		"alias": "ENGEL & VOELKERS",
		"id": "9202758116439",
		"isBank": false,
		"logo": "https://static.fotocasa.es/images/client/fbf9f07f-f160-44e0-adbc-0ba48ef41f10/20250519081942?rule=original",
		"name": "EV MMC SPAIN ,S.L.U",
		"publisherId": "fbf9f07f-f160-44e0-adbc-0ba48ef41f10",
		"reference": "I-02ZJLM-W-02ZJLM",
		"type": "professional",
		"urls": [
			{
				"language": "es_ES",
				"value": "/inmobiliarias/engel-voelkers-9202758116439"
			},
			{
				"language": "ca_ES",
				"value": "/ca/immobiliaries/engel-voelkers-9202758116439"
			},
			{
				"language": "de_DE",
				"value": "/de/immobilienagentur/engel-voelkers-9202758116439"
			},
			{
				"language": "en_US",
				"value": "/en/real-estate-agencies/engel-voelkers-9202758116439"
			}
		]
	},
	"propertyId": 186181599,
	"propertySubtype": "APARTMENT",
	"propertyType": "HOMES",
	"transactionType": "SALE"
}
````

***

**Need a custom solution? Have a feature request or just want to chat?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

# Actor input Schema

## `startUrl` (type: `string`):

The search page URL to scrape from fotocasa.es.

## `maxItems` (type: `integer`):

Maximum number of listings to scrape.

## Actor input object example

```json
{
  "startUrl": "https://www.fotocasa.es/es/comprar/viviendas/barcelona-capital/todas-las-zonas/l?maxPrice=50000",
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
    "startUrl": "https://www.fotocasa.es/es/comprar/viviendas/barcelona-capital/todas-las-zonas/l?maxPrice=50000",
    "maxItems": 2000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/fotocasa-es-search-results-scraper-by-search-url-ppr").call(input);

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
    "startUrl": "https://www.fotocasa.es/es/comprar/viviendas/barcelona-capital/todas-las-zonas/l?maxPrice=50000",
    "maxItems": 2000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/fotocasa-es-search-results-scraper-by-search-url-ppr").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.fotocasa.es/es/comprar/viviendas/barcelona-capital/todas-las-zonas/l?maxPrice=50000",
  "maxItems": 2000
}' |
apify call azzouzana/fotocasa-es-search-results-scraper-by-search-url-ppr --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/fotocasa-es-search-results-scraper-by-search-url-ppr",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
