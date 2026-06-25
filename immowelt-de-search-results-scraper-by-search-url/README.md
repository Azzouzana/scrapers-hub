# 🚀 Immowelt.de Property Listings Scraper — Classifieds & New Projects (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Immowelt.de Property Listings Scraper — Classifieds & New Projects (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/immowelt-de-search-results-scraper-by-search-url?fpr=cbgdsf)

---

## Immowelt.de Property Listings Scraper — Classifieds & New Projects (By Search URL)

### 🤩 Features

🚀 Our blazing fast immowelt.de search results scraper & monitor🏠 lets you extract real estate ads' information and
export them to various format (JSON, CSV, HTML etc..)
🔥 Bring your search URL and you're good to go! We support both classified & new projects search sections!
👉 It enables you to scrape rich details as title, descriptions, photos, energy information, construction date, price,
publisher information, contact details, nearby transportation and much more. 🚀

The scraper has a required `startUrl` parameter which is an array holding a list of classifieds or new projects search URLS:

- Examples of valid URL:
    - `https://www.immowelt.de/classified-search?distributionTypes=Buy,Buy_Auction&estateTypes=House,Apartment&locations=AD08DE6748`
    - `https://www.immowelt.de/project-search?distributionTypes=Buy&estateTypes=House,Apartment&locations=AD08DE6345&projectTypes=New_Build`

### 🤔 Why scrape immowelt.de?

immowelt.de is one of the top real estate websites in Germany, with hundreds of thousand of ads, there's definitely something for
you out there!

So what could you do with all these ads?

- Find real estate for sale nearby
- Do market data analysis
- Build a real estate agent email list
- Collect housing data for research or personal purposes
- Compare collected data with home value index
- Use the data for overall real estate data analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

### 🤑 Cost of usage

The cost of using this scraper is **$1.00 for every 1000 real estate items scraped**, no hidden fees!


### 🛠️ Input

| Field | Type | Description | Default value / Example |
| ----- | ---- | ----------- | ------------- |
| `startUrl` | `array` | the search page's result link | `https://www.immowelt.de/classified-search?distributionTypes=Buy,Buy_Auction&estateTypes=House,Apartment&locations=AD08DE6748` |
| `enableFlattening` | `boolean` | Enable or disable data flattening | `false` |
| `maxItems` | `number` | Maximum number of items to scrape | `2000` |


### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

### 🧐 Output

Output is stored in a dataset. Each item is information about a real estate item:

#### Output examples

