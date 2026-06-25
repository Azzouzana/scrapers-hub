# 🚀 LandWatch Scraper — Land Listings & Find an Agent (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the LandWatch Scraper — Land Listings & Find an Agent (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/landwatch-com-scraper-pro-by-search-url?fpr=cbgdsf)

---

## LandWatch Scraper — Land Listings & Find an Agent (By Search URL)

### ⚡ Features

This scraper supports **two kinds of searches** on LandWatch - the same URLs you already use in your browser:

1. **Land for sale** - browse/search results for listings.  
2. **Find an Agent** - broker/agent directory results by location or by name.

#### **🚀 Key Features**

* **Comprehensive Details:** **150+ data points** per item! Scrapes price, acreage, and full location (City, County, ZIP). Beyond the basics, capture agent socials, sales history, property types, full descriptions, media, and much more.

* **Massive Scale:** Bypasses website caps to retrieve thousands of results per run.

* **High Speed:** Built for speed first—because time is money. ⚡

* **Structured Output:** Export to **JSON** or **CSV**, or integrate the API directly into your own applications, AI, or LLM workflows. 🛠️

* **Cost-Effective:** Professional-grade results for a price cheaper than your cup of coffee. ☕


### 🛠️ How to use this actor

1. [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf)  -  no credit card required.  
2. Open the actor, fill in **Input**, and start a run.  
3. Try the free tier first to see if the fields match what you need.  

You need a **`startUrl`**: open LandWatch in your browser, go to the results you want, and copy the address bar URL.

- Must be on **landwatch.com**  
- **Land listings  -  examples:**  
  - `https://www.landwatch.com/texas-land-for-sale/price-under-6000`  
  - `https://www.landwatch.com/nebraska-land-for-sale/farms-ranches/price-250000-499999`  
- **Find an Agent  -  examples:**  
  - `https://www.landwatch.com/find-agent/austin-county-t/`  
  - `https://www.landwatch.com/find-agent/name/john/`

Page numbers in the link don’t matter for either mode - the actor pages until it hits **maxItems** or built-in safety limits. For huge markets, **narrow your filters** on LandWatch (area, price, type, etc.) or split the work across multiple runs or URLs.

### 💰 Cost of usage

**$1 per 1,000 dataset rows** scraped (each listing or broker row counts the same). No hidden fees.

| Rows scraped | Cost |
| -------: | ---: |
| 250 | ~$0.25 |
| 1,000 | ~$1.00 |

### 🆓 Free tier limitations

So everyone can try it fairly, **free accounts** usually get:

- **Sample size:** up to **5 rows** per run  -  enough to check quality (listings or agents).  
- **Daily cap:** **5 runs** per calendar day (UTC).  
- **Cooldown:** about **30 minutes** between runs.  

> Exact limits for free users can change with platform load.

