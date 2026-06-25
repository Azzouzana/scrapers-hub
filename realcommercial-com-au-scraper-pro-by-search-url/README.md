# 🚀 Realcommercial.com.au Scraper — Sale, Lease, Sold & Leased (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Realcommercial.com.au Scraper — Sale, Lease, Sold & Leased (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/realcommercial-com-au-scraper-pro-by-search-url?fpr=cbgdsf)

---

## Realcommercial.com.au Scraper — Sale, Lease, Sold & Leased (By Search URL)

### Features

Our **realcommercial.com.au** search scraper pulls commercial property listings from a search URL and saves them as JSON, CSV, and more ⚡ for less than a coffee.

Paste your search link, set how many listings you want, and run. Each listing includes address, price, photos, description, highlights, agency/agent details (email & phone when available) and more.

Supports **for-sale**, **for-lease**, **sold**, and **leased** search results.

### How to use this actor 🚀

1. [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required.
2. Open the actor, add your **Input**, and start a run.
3. Use the free tier to see if the output fits your project before scaling up.

The scraper needs a **`startUrl`**: a search URL from realcommercial.com.au with your filters applied in the browser.

- Starts with: `https://www.realcommercial.com.au/for-sale/` (or `for-lease`, `sold`, `leased`)
- Example: `https://www.realcommercial.com.au/for-sale/melbourne-vic-3000/?activeSort=date-desc&includePropertiesWithin=includesurrounding`

### Cost of usage

**$1 per 1,000 listings** scraped. No hidden fees.

| Listings | Cost |
| -------: | ---: |
| 100 | ~$0.1 |
| 1,000 | ~$1.00 |
| 5,000 | ~$5.00 |
| 10,000 | ~$10.00 |

### Free tier

- Up to **5 listings** per run
- ~**5 runs** per day (UTC)
- ~**30 min** cooldown between runs

A **paid plan** lifts those caps. [Apify pricing](https://apify.com/pricing?fpr=cbgdsf).

### Input

| Field | Type | Description | Example |
| ----- | ---- | ----------- | ------- |
| `startUrl` | `string` | Search URL from realcommercial.com.au | `https://www.realcommercial.com.au/for-sale/...` |
| `maxItems` | `number` | Listings to collect | `10` |

### Output

Each dataset row is one listing. Example:

```json
{
    "id": "504962068",
    "availableChannels": [
        "LEASE"
    ],
    "propertyTypes": [
        "OFFICES"
    ],
    "product": "ELITE_PLUS",
    "media": [
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/cde2a65a6811050c66fbe937ae54fdd7a87be0de37a784a4d769caa00c248f96/image0.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/cde2a65a6811050c66fbe937ae54fdd7a87be0de37a784a4d769caa00c248f96/image0.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/cde2a65a6811050c66fbe937ae54fdd7a87be0de37a784a4d769caa00c248f96/image0.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 1"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/4579d044fd17437b9e10e0608f3dbc63242cc78ffaf04a3a5ee35dd085b35493/image1.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/4579d044fd17437b9e10e0608f3dbc63242cc78ffaf04a3a5ee35dd085b35493/image1.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/4579d044fd17437b9e10e0608f3dbc63242cc78ffaf04a3a5ee35dd085b35493/image1.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 2"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/7d4ee2f0b10268670b9a078b058fd10b4dff19d9b0971126b0e7a09be3061d25/image2.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/7d4ee2f0b10268670b9a078b058fd10b4dff19d9b0971126b0e7a09be3061d25/image2.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/7d4ee2f0b10268670b9a078b058fd10b4dff19d9b0971126b0e7a09be3061d25/image2.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 3"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/e4173ca3ee1caaf041e3a39c871677b5286a9aa71569db87d3ea54d97cd45a82/image3.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/e4173ca3ee1caaf041e3a39c871677b5286a9aa71569db87d3ea54d97cd45a82/image3.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/e4173ca3ee1caaf041e3a39c871677b5286a9aa71569db87d3ea54d97cd45a82/image3.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 4"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/7a1261f8cca749ce8bb029950a8dac99a73845ce3ba1bea16038a7ead58637e8/image4.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/7a1261f8cca749ce8bb029950a8dac99a73845ce3ba1bea16038a7ead58637e8/image4.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/7a1261f8cca749ce8bb029950a8dac99a73845ce3ba1bea16038a7ead58637e8/image4.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 5"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/7dcd54a55bce90a8a032aceef1e4cdf9d348128e1993f7314d62cf9e46a09248/image5.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/7dcd54a55bce90a8a032aceef1e4cdf9d348128e1993f7314d62cf9e46a09248/image5.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/7dcd54a55bce90a8a032aceef1e4cdf9d348128e1993f7314d62cf9e46a09248/image5.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 6"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/06d4f945956ff39a1db9647f703c8e508d7fa71eb207ceb8382e2d0401ac9f3d/image6.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/06d4f945956ff39a1db9647f703c8e508d7fa71eb207ceb8382e2d0401ac9f3d/image6.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/06d4f945956ff39a1db9647f703c8e508d7fa71eb207ceb8382e2d0401ac9f3d/image6.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 7"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/ad53f55ec1541d0d6f6cf09e07fa5cdf7e6e3a5fa9d3d4139e26f8c81900fea6/image7.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/ad53f55ec1541d0d6f6cf09e07fa5cdf7e6e3a5fa9d3d4139e26f8c81900fea6/image7.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/ad53f55ec1541d0d6f6cf09e07fa5cdf7e6e3a5fa9d3d4139e26f8c81900fea6/image7.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 8"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/cef1ec16b35da24052c599abb61ec9fb0564bbff53ed7b3c8b69380c101c248f/image8.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/cef1ec16b35da24052c599abb61ec9fb0564bbff53ed7b3c8b69380c101c248f/image8.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/cef1ec16b35da24052c599abb61ec9fb0564bbff53ed7b3c8b69380c101c248f/image8.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 9"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/3b7c9f66060e113284fb25371c44e4812f5ece663e79b5ee5820de2f9ec81e8c/image9.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/3b7c9f66060e113284fb25371c44e4812f5ece663e79b5ee5820de2f9ec81e8c/image9.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/3b7c9f66060e113284fb25371c44e4812f5ece663e79b5ee5820de2f9ec81e8c/image9.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 10"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/ad928e56c51a32834f36bedaec9d3c1def6486ed23f848c1752b417b08879a7a/image10.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/ad928e56c51a32834f36bedaec9d3c1def6486ed23f848c1752b417b08879a7a/image10.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/ad928e56c51a32834f36bedaec9d3c1def6486ed23f848c1752b417b08879a7a/image10.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 11"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/1cb3abafa9c02611173c0fea3bd23fae31124332519d7f22e211cea617977957/image11.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/1cb3abafa9c02611173c0fea3bd23fae31124332519d7f22e211cea617977957/image11.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/1cb3abafa9c02611173c0fea3bd23fae31124332519d7f22e211cea617977957/image11.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 12"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/e9a2ed20aedb8958db9dc9ebe7379d97c308bd722d537bc51449179efc795a74/image12.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/e9a2ed20aedb8958db9dc9ebe7379d97c308bd722d537bc51449179efc795a74/image12.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/e9a2ed20aedb8958db9dc9ebe7379d97c308bd722d537bc51449179efc795a74/image12.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 13"
        },
        {
            "type": "PHOTO",
            "detailUrl": "https://i1.au.reastatic.net/800x533-smart=85,r=33,g=40,b=46/fc57ac19186081825601f7fca2872785686d8f6ef89eaa5de6760e0adfccedce/image13.jpg",
            "galleryUrl": "https://i1.au.reastatic.net/1200x900-smart=80,r=33,g=40,b=46/fc57ac19186081825601f7fca2872785686d8f6ef89eaa5de6760e0adfccedce/image13.jpg",
            "thumbnailUrl": "https://i1.au.reastatic.net/400x300-smart=80,r=33,g=40,b=46/fc57ac19186081825601f7fca2872785686d8f6ef89eaa5de6760e0adfccedce/image13.jpg",
            "alt": "474 Flinders Street Melbourne VIC 3000 - Image 14"
        }
    ],
    "video": null,
    "address": {
        "street": "474 Flinders Street",
        "suburb": "Melbourne",
        "state": "VIC",
        "postcode": "3000",
        "latitude": -37.81988763,
        "longitude": 144.95829489,
        "marketingRegion": "melbourne_city___greater_region"
    },
    "description": "A rare chance to secure 9B certified education space at Level 9, 474 Flinders Street. Conveniently located between Flinders Street and Southern Cross Stations both being short walks away, the building offers excellent access with major tram, and bus networks at the doorstep ensuring effortless travel for students and staff to commute from across Melbourne CBD and Metropolitan locations.\r\n\r\nLevel 9 (359sqm) features an existing fitout comprising of 11 Classrooms, 2 Meeting room/Private offices, Reception/Waiting area, and Kitchen area.\r\n\r\nThe Tenancy benefits from great views and natural light, and is surrounded by a wide range of premium amenities including popular Melbourne cafes, restaurants, and retail options attracting foot traffic to the precinct.\r\n\r\n474 Flinders Street presents an amazing solution for education providers with flexible configuration and space primed for education use.\r\n\r\nFor further information or to arrange an inspection, please contact the appointed Colliers agents",
    "highlights": [
        "9B Ready",
        "Excellent Transport Connectivity",
        "Existing Education Fitout"
    ],
    "headline": "Rare Opportunity - 9B Certified Education Space",
    "lastUpdatedDate": "2025-10-09T00:02:12Z",
    "listDate": "2025-09-19",
    "daysActive": null,
    "tours": [],
    "threeDimensionalTours": [],
    "status": null,
    "agencies": [
        {
            "id": "CXXSIC",
            "name": "Colliers - Melbourne",
            "address": {
                "street": "Level 30, 367 Collins Street",
                "suburb": "MELBOURNE",
                "state": "VIC",
                "postcode": "3000",
                "latitude": null,
                "longitude": null
            },
            "phone": {
                "display": "03 9629 8888",
                "dial": "+61396298888"
            },
            "brandingColor": "#25408f",
            "logoUrl": "https://i1.au.reastatic.net/84x63-fit/34229594904b963f0d733600ae1d2806ce327c663109786938165bd5b0f3cbfb/large_commercial.jpg",
            "enquiryUrl": "https://api.realcommercial.com.au/mobile/enquiries/504962068/CXXSIC",
            "agents": [
                {
                    "id": "3743660",
                    "name": "Tommy McRae",
                    "email": "Tommy.McRae@colliers.com",
                    "phone": {
                        "display": "0429112783",
                        "dial": "+61429112783"
                    },
                    "enquiryUrl": "https://api.realcommercial.com.au/mobile/enquiries/504962068/CXXSIC",
                    "photoUrl": "https://i1.au.reastatic.net/142x176/c27efcaeae0a538573644193f1959f47c10fa1ea81b0863abea4b14924a87823/main.jpg",
                    "photoSquareUrl": "https://i1.au.reastatic.net/120x120/c27efcaeae0a538573644193f1959f47c10fa1ea81b0863abea4b14924a87823/main.jpg",
                    "photoAlt": "Agent photo"
                },
                {
                    "id": "3083387",
                    "name": "Izabella Minas",
                    "email": "Izabella.Minas@colliers.com",
                    "phone": {
                        "display": "0404208333",
                        "dial": "+61404208333"
                    },
                    "enquiryUrl": "https://api.realcommercial.com.au/mobile/enquiries/504962068/CXXSIC",
                    "photoUrl": "https://i1.au.reastatic.net/142x176/c37a6d999c9e123be17658a3ed0796f0b9906a93b3489c8c8446fbcacc7c8bbc/main.jpg",
                    "photoSquareUrl": "https://i1.au.reastatic.net/120x120/c37a6d999c9e123be17658a3ed0796f0b9906a93b3489c8c8446fbcacc7c8bbc/main.jpg",
                    "photoAlt": "Agent photo"
                }
            ]
        }
    ],
    "documents": [],
    "authorityType": {
        "displayValue": null
    },
    "event": null,
    "price": {
        "salePrice": null,
        "leasePrice": {
            "displayPrice": "Please contact agent",
            "displayPricePerSquareMeter": null,
            "taxType": null,
            "outgoings": null,
            "excludesOutgoings": false
        },
        "soldPrice": null
    },
    "generalAttributes": {
        "floorArea": {
            "value": "359 m²"
        },
        "landArea": null,
        "leaseTerm": null,
        "leasedOn": null,
        "leaseExpiry": null,
        "soldDate": null,
        "carSpaces": null,
        "parkingInfo": null,
        "propertyExtent": null,
        "municipality": null,
        "zoning": null,
        "tenure": null,
        "rawTenure": null,
        "energyRating": null,
        "returnOnInvestment": null
    },
    "buildingDetails": null,
    "shareUrl": "https://www.realcommercial.com.au/504962068",
    "isExactMatch": true,
    "isSurroundingMatch": false
}
````

### Search keywords

realcommercial scraper, realcommercial.com.au scraper, realcommercial API, scrape realcommercial, commercial real estate scraper Australia, commercial property data, realcommercial to CSV, realcommercial to JSON, Apify realcommercial, commercial property scraper

#### 📬 Contact & Custom Solutions

- **Discord**: `@azzouzana`
- **Email**: `labs@azzouzana.com`

### Disclaimer

This actor is an **independent tool**, not affiliated with or endorsed by realcommercial.com.au, REA Group, or related companies. Trademarks belong to their owners.

# Actor input Schema

## `startUrl` (type: `string`):

A valid realcommercial.com.au search URL (for-sale, for-lease, sold, or leased) with filters applied.

## `maxItems` (type: `integer`):

Maximum listings to scrape

## Actor input object example

```json
{
  "startUrl": "https://www.realcommercial.com.au/for-sale/melbourne-vic-3000/?activeSort=date-desc&includePropertiesWithin=includesurrounding",
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
    "startUrl": "https://www.realcommercial.com.au/for-sale/melbourne-vic-3000/?activeSort=date-desc&includePropertiesWithin=includesurrounding",
    "maxItems": 10
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/realcommercial-com-au-scraper-pro-by-search-url").call(input);

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
    "startUrl": "https://www.realcommercial.com.au/for-sale/melbourne-vic-3000/?activeSort=date-desc&includePropertiesWithin=includesurrounding",
    "maxItems": 10,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/realcommercial-com-au-scraper-pro-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.realcommercial.com.au/for-sale/melbourne-vic-3000/?activeSort=date-desc&includePropertiesWithin=includesurrounding",
  "maxItems": 10
}' |
apify call azzouzana/realcommercial-com-au-scraper-pro-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/realcommercial-com-au-scraper-pro-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