The scraping result may look like this An output might look like this:
-with data flattening disabled:
```json
{
	"brand": "immowelt",
	"id": "263ELWYT61N2",
	"status": "Published",
	"metadata": {
		"id": "263ELWYT61N2",
		"legacyId": "a88d2b01-3bff-4477-a526-db79c284d1bb",
		"creationDate": "2026-02-13T12:29:13.64Z",
		"updateDate": "2026-02-13T12:29:29.936Z",
		"status": {
			"status": true,
			"enrichments": {
				"contactSettings": false,
				"geo": false,
				"intermediary": false,
				"media": false,
				"onlineId": false
			}
		}
	},
	"location": {
		"address": {
			"country": "DEU",
			"city": "Berlin",
			"zipCode": "12159",
			"street": "Friedenauer Höhe 14",
			"district": "Friedenau"
		},
		"isAddressPublished": true
	},
	"hardFacts": {
		"title": "Wohnung zur Miete - Erstbezug",
		"keyfacts": [
			"2 Zimmer",
			"48,3 m²",
			"5. Geschoss"
		],
		"facts": [
			{
				"type": "numberOfRooms",
				"value": "2 Zimmer",
				"splitValue": "2",
				"label": "Zimmer"
			},
			{
				"type": "livingSpace",
				"value": "48,3 m²",
				"splitValue": "48,3",
				"label": "m²"
			},
			{
				"type": "numberOfFloors",
				"value": "5. Geschoss",
				"splitValue": "5.",
				"label": "Geschoss"
			}
		],
		"price": {
			"value": "1.429 €",
			"formatted": "1.429 €",
			"additionalInformation": "Kaltmiete",
			"addition": {
				"value": "Kaltmiete"
			},
			"financialLink": {
				"href": "https://www.immowelt.de/immobilienfinanzierung-anfragen/?price=1429&originvariant=expose-hardfacts&zip=12159&city=Berlin&classifiedid=a88d2b01-3bff-4477-a526-db79c284d1bb&m=classified_detail_request_offer_find_financing_partners_step1",
				"label": "Finanzierung anfragen",
				"partnerName": "KFW"
			},
			"ariaLabel": "1429 €"
		},
		"prices": [
			{
				"label": "Kaltmiete",
				"value": "1.429 €",
				"ariaLabel": "1429 €"
			},
			{
				"label": "Warmmiete",
				"value": "1.619 €",
				"ariaLabel": "1619 €"
			}
		]
	},
	"gallery": {
		"images": [
			{
				"key": "7b85e374-2e40-4e91-849e-6246f0bbfcfc",
				"url": "https://mms.immowelt.de/7/b/8/5/7b85e374-2e40-4e91-849e-6246f0bbfcfc.jpg?ci_seal=7f00d16614ab5c14dea91417d3a25bdb2205a0e3",
				"description": "09_Südbalkone für alle Wohnungen",
				"alt": "Wohnung zur Miete - Erstbezug 1.429 € 2 Zimmer 48,3 m² 5. Geschoss Friedenauer Höhe 14 Friedenau Berlin 12159",
				"title": "09_Südbalkone für alle Wohnungen",
				"ariaLabel": "09_Südbalkone für alle Wohnungen",
				"classification": {
					"name": "BUILDING_FACADE",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "57f98588-b78e-4435-a9b7-e45db28b6300",
				"url": "https://mms.immowelt.de/5/7/f/9/57f98588-b78e-4435-a9b7-e45db28b6300.jpg?ci_seal=bd81ff24e148acf76da41e471891088378c24338",
				"description": "moderne Einbauküche",
				"title": "moderne Einbauküche",
				"ariaLabel": "moderne Einbauküche",
				"classification": {
					"name": "KITCHEN",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "1c458e7a-be73-4c13-ae47-c926fe58f1ce",
				"url": "https://mms.immowelt.de/1/c/4/5/1c458e7a-be73-4c13-ae47-c926fe58f1ce.jpg?ci_seal=44a35806c91824822f259fc57d41ad735071bcc1",
				"description": "Wonzimmer mit Zugang zum Balkon",
				"title": "Wonzimmer mit Zugang zum Balkon",
				"ariaLabel": "Wonzimmer mit Zugang zum Balkon",
				"classification": {
					"name": "EMPTY_ROOM",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "6a483897-fdc4-44eb-824d-111e06dc308f",
				"url": "https://mms.immowelt.de/6/a/4/8/6a483897-fdc4-44eb-824d-111e06dc308f.jpg?ci_seal=decb2178f1e757ceb0ff4e878cf6275a11f2abdb",
				"description": "separates Schlafzimmer",
				"title": "separates Schlafzimmer",
				"ariaLabel": "separates Schlafzimmer",
				"classification": {
					"name": "EMPTY_ROOM",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "ea3789b5-433d-42ed-a7b3-511d8fa831ac",
				"url": "https://mms.immowelt.de/e/a/3/7/ea3789b5-433d-42ed-a7b3-511d8fa831ac.jpg?ci_seal=f55d973fff3b32eb1cf6662ee81b5de140e04581",
				"description": "helle Räume",
				"title": "helle Räume",
				"ariaLabel": "helle Räume",
				"classification": {
					"name": "EMPTY_ROOM",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "f7b96b94-a367-4200-a22b-86a5c68c9809",
				"url": "https://mms.immowelt.de/f/7/b/9/f7b96b94-a367-4200-a22b-86a5c68c9809.jpg?ci_seal=188db3a6c034af29cfb0badd39479f2acdc6b4df",
				"description": "Offene Wohnküche",
				"title": "Offene Wohnküche",
				"ariaLabel": "Offene Wohnküche",
				"classification": {
					"name": "EMPTY_ROOM",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "022baf22-73df-494e-a90b-6ca814a2fb28",
				"url": "https://mms.immowelt.de/0/2/2/b/022baf22-73df-494e-a90b-6ca814a2fb28.jpg?ci_seal=40e7a557d0c6012dc03bc29289eb3d36a1e14468",
				"description": "himmlischer Balkon",
				"title": "himmlischer Balkon",
				"ariaLabel": "himmlischer Balkon",
				"classification": {
					"name": "BALCONY",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "6cda59b5-205f-4791-8277-361a921a27bf",
				"url": "https://mms.immowelt.de/6/c/d/a/6cda59b5-205f-4791-8277-361a921a27bf.jpg?ci_seal=86acc8e4ed6f4415f6f4f581649458773541ceae",
				"description": "modernes Wannenbad",
				"title": "modernes Wannenbad",
				"ariaLabel": "modernes Wannenbad",
				"classification": {
					"name": "BATHROOM",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "330bbd48-389a-487c-afcf-541a7f556db3",
				"url": "https://mms.immowelt.de/3/3/0/b/330bbd48-389a-487c-afcf-541a7f556db3.jpg?ci_seal=8e30f26d87df73edd470e18644aa94c477581ff8",
				"description": "praktische Einbauschränke im Flur",
				"title": "praktische Einbauschränke im Flur",
				"ariaLabel": "praktische Einbauschränke im Flur",
				"classification": {
					"name": "CLOSET",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "b8f61dca-8100-4dce-a649-c769f768871d",
				"url": "https://mms.immowelt.de/b/8/f/6/b8f61dca-8100-4dce-a649-c769f768871d.jpg?ci_seal=5d37626b2e74bc65dec7895ab39dd77e05cbb7c1",
				"description": "Stadtquartier Friedenauer Höhe",
				"title": "Stadtquartier Friedenauer Höhe",
				"ariaLabel": "Stadtquartier Friedenauer Höhe",
				"classification": {
					"name": "BUILDING_FACADE",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "535f9c8e-04a8-4fae-9149-cd282a40e63c",
				"url": "https://mms.immowelt.de/5/3/5/f/535f9c8e-04a8-4fae-9149-cd282a40e63c.jpg?ci_seal=bded393abaede08c83d484e9789c4ddc7e2523a2",
				"description": "Ruhepol + Kraftort",
				"title": "Ruhepol + Kraftort",
				"ariaLabel": "Ruhepol + Kraftort",
				"classification": {
					"name": "BUILDING_FACADE",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "9e5f75d9-5537-4ead-9398-0ed3d2b9a244",
				"url": "https://mms.immowelt.de/9/e/5/f/9e5f75d9-5537-4ead-9398-0ed3d2b9a244.jpg?ci_seal=50bd9ce6e0bf0f0cbfb3bf29dc4e2484c569c5a2",
				"description": "Ruhige Südausrichtung",
				"title": "Ruhige Südausrichtung",
				"ariaLabel": "Ruhige Südausrichtung",
				"classification": {
					"name": "EXTERIOR_VIEW",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "48a16c5c-af3b-4c00-8b64-f5cd037aa82c",
				"url": "https://mms.immowelt.de/4/8/a/1/48a16c5c-af3b-4c00-8b64-f5cd037aa82c.jpg?ci_seal=ea9e7aa7d2d495211e2e6a4dc68f54b19aec218d",
				"description": "Mitten im Schöneberger Ortsteil Friedenau",
				"title": "Mitten im Schöneberger Ortsteil Friedenau",
				"ariaLabel": "Mitten im Schöneberger Ortsteil Friedenau",
				"classification": {
					"name": "EXTERIOR_VIEW",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "e97500f6-38a4-4b62-a826-aa118db7046f",
				"url": "https://mms.immowelt.de/e/9/7/5/e97500f6-38a4-4b62-a826-aa118db7046f.jpg?ci_seal=0e657803bdbe3ebc7403b61af613bca600d79102",
				"description": "Südbalkone für alle Wohnungen",
				"title": "Südbalkone für alle Wohnungen",
				"ariaLabel": "Südbalkone für alle Wohnungen",
				"classification": {
					"name": "BUILDING_FACADE",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "599e304b-12ff-47e9-9eac-bb3eee63cdfd",
				"url": "https://mms.immowelt.de/5/9/9/e/599e304b-12ff-47e9-9eac-bb3eee63cdfd.jpg?ci_seal=ee8abeda74665cc498062083cb6e1efa9eb43a93",
				"description": "Wohnbereich Musterwohnung",
				"title": "Wohnbereich Musterwohnung",
				"ariaLabel": "Wohnbereich Musterwohnung",
				"classification": {
					"name": "LIVING_ROOM",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "d77c7cc7-0e49-4a04-abc0-26665eeb29c6",
				"url": "https://mms.immowelt.de/d/7/7/c/d77c7cc7-0e49-4a04-abc0-26665eeb29c6.jpg?ci_seal=f0c6ed0d417194cecc9674eccd36561f18583a22",
				"description": "Schlafzimmer Musterwohnung",
				"title": "Schlafzimmer Musterwohnung",
				"ariaLabel": "Schlafzimmer Musterwohnung",
				"classification": {
					"name": "BEDROOM",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "b385b72b-35c4-4f0a-8f1b-53ca4b6b581f",
				"url": "https://mms.immowelt.de/b/3/8/5/b385b72b-35c4-4f0a-8f1b-53ca4b6b581f.jpg?ci_seal=e81f516077a9d581465c279979a696d20b0399d6",
				"description": "Hochwertige Einbauküche und Einbauschränke",
				"title": "Hochwertige Einbauküche und Einbauschränke",
				"ariaLabel": "Hochwertige Einbauküche und Einbauschränke",
				"classification": {
					"name": "KITCHEN",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "d1f78a86-772c-4959-8ca2-36354d8795a6",
				"url": "https://mms.immowelt.de/d/1/f/7/d1f78a86-772c-4959-8ca2-36354d8795a6.jpg?ci_seal=e6decb6824a0e0311278e7afd474ee6695aeb9f4",
				"description": "Markenbad mit Wanne oder Dusche",
				"title": "Markenbad mit Wanne oder Dusche",
				"ariaLabel": "Markenbad mit Wanne oder Dusche",
				"classification": {
					"name": "BATHROOM",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "b90816ac-23ac-4ee0-9b86-bd2022aab985",
				"url": "https://mms.immowelt.de/b/9/0/8/b90816ac-23ac-4ee0-9b86-bd2022aab985.jpg?ci_seal=4627e7889816c716b116e999fba26ee0299d9db1",
				"description": "Markenbad mit Dusche oder Wanne",
				"title": "Markenbad mit Dusche oder Wanne",
				"ariaLabel": "Markenbad mit Dusche oder Wanne",
				"classification": {
					"name": "BATHROOM",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "88327f8b-02d8-439c-a523-c559722384cd",
				"url": "https://mms.immowelt.de/8/8/3/2/88327f8b-02d8-439c-a523-c559722384cd.jpg?ci_seal=a393f5757e5e15bfbd11ac181edca75433d3ebd8",
				"description": "Wohnbereich Musterstudio",
				"title": "Wohnbereich Musterstudio",
				"ariaLabel": "Wohnbereich Musterstudio",
				"classification": {
					"name": "LIVING_ROOM",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "24858eb5-015f-4f43-a595-530a482128a6",
				"url": "https://mms.immowelt.de/2/4/8/5/24858eb5-015f-4f43-a595-530a482128a6.jpg?ci_seal=1545a381a9c7e77a98b2ad2f272cd8f989c51094",
				"description": "Repräsentativer Eingangsbereich",
				"title": "Repräsentativer Eingangsbereich",
				"ariaLabel": "Repräsentativer Eingangsbereich",
				"classification": {
					"name": "HALLWAY",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "91bbf910-0a2a-4e94-ba2d-6d9d5dcbdb1a",
				"url": "https://mms.immowelt.de/9/1/b/b/91bbf910-0a2a-4e94-ba2d-6d9d5dcbdb1a.jpg?ci_seal=ee0f4e3143fd52f9acdec61da7709de5001e1a93",
				"description": "Fahrradabstellplätze mit Ladestation",
				"title": "Fahrradabstellplätze mit Ladestation",
				"ariaLabel": "Fahrradabstellplätze mit Ladestation",
				"classification": {
					"name": "EMPTY_ROOM",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			},
			{
				"key": "5fd09be9-9fda-403b-9611-31ed6a27a1d7",
				"url": "https://mms.immowelt.de/5/f/d/0/5fd09be9-9fda-403b-9611-31ed6a27a1d7.jpg?ci_seal=4979ccdfbddcafe8229dc10b931f21ae340697bd",
				"description": "Optionale Tiefgarage",
				"title": "Optionale Tiefgarage",
				"ariaLabel": "Optionale Tiefgarage",
				"classification": {
					"name": "GARAGE",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			}
		],
		"floorplans": [
			{
				"key": "48a9b4f3-5a43-4673-85a0-b257691d8ff3",
				"url": "https://mms.immowelt.de/4/8/a/9/48a9b4f3-5a43-4673-85a0-b257691d8ff3.jpg?ci_seal=e7564f6f911369e2c6f8d6e27cd00a8ff3b6f73d",
				"description": "Smyles_Grundriss_WE_306",
				"alt": "Wohnung zur Miete - Erstbezug 1.429 € 2 Zimmer 48,3 m² 5. Geschoss Friedenauer Höhe 14 Friedenau Berlin 12159",
				"title": "Smyles_Grundriss_WE_306",
				"ariaLabel": "Smyles_Grundriss_WE_306",
				"classification": {
					"name": "FLOORPLAN",
					"version": "scene-classification-sagemaker-endpoint-live-1-3-10"
				}
			}
		],
		"availableFeatures": {
			"floorplans": true,
			"virtualTours": true
		}
	},
	"tracking": {
		"name": "classified",
		"list_name": "classified_detail_similars_bottom",
		"id": "263ELWYT61N2",
		"price": 1429,
		"estate_type": "av_2",
		"distribution_type": "1",
		"country": "Germany",
		"city": "Berlin",
		"region": "Berlin",
		"province": "Berlin",
		"currency": "EUR",
		"zip_code": "12159",
		"building_state": "FIRST_TIME_USE",
		"legacy_id": "a88d2b01-3bff-4477-a526-db79c284d1bb",
		"product_type": "standard",
		"client_id": "1107086",
		"energy_certificate": "B"
	},
	"provider": {
		"intermediaryCard": {
			"title": "STRATEGIS AG",
			"subtitle": "Gewerblicher Anbieter",
			"display": true,
			"logoUrl": "https://mms.immowelt.de/b/f/2/1/bf213538-3e94-4549-9aef-a9063d983f6f.jpg?ci_seal=3b1d4022350df6c3ca4b9f8fb7eec7acb30acdfe",
			"logoHref": "https://www.immowelt.de/profil/9e54973f13ffde498cb2190efc8b9890"
		},
		"contactCard": {
			"title": "Stefan Prill",
			"subtitle": "Dein Kontakt",
			"display": true,
			"logoUrl": null
		},
		"website": "https://www.strategis.de/",
		"isPrivateOwner": false,
		"profileUrl": "https://www.immowelt.de/profil/9e54973f13ffde498cb2190efc8b9890",
		"imprintUrl": "https://www.immowelt.de/profil/9e54973f13ffde498cb2190efc8b9890#impressum",
		"agencyLegalInformations": [],
		"publisherType": "AGENCY",
		"displayLinks": true,
		"badge": {
			"title": "immowelt Partner",
			"imageUrl": "https://s.immowelt.org/shared/images/partner-badges/partner.svg"
		},
		"address": "Leipziger Straße 51, 10117 Berlin",
		"phoneNumbers": [
			"030 44353300"
		],
		"agencyStrip": {
			"agencyColor": "#1090d0",
			"fontColor": "#000000"
		}
	},
	"cardProvider": {
		"title": "Stefan Prill",
		"subtitle": "Dein Kontakt",
		"logoUrl": null,
		"agencyStrip": {
			"agencyColor": "#1090d0",
			"fontColor": "#000000"
		}
	},
	"energyClass": "B",
	"mainDescription": {
		"headline": "Smyles - tolle Neubauwohnung mit Südbalkon",
		"description": "Das neue Stadtquartier Smyles Berlin im Schöneberger Ortsteil Friedenau verfügt über fünf moderne Gebäude mit insgesamt 537 hellen 1- bis 3-Zimmer-Wohnungen zur Miete. Über acht Geschosse verteilen s...",
		"metadata": {
			"language": "de"
		}
	},
	"type": "PROFESSIONAL",
	"url": "https://www.immowelt.de/expose/a88d2b01-3bff-4477-a526-db79c284d1bb",
	"portal": "immowelt",
	"rawData": {
		"distributionType": "RENT",
		"propertyType": "APARTMENT",
		"geoIdHierarchy": [
			{
				"id": "NBH2DE91302024",
				"typeKey": "NBH2"
			},
			{
				"id": "AD09DE481",
				"typeKey": "AD09"
			},
			{
				"id": "AD08DE8634",
				"typeKey": "AD08"
			},
			{
				"id": "AD06DE326",
				"typeKey": "AD06"
			},
			{
				"id": "AD04DE11",
				"typeKey": "AD04"
			},
			{
				"id": "AD02DE1",
				"typeKey": "AD02"
			}
		],
		"price": 1619,
		"offererMarketingKey": "Smyles306",
		"providercity": "Berlin",
		"providerzipcode": "10117",
		"surface": {
			"main": 48.25,
			"plot": null
		},
		"nbroom": 2,
		"contactLocationEnabled": false
	},
	"tags": {
		"isExclusive": false,
		"has3DVisit": true,
		"hasBrokerageFee": false,
		"isNew": true
	},
	"display": "classified",
	"cps": "263ELWYT61N2"
}
````

- with data flattening enabled:

```json
{
	"brand": "immowelt",
	"cps": "263ELWYT61N2",
	"display": "classified",
	"hardFacts_facts": [
		{
			"label": "Zimmer",
			"splitValue": "2",
			"type": "numberOfRooms",
			"value": "2 Zimmer"
		},
		{
			"label": "m²",
			"splitValue": "48,3",
			"type": "livingSpace",
			"value": "48,3 m²"
		},
		{
			"label": "Geschoss",
			"splitValue": "5.",
			"type": "numberOfFloors",
			"value": "5. Geschoss"
		}
	],
	"hardFacts_keyfacts": [
		"2 Zimmer",
		"48,3 m²",
		"5. Geschoss"
	],
	"hardFacts_price_addition_value": "Kaltmiete",
	"hardFacts_price_additionalInformation": "Kaltmiete",
	"hardFacts_price_ariaLabel": "1429 €",
	"hardFacts_price_financialLink_href": "https://www.immowelt.de/immobilienfinanzierung-anfragen/?price=1429&originvariant=expose-hardfacts&zip=12159&city=Berlin&classifiedid=a88d2b01-3bff-4477-a526-db79c284d1bb&m=classified_detail_request_offer_find_financing_partners_step1",
	"hardFacts_price_financialLink_label": "Finanzierung anfragen",
	"hardFacts_price_financialLink_partnerName": "KFW",
	"hardFacts_price_formatted": "1.429 €",
	"hardFacts_price_value": "1.429 €",
	"hardFacts_prices": [
		{
			"ariaLabel": "1429 €",
			"label": "Kaltmiete",
			"value": "1.429 €"
		},
		{
			"ariaLabel": "1619 €",
			"label": "Warmmiete",
			"value": "1.619 €"
		}
	],
	"hardFacts_title": "Wohnung zur Miete - Erstbezug",
	"id": "263ELWYT61N2",
	"location_address_city": "Berlin",
	"location_address_country": "DEU",
	"location_address_district": "Friedenau",
	"location_address_street": "Friedenauer Höhe 14",
	"location_address_zipCode": "12159",
	"location_isAddressPublished": true,
	"mainDescription_description": "Das neue Stadtquartier Smyles Berlin im Schöneberger Ortsteil Friedenau verfügt über fünf moderne Gebäude mit insgesamt 537 hellen 1- bis 3-Zimmer-Wohnungen zur Miete. Über acht Geschosse verteilen s...",
	"mainDescription_headline": "Smyles - tolle Neubauwohnung mit Südbalkon",
	"mainDescription_metadata_language": "de",
	"metadata_creationDate": "2026-02-13T12:29:13.64Z",
	"metadata_id": "263ELWYT61N2",
	"metadata_legacyId": "a88d2b01-3bff-4477-a526-db79c284d1bb",
	"metadata_status_enrichments_contactSettings": false,
	"metadata_status_enrichments_geo": false,
	"metadata_status_enrichments_intermediary": false,
	"metadata_status_enrichments_media": false,
	"metadata_status_enrichments_onlineId": false,
	"metadata_status_status": true,
	"metadata_updateDate": "2026-02-13T12:29:29.936Z",
	"portal": "immowelt",
	"provider_address": "Leipziger Straße 51, 10117 Berlin",
	"provider_agencyLegalInformations": [],
	"provider_agencyStrip_agencyColor": "#1090d0",
	"provider_agencyStrip_fontColor": "#000000",
	"provider_badge_imageUrl": "https://s.immowelt.org/shared/images/partner-badges/partner.svg",
	"provider_badge_title": "immowelt Partner",
	"provider_contactCard_display": true,
	"provider_contactCard_logoUrl": null,
	"provider_contactCard_subtitle": "Dein Kontakt",
	"provider_contactCard_title": "Stefan Prill",
	"provider_displayLinks": true,
	"provider_imprintUrl": "https://www.immowelt.de/profil/9e54973f13ffde498cb2190efc8b9890#impressum",
	"provider_intermediaryCard_display": true,
	"provider_intermediaryCard_logoHref": "https://www.immowelt.de/profil/9e54973f13ffde498cb2190efc8b9890",
	"provider_intermediaryCard_logoUrl": "https://mms.immowelt.de/b/f/2/1/bf213538-3e94-4549-9aef-a9063d983f6f.jpg?ci_seal=3b1d4022350df6c3ca4b9f8fb7eec7acb30acdfe",
	"provider_intermediaryCard_subtitle": "Gewerblicher Anbieter",
	"provider_intermediaryCard_title": "STRATEGIS AG",
	"provider_isPrivateOwner": false,
	"provider_phoneNumbers": [
		"030 44353300"
	],
	"provider_profileUrl": "https://www.immowelt.de/profil/9e54973f13ffde498cb2190efc8b9890",
	"provider_publisherType": "AGENCY",
	"provider_website": "https://www.strategis.de/",
	"rawData_contactLocationEnabled": false,
	"rawData_distributionType": "RENT",
	"rawData_geoIdHierarchy": [
		{
			"id": "NBH2DE91302024",
			"typeKey": "NBH2"
		},
		{
			"id": "AD09DE481",
			"typeKey": "AD09"
		},
		{
			"id": "AD08DE8634",
			"typeKey": "AD08"
		},
		{
			"id": "AD06DE326",
			"typeKey": "AD06"
		},
		{
			"id": "AD04DE11",
			"typeKey": "AD04"
		},
		{
			"id": "AD02DE1",
			"typeKey": "AD02"
		}
	],
	"rawData_nbroom": 2,
	"rawData_offererMarketingKey": "Smyles306",
	"rawData_price": 1619,
	"rawData_propertyType": "APARTMENT",
	"rawData_providercity": "Berlin",
	"rawData_providerzipcode": "10117",
	"rawData_surface_main": 48.25,
	"rawData_surface_plot": null,
	"status": "Published",
	"tags_has3DVisit": true,
	"tags_hasBrokerageFee": false,
	"tags_isExclusive": false,
	"tags_isNew": true,
	"tracking_building_state": "FIRST_TIME_USE",
	"tracking_city": "Berlin",
	"tracking_client_id": "1107086",
	"tracking_country": "Germany",
	"tracking_currency": "EUR",
	"tracking_distribution_type": "1",
	"tracking_energy_certificate": "B",
	"tracking_estate_type": "av_2",
	"tracking_id": "263ELWYT61N2",
	"tracking_legacy_id": "a88d2b01-3bff-4477-a526-db79c284d1bb",
	"tracking_list_name": "classified_detail_similars_bottom",
	"tracking_name": "classified",
	"tracking_price": 1429,
	"tracking_product_type": "standard",
	"tracking_province": "Berlin",
	"tracking_region": "Berlin",
	"tracking_zip_code": "12159",
	"type": "PROFESSIONAL",
	"url": "https://www.immowelt.de/expose/a88d2b01-3bff-4477-a526-db79c284d1bb"
}
```

### 📬 Contact & Support

**Need a custom solution? Have a feature request?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

***

### ⚠️ Disclaimer

This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by AVIV Germany GmbH or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

# Actor input Schema

## `startUrl` (type: `string`):

Search results page URL

## `maxItems` (type: `integer`):

Maximum number of listings to scrape.

## `enableFlattening` (type: `boolean`):

If enabled, the actor will flatten the nested JSON output into a single level object for better readability and easier export to spreadsheets (e.g. CSV).

## Actor input object example

```json
{
  "startUrl": "https://www.immowelt.de/classified-search?distributionTypes=Buy,Buy_Auction&estateTypes=House,Apartment&locations=AD08DE6748&projectTypes=Investment",
  "maxItems": 2000,
  "enableFlattening": false
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
    "startUrl": "https://www.immowelt.de/classified-search?distributionTypes=Buy,Buy_Auction&estateTypes=House,Apartment&locations=AD08DE6748&projectTypes=Investment",
    "maxItems": 2000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/immowelt-de-search-results-scraper-by-search-url").call(input);

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
    "startUrl": "https://www.immowelt.de/classified-search?distributionTypes=Buy,Buy_Auction&estateTypes=House,Apartment&locations=AD08DE6748&projectTypes=Investment",
    "maxItems": 2000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/immowelt-de-search-results-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.immowelt.de/classified-search?distributionTypes=Buy,Buy_Auction&estateTypes=House,Apartment&locations=AD08DE6748&projectTypes=Investment",
  "maxItems": 2000
}' |
apify call azzouzana/immowelt-de-search-results-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/immowelt-de-search-results-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