Subscribe to a **paid plan** to lift those limitations. See [Apify pricing](https://apify.com/pricing?fpr=cbgdsf).

### 📥 Input

| Field | Type | Description | Example |
| ----- | ---- | ----------- | ------- |
| `startUrl` | Text | Land browse URL **or** Find an Agent URL (`/find-agent/…` or `/find-agent/name/…`) | `https://www.landwatch.com/illinois-land-for-sale/` or `https://www.landwatch.com/find-agent/austin-county-t/` |
| `maxItems` | Number | How many unique rows to collect **per run** (up to 2.5K for lands search and up to 3K for agents search).  | `50` |
| `fetchSellerAgentDetails` | On / off | **Optional.** Off by default (fastest runs). On: fills in **full agent/seller profiles** the same way for **land listings** and **Find an Agent**. | `false` |

### 📦 Output

Each listing or agent scraped is pushed as a dataset item. Output shapes below:

**Land listing** example shape:

```json
{
	"id": 21197003,
	"acres": 146,
	"acresDisplay": "146 acres",
	"address": "2801 Putter Drive",
	"auctionDate": "0001-01-01T00:00:00",
	"baths": 0,
	"bathsDisplay": "",
	"beds": 0,
	"bedsDisplay": "",
	"brokerCanonicalUrl": "/profile/brandon-swartzlander/175195",
	"brokerCompany": "Midwest Farm & Land Co. LLC",
	"brokerName": "Brandon Swartzlander",
	"brokerPhone": "(618) 322-1675",
	"canonicalUrl": "https://www.landwatch.com/marion-county-illinois-commercial-property-for-sale/pid/420602491",
	"city": "Centralia",
	"companyLogoDocumentId": 3791814522,
	"county": "Marion County",
	"countyLabel": "County",
	"description": "A premier 18-hole golf destination with modern amenities, lakeside dining, and event facilities offering excellent investment and growth potential.",
	"encodedBoundaryPoints": "",
	"executiveSummary": null,
	"externalSourceId": null,
	"halfBaths": 0,
	"halfBathsDisplay": null,
	"hasCustomMap": true,
	"hasExteriorMatterport": false,
	"hasHouse": false,
	"hasVideo": false,
	"hasVirtualTour": false,
	"homesqft": 0,
	"homesqftDisplay": "",
	"imageAltTextDisplay": "Land for sale in Marion County, Illinois",
	"imageCount": 45,
	"imageUrls": [
		"https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5836253734",
		"..."
	],
	"insertDate": "2024-08-13T11:00:04.67",
	"isALC": false,
	"isCourtesy": false,
	"isDiamond": true,
	"isFirstFreeListing": false,
	"isGold": false,
	"isLiked": false,
	"isPlatinum": false,
	"isShowcase": false,
	"lake": null,
	"lastUpdated": "2026-01-21T12:35:09.837",
	"latitude": 38.51763,
	"listHubListingKey": null,
	"listingLevel": 30,
	"listingLevelTitle": "Signature Partner",
	"longitude": -89.08795,
	"onMarketDate": "0001-01-01T00:00:00",
	"price": 2900000,
	"priceChangeAmount": 0,
	"priceChangeDate": "0001-01-01T00:00:00",
	"priceChangePercentage": 0,
	"priceDisplay": "$2,900,000",
	"pricePerAcre": 19863.01,
	"propertyTypes": 64,
	"propertyTypesLabel": "Commercial Property",
	"salesDate": "0001-01-01T00:00:00",
	"salesPrice": 0,
	"shortPrice": "$2.9M",
	"shortPriceChangeAmount": "$0",
	"state": "Illinois",
	"stateAbbreviation": "IL",
	"stateCode": "IL",
	"status": 1,
	"title": "Lakeside Golf Paradise",
	"types": [
		"Commercial Property"
	],
	"url": "https://www.landwatch.com/marion-county-illinois-commercial-property-for-sale/pid/420602491",
	"zip": "62801"
}
````

**Agent** example shape:

```json
{
	"id": 3616,
	"accountId": 3616,
	"accountSubTypeId": 4,
	"accountType": 41,
	"active": true,
	"adDesc": "",
	"address1": "5833 CR 531",
	"address2": "",
	"alcAdvancedCertified": false,
	"alcCertified": false,
	"badgeId": 3759625769,
	"canonicalUrl": "https://www.landwatch.com/profile/texas-ranch-sales-llc/3616",
	"city": "Hondo",
	"companyAddress1": "920 Main Street",
	"companyAddress2": "",
	"companyCity": "Boerne",
	"companyName": "Texas Ranch Sales, LLC",
	"companyState": "TX",
	"companyZip": "78006",
	"contactName": "Texas Ranch Sales, LLC",
	"courtesyListingCount": 0,
	"description": [
		"Texas Ranch Sales brokers and represents ..."
	],
	"details_accountId": 3616,
	"details_accountSubTypeId": 4,
	"details_accountType": 41,
	"details_active": true,
	"details_adDesc": "",
	"details_address1": "5833 CR 531",
	"details_address2": "",
	"details_alcAdvancedCertified": false,
	"details_alcCertified": false,
	"details_badgeId": 3759625769,
	"details_canonicalUrl": "/profile/texas-ranch-sales-llc/3616",
	"details_city": "Hondo",
	"details_companyAddress1": "920 Main Street",
	"details_companyAddress2": "",
	"details_companyCity": "Boerne",
	"details_companyName": "Texas Ranch Sales, LLC",
	"details_companyState": "TX",
	"details_companyZip": "78006",
	"details_contactName": "Texas Ranch Sales, LLC",
	"details_courtesyListingCount": 0,
	"details_description": [
		"Texas Ranch Sales brokers and represents ..."
	],
	"details_email": null,
	"details_expirationDate": "2026-09-21T00:00:00",
	"details_homesContactId": "0",
	"details_homesUserId": null,
	"details_inCityStateSeoText": " in Boerne, TX",
	"details_insertDate": "2006-04-18T12:10:28.243",
	"details_isFree": false,
	"details_isSeller": true,
	"details_landStarAwards": [
		{
			"quarter": 0,
			"year": 2023
		},
		{
			"quarter": 1,
			"year": 2023
		},
		{
			"quarter": 2,
			"year": 2023
		},
		{
			"quarter": 3,
			"year": 2023
		},
		{
			"quarter": 4,
			"year": 2023
		},
		{
			"quarter": 0,
			"year": 2024
		},
		{
			"quarter": 1,
			"year": 2024
		},
		{
			"quarter": 2,
			"year": 2024
		},
		{
			"quarter": 3,
			"year": 2024
		},
		{
			"quarter": 4,
			"year": 2024
		},
		{
			"quarter": 0,
			"year": 2025
		},
		{
			"quarter": 1,
			"year": 2025
		},
		{
			"quarter": 2,
			"year": 2025
		},
		{
			"quarter": 3,
			"year": 2025
		},
		{
			"quarter": 4,
			"year": 2025
		}
	],
	"details_landStarWinCount": 0,
	"details_leadRoutingEmail": null,
	"details_licenseNumber": "",
	"details_listingCount": 0,
	"details_logoId": 2703760373,
	"details_optInLeadTargeting": true,
	"details_otherListings": [
		{
			"imageAltTextDisplay": "Land for sale in Austin County, Texas",
			"id": 23838194,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/austin-county-texas-farms-and-ranches-for-sale/pid/423242690",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5566216281"
		},
		{
			"imageAltTextDisplay": "Land for sale in Gillespie County, Texas",
			"id": 24351761,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/gillespie-county-texas-farms-and-ranches-for-sale/pid/423756257",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5652279667"
		},
		{
			"imageAltTextDisplay": "Land for sale in Grayson County, Texas",
			"id": 26943713,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/grayson-county-texas-farms-and-ranches-for-sale/pid/426348208",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-6114627958"
		},
		{
			"imageAltTextDisplay": "Land for sale in Val Verde County, Texas",
			"id": 22068675,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/val-verde-county-texas-farms-and-ranches-for-sale/pid/421473173",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5350985465"
		}
	],
	"details_parentAccountId": 0,
	"details_parentAccountType": 0,
	"details_phoneNumbers_associatedAccountId": 3616,
	"details_phoneNumbers_associatedListingId": 0,
	"details_phoneNumbers_cellPhone": "",
	"details_phoneNumbers_fax": "",
	"details_phoneNumbers_listingPhone": null,
	"details_phoneNumbers_officePhone": "(830) 741-8906",
	"details_phoneNumbers_partnerPhone": null,
	"details_phoneNumbers_preferredPhone": "(830) 741-8906",
	"details_phoneNumbers_tollFree": "",
	"details_phoneNumbers_tpnForAccount": null,
	"details_phoneNumbers_tpnForListing": null,
	"details_portraitId": 3832720652,
	"details_portraitImageUpdateDate": null,
	"details_routeContext_component": "SellerDetails",
	"details_routeContext_financeCenter": null,
	"details_routeContext_isDiamondListing": false,
	"details_routeContext_locationId": 0,
	"details_routeContext_locationName": null,
	"details_routeContext_locationType": 0,
	"details_routeContext_pageType": "BrokerDetailsPage",
	"details_routeContext_pageTypeGA": "Seller Details",
	"details_routeContext_urlKey": "/profile/texas-ranch-sales-llc/3616",
	"details_sellerCarouselListings": [
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 23838194,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423242690",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5566216281"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24351761,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423756257",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5652279667"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Oklahoma",
			"id": 25465863,
			"price": 1050000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-oklahoma-farms-and-ranches-for-sale/pid/424870359",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5825751076"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24654277,
			"price": 650000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/424058773",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5704726062"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24506234,
			"price": 127855,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423910730",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5676535343"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 27089296,
			"price": 3900000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/426493791",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-6146174261"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 25501228,
			"price": 710000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/424905724",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5832686551"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 27089290,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/426493785",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-6146174218"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 23763906,
			"price": 846900,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423168402",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5555827733"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24447975,
			"price": 475000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423852471",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5666344742"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24670916,
			"price": 874900,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/424075412",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5706979522"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 21985673,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/421390171",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5345660440"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 27101301,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/426505796",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-6148521007"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24770295,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/424174791",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5724957526"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Oklahoma",
			"id": 26327758,
			"price": 2100000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-oklahoma-farms-and-ranches-for-sale/pid/425732253",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5997398411"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 26808007,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/426212502",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-6089671867"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 22068675,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/421473173",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5350985465"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 23546782,
			"price": 425000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/422951278",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5526324865"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 25509822,
			"price": 1050000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/424914318",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5834403271"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24712111,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/424116607",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5715881757"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24088933,
			"price": 1995000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423493429",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5606923920"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 23635702,
			"price": 1100000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423040198",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5537951694"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 26327932,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/425732427",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5997419006"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 23450669,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/422855165",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5514639486"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 22786928,
			"price": 2990000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/422191424",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5433757106"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 25705811,
			"price": 1282500,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/425110307",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5876033148"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 25605401,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/425009897",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5852170184"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 21736721,
			"price": 1850000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/421141219",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5324772881"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24506226,
			"price": 700000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423910722",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5676534695"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 18061060,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/417467538",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5045897161"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 20045745,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/419452223",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5224221176"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 23545582,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/422950078",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5526228470"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Oregon",
			"id": 14205748,
			"price": 15000000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-oregon-farms-and-ranches-for-sale/pid/413612230",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-4044809863"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 21842117,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/421246615",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5333951561"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 21126119,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/420531607",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5281668575"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 21079512,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/420485000",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5279015269"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 19987857,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/419394335",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5220835373"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Oregon",
			"id": 14204376,
			"price": 20000000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-oregon-farms-and-ranches-for-sale/pid/413610858",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-4044769595"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 18427760,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/417834238",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5071082204"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 22085780,
			"price": 285000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/421490278",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5352121299"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , New Mexico",
			"id": 22346210,
			"price": 4000000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-new-mexico-farms-and-ranches-for-sale/pid/421750706",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5379762152"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24766751,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/424171247",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5724836504"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 25900138,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/425304634",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5923152441"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 21093238,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/420498726",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5279794675"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 21079622,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/420485110",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5279020354"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 27101296,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/426505791",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-6148503737"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 22207449,
			"price": 1395000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/421611947",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5360626990"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24602188,
			"price": 295000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/424006684",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5694426959"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 23723906,
			"price": 949000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423128402",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5550586175"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 22085498,
			"price": 3950000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/421489996",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5352079339"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24544084,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423948580",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5682321052"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24475589,
			"price": 1061400,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423880085",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5670121570"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 22641741,
			"price": 470000,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/422046237",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5415885528"
		},
		{
			"imageAltTextDisplay": "Farm and Ranch for sale in  , Texas",
			"id": 24118436,
			"price": 1,
			"status": 1,
			"canonicalUrl": "https://www.landwatch.com/-texas-farms-and-ranches-for-sale/pid/423522932",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5610389034"
		}
	],
	"details_sellerId": 3616,
	"details_sellerListingStats_activeAcreageMax": 0,
	"details_sellerListingStats_activeAcreageMin": 0,
	"details_sellerListingStats_activeListingCount": 0,
	"details_sellerListingStats_activePriceMax": 0,
	"details_sellerListingStats_activePriceMin": 0,
	"details_sellerListingStats_allTimeAcreageMax": 87819,
	"details_sellerListingStats_allTimeAcreageMin": 0.2,
	"details_sellerListingStats_allTimeListingCount": 1739,
	"details_sellerListingStats_allTimePriceMax": 35000000,
	"details_sellerListingStats_allTimePriceMin": 10000,
	"details_sellerListingStats_lastFiveYearsAcreageMax": 87819,
	"details_sellerListingStats_lastFiveYearsAcreageMin": 0.2,
	"details_sellerListingStats_lastFiveYearsListingCount": 937,
	"details_sellerListingStats_lastFiveYearsPriceMax": 35000000,
	"details_sellerListingStats_lastFiveYearsPriceMin": 10000,
	"details_sellerListingStats_lastTenYearsAcreageMax": 87819,
	"details_sellerListingStats_lastTenYearsAcreageMin": 0.2,
	"details_sellerListingStats_lastTenYearsListingCount": 1280,
	"details_sellerListingStats_lastTenYearsPriceMax": 35000000,
	"details_sellerListingStats_lastTenYearsPriceMin": 10000,
	"details_sellerListingStats_lastThreeYearsAcreageMax": 87819,
	"details_sellerListingStats_lastThreeYearsAcreageMin": 0.2,
	"details_sellerListingStats_lastThreeYearsListingCount": 559,
	"details_sellerListingStats_lastThreeYearsPriceMax": 25900000,
	"details_sellerListingStats_lastThreeYearsPriceMin": 66500,
	"details_sellerMedia_Facebook_active": 1,
	"details_sellerMedia_Facebook_isVideo": false,
	"details_sellerMedia_Facebook_mediaId": "TexasRanchSalesLLC",
	"details_sellerMedia_Facebook_mediaThumbnail": null,
	"details_sellerMedia_Facebook_mediaTypeId": 4,
	"details_sellerMedia_Facebook_mediaUrl": "https://www.facebook.com/TexasRanchSalesLLC",
	"details_sellerMedia_Facebook_oEmbedResponse": null,
	"details_sellerMedia_Facebook_providerId": 5,
	"details_sellerMedia_Instagram_active": 1,
	"details_sellerMedia_Instagram_isVideo": false,
	"details_sellerMedia_Instagram_mediaId": "texasranchsalesllc/",
	"details_sellerMedia_Instagram_mediaThumbnail": null,
	"details_sellerMedia_Instagram_mediaTypeId": 4,
	"details_sellerMedia_Instagram_mediaUrl": "https://www.instagram.com/texasranchsalesllc/",
	"details_sellerMedia_Instagram_oEmbedResponse": null,
	"details_sellerMedia_Instagram_providerId": 6,
	"details_sellerMedia_Linkedin_active": 1,
	"details_sellerMedia_Linkedin_isVideo": false,
	"details_sellerMedia_Linkedin_mediaId": "company/texasranchsales",
	"details_sellerMedia_Linkedin_mediaThumbnail": null,
	"details_sellerMedia_Linkedin_mediaTypeId": 4,
	"details_sellerMedia_Linkedin_mediaUrl": "https://www.linkedin.com/company/texasranchsales",
	"details_sellerMedia_Linkedin_oEmbedResponse": null,
	"details_sellerMedia_Linkedin_providerId": 4,
	"details_smsNotifications": false,
	"details_soldListings": [
		{
			"imageAltTextDisplay": "Land in Edwards County, Texas",
			"id": 16907716,
			"price": 1075000,
			"status": 4,
			"canonicalUrl": "https://www.landwatch.com/edwards-county-texas-farms-and-ranches-for-sale/pid/416314194",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5142073299"
		},
		{
			"imageAltTextDisplay": "Land in Walker County, Texas",
			"id": 19729439,
			"price": 1,
			"status": 4,
			"canonicalUrl": "https://www.landwatch.com/walker-county-texas-farms-and-ranches-for-sale/pid/419135917",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5205085384"
		},
		{
			"imageAltTextDisplay": "Land in Grimes County, Texas",
			"id": 19236225,
			"price": 1,
			"status": 4,
			"canonicalUrl": "https://www.landwatch.com/grimes-county-texas-farms-and-ranches-for-sale/pid/418642703",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5162253304"
		},
		{
			"imageAltTextDisplay": "Land in Collin County, Texas",
			"id": 16680442,
			"price": 1,
			"status": 4,
			"canonicalUrl": "https://www.landwatch.com/collin-county-texas-farms-and-ranches-for-sale/pid/416086920",
			"imageUrl": "https://assets.landwatch.com/resizedimages/0/1920/w/80/w/1-5000885517"
		}
	],
	"details_stateAbbreviation": "TX",
	"details_stripeCustomerId": null,
	"details_tierListingCount": 0,
	"details_totalRows": 0,
	"details_upgradeListingCount": 0,
	"details_uploadedSellerFiles": [],
	"details_url": "www.texasranchsalesllc.com",
	"details_zip": "78861",
	"email": null,
	"expirationDate": null,
	"homesContactId": null,
	"homesUserId": null,
	"inCityStateSeoText": " in Boerne, TX",
	"insertDate": null,
	"isFree": false,
	"isSeller": false,
	"landStarWinCount": 5,
	"leadRoutingEmail": null,
	"licenseNumber": "",
	"listingCount": 0,
	"logoUrl": "https://assets.landwatch.com/resizedimages/150/150/l/80/w/1-2703760373",
	"optInLeadTargeting": true,
	"parentAccountId": 0,
	"parentAccountType": 0,
	"phoneNumbers": {
		"associatedAccountId": 3616,
		"associatedListingId": 0,
		"cellPhone": "",
		"fax": "",
		"listingPhone": null,
		"officePhone": "(830) 741-8906",
		"partnerPhone": null,
		"tollFree": "",
		"tpnForAccount": null,
		"tpnForListing": null,
		"preferredPhone": "(830) 741-8906"
	},
	"portraitImageUpdateDate": null,
	"portraitUrl": "https://assets.landwatch.com/resizedimages/150/150/l/80/w/1-3832720652",
	"sellerListingStats": {
		"activePriceMin": 127855,
		"activePriceMax": 20000000,
		"activeAcreageMin": 7,
		"activeAcreageMax": 26820,
		"activeListingCount": 130,
		"allTimePriceMin": 0,
		"allTimePriceMax": 0,
		"allTimeAcreageMin": 0,
		"allTimeAcreageMax": 0,
		"allTimeListingCount": 0,
		"lastThreeYearsPriceMin": 0,
		"lastThreeYearsPriceMax": 0,
		"lastThreeYearsAcreageMin": 0,
		"lastThreeYearsAcreageMax": 0,
		"lastThreeYearsListingCount": 0,
		"lastFiveYearsPriceMin": 0,
		"lastFiveYearsPriceMax": 0,
		"lastFiveYearsAcreageMin": 0,
		"lastFiveYearsAcreageMax": 0,
		"lastFiveYearsListingCount": 0,
		"lastTenYearsPriceMin": 0,
		"lastTenYearsPriceMax": 0,
		"lastTenYearsAcreageMin": 0,
		"lastTenYearsAcreageMax": 0,
		"lastTenYearsListingCount": 0
	},
	"smsNotifications": false,
	"stateAbbreviation": "TX",
	"stripeCustomerId": null,
	"tierListingCount": 0,
	"totalRows": 0,
	"upgradeListingCount": 0,
	"url": "https://www.landwatch.com/profile/texas-ranch-sales-llc/3616",
	"zip": "78861"
}
```

### ⚠️ Limitations

- **Lands search:** up to **2,500** unique listings per run; narrow big markets (county, price, acreage, type) or split across URLs/runs - otherwise, feel free to reach out to us for large-scale scraping.
- **Agents search:**  up to **3,000** per run. Very large markets may not yield every profile you expect in one go - use **narrower search filters** or split across URLs/runs - otherwise, feel free to reach out to us for large-scale scraping.
- LandWatch may change their site; if something breaks, message us.
- This tool only uses **public** data visible on the site.

### 🔍 SEO keywords

landwatch, LandWatch, landwatch scraper, landwatch.com, landwatch.com scraper, scrape landwatch, landwatch data, landwatch listings, landwatch land for sale, landwatch find agent, landwatch agents, landwatch brokers, landwatch export, landwatch CSV, landwatch JSON, Apify landwatch, landwatch API alternative, landwatch automation

#### 📞 Contact us

**Need a custom solution, a tweak for your workflow, or just want to say hi?**

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

### ⚖️ Disclaimer

This actor is an **independent tool**, not affiliated with or endorsed by LandWatch or its owners. Trademarks belong to their owners.

# Actor input Schema

## `startUrl` (type: `string`):

Paste the land or agent search URLs

## `maxItems` (type: `integer`):

How many unique lands or agents to collect from this search URL

## `fetchSellerAgentDetails` (type: `boolean`):

Turn on to add fuller seller or agents/broker profile fields (contacts, socials, sales history, etc.)

## Actor input object example

```json
{
  "startUrl": "https://www.landwatch.com/texas-land-for-sale/price-under-6000",
  "maxItems": 10,
  "fetchSellerAgentDetails": false
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
    "startUrl": "https://www.landwatch.com/texas-land-for-sale/price-under-6000",
    "maxItems": 10
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/landwatch-com-scraper-pro-by-search-url").call(input);

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
    "startUrl": "https://www.landwatch.com/texas-land-for-sale/price-under-6000",
    "maxItems": 10,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/landwatch-com-scraper-pro-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.landwatch.com/texas-land-for-sale/price-under-6000",
  "maxItems": 10
}' |
apify call azzouzana/landwatch-com-scraper-pro-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/landwatch-com-scraper-pro-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
