# 🚀 Propertyfinder Scraper — Rent, Buy & New Projects (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Propertyfinder Scraper — Rent, Buy & New Projects (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/propertyfinder-ads-search-results-pages-scraper?fpr=cbgdsf)

---

## Propertyfinder Scraper — Rent, Buy & New Projects (By Search URL)

### 🤩 Features

🚀 Our blazing fast Propertyfinder search results scraper🏠 lets you extract real estate ads' information and export them to various format (JSON, CSV, HTML etc..)
🔥 Bring your search URLs and you're good to go!
👉 It enables you to scrape rich details as title, descriptions, photos, energy information, construction date, price, publisher information (email/phone number included) nearby transaportations and a lot more.

=> This actor scrapes **rent**, **buy** and **new projects** search pages results.

The scraper has a required `startUrl` parameter which is an array holding a list of direct real estate links
- Examples of valid URLs:
  - `https://www.propertyfinder.ae/en/search?c=2&pf=19000&pt=20000&fu=0&rp=y&ob=mr`
  - `https://www.propertyfinder.sa/en/search?c=1&t=1&pt=80000&fu=0&ob=mr`
  - `https://www.propertyfinder.ae/en/new-projects?c=5&t=1&ob=mr`

The actor supports scraping data from Propertyfinder in the following countries: the United Arab Emirates (AE), Saudi Arabia (SA), Qatar (QA), Egypt (EG), and Bahrain (BH)

### Looking for something else?

- If you want to search for agents or brokers (e.g: `https://www.propertyfinder.ae/en/find-agent/search?text=dianas&category_id=2`) and want to scrape their information in a structured way (JSON, Excel, XML, etc.), feel free to check out the [📞 Propertyfinder agents/brokers search pages scraper](https://apify.com/azzouzana/propertyfinder-agents-brokers-search-pages-scraper).

### 🤔 Why scrape Propertyfinder?

Propertyfinder is one of the most popular real estate websites in the MENA region, with hundreds of thousand of ads, there's definitely something for you out there!

So what could you do with all these ads?

- Find real estate for sale nearby
- Do market data analysis
- Build a real estate agent email list
- Collect housing data for research or personal purposes
- Compare collected data with home value index
- Use the data for overall real estate data analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

### 🤑 Cost of usage

The usage cost is $1.00 per 1,000 items.

#### Cost Calculation Example

You want to scrape **2,000 listings**.
- Total cost: (2,000 / 1,000) * $1.00 = **$2.00**

> **Note:** This is a Pay-Per-Event actor. You are only charged for successfully scraped items.

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

### 🛠️ Input

| Field | Type | Description | Default value / Example                                                           |
| ----- | ---- | ----------- |-----------------------------------------------------------------------------------|
| `startUrl` | `array` | the search page's result link | `https://www.propertyfinder.ae/en/search?c=2&pfxx=19000&pt=20000&fu=0&rp=y&ob=mr` 
| `maxItems` | `integer` | The maximum number of items to scrape. | `100`                                                         |
| `enableFlattening` | `boolean` | Flatten the result | `false` |

### 🧐 Output

Output is stored in a dataset. Each item is information about a real estate item.

#### Output example

##### 2. Nested (enableFlattening: false)
Preserves the original structure.

```json
{
  "id": "16306053",
  "category_id": 2,
  "property_type": "Villa",
  "price": {
    "value": 170000,
    "currency": "AED",
    "period": "yearly"
  },
  "location": {
      "id": "4618",
      "full_name": "Mira Oasis 1, Mira Oasis, Reem, Dubai",
      "coordinates": {
          "lat": 25.012973,
          "lon": 55.29406
      }
  },
  "title": "Vacant Now | Type C | Back to Back",
  "agent": {
      "id": "223887",
      "name": "Chris Lieb Van Wyk",
      "email": "chris@paragonproperties.ae"
  }
}
````

```json
[{
    "id": "754789",
    "category_id": 1,
    "property_type": "Apartment",
    "price": {
        "value": 180000,
        "currency": "BHD",
        "period": "sell",
        "is_hidden": false
    },
    "title": "Stunning Sea View Brand New Apartment",
    "location": {
        "id": "127",
        "full_name": "Bahrain Financial Harbour, Manama, Capital Governorate",
        "coordinates": {
            "lat": 26.23778533935547,
            "lon": 50.57342529296875
        },
        "slug": "manama-bahrain-financial-harbour",
        "path": "5.34.127",
        "type": "COMMUNITY",
        "name": "Bahrain Financial Harbour",
        "path_name": "Capital Governorate, Manama"
    },
    "images": {
        "property": [
            {
                "small": "https://www.propertyfinder.bh/property/b3d89eb01fb005f3aafed15ab76d4de6/416/272/MODE/23d501/754789-aacado.jpg?ctr=bh",
                "medium": "https://www.propertyfinder.bh/property/b3d89eb01fb005f3aafed15ab76d4de6/668/452/MODE/96d382/754789-aacado.jpg?ctr=bh",
                "full": "https://www.propertyfinder.bh/property/b3d89eb01fb005f3aafed15ab76d4de6/1312/894/MODE/6e5c51/754789-aacado.jpg?ctr=bh",
                "classification_label": "Terrace",
                "thumbnail": "https://www.propertyfinder.bh/property/b3d89eb01fb005f3aafed15ab76d4de6/260/185/MODE/47669f/754789-aacado.jpg?ctr=bh"
            },
            {
                "small": "https://www.propertyfinder.bh/property/0e28577e0507ffb0f7ef1f098cf0c5ae/416/272/MODE/e7e4ad/754789-92390o.jpg?ctr=bh",
                "medium": "https://www.propertyfinder.bh/property/0e28577e0507ffb0f7ef1f098cf0c5ae/668/452/MODE/903c5d/754789-92390o.jpg?ctr=bh",
                "full": "https://www.propertyfinder.bh/property/0e28577e0507ffb0f7ef1f098cf0c5ae/1312/894/MODE/193805/754789-92390o.jpg?ctr=bh",
                "classification_label": "Empty Room",
                "thumbnail": "https://www.propertyfinder.bh/property/0e28577e0507ffb0f7ef1f098cf0c5ae/260/185/MODE/633e7c/754789-92390o.jpg?ctr=bh"
            },
            {
                "small": "https://www.propertyfinder.bh/property/e41dd1174876225e01ad723a0ddda768/416/272/MODE/b37f7e/754789-d3cc7o.jpg?ctr=bh",
                "medium": "https://www.propertyfinder.bh/property/e41dd1174876225e01ad723a0ddda768/668/452/MODE/b77b75/754789-d3cc7o.jpg?ctr=bh",
                "full": "https://www.propertyfinder.bh/property/e41dd1174876225e01ad723a0ddda768/1312/894/MODE/e1b776/754789-d3cc7o.jpg?ctr=bh",
                "classification_label": "Empty Room",
                "thumbnail": "https://www.propertyfinder.bh/property/e41dd1174876225e01ad723a0ddda768/260/185/MODE/4a1dd6/754789-d3cc7o.jpg?ctr=bh"
            },
            {
                "small": "https://www.propertyfinder.bh/property/6939d0ac5f0a5954a7e3ececf8e03db0/416/272/MODE/81ffa1/754789-a79fdo.jpg?ctr=bh",
                "medium": "https://www.propertyfinder.bh/property/6939d0ac5f0a5954a7e3ececf8e03db0/668/452/MODE/1088b4/754789-a79fdo.jpg?ctr=bh",
                "full": "https://www.propertyfinder.bh/property/6939d0ac5f0a5954a7e3ececf8e03db0/1312/894/MODE/981b2d/754789-a79fdo.jpg?ctr=bh",
                "classification_label": "Kitchen",
                "thumbnail": "https://www.propertyfinder.bh/property/6939d0ac5f0a5954a7e3ececf8e03db0/260/185/MODE/563002/754789-a79fdo.jpg?ctr=bh"
            },
            {
                "small": "https://www.propertyfinder.bh/property/a400536d0f7a7072d2aafefb1cbd2ac3/416/272/MODE/cd79d8/754789-477e2o.jpg?ctr=bh",
                "medium": "https://www.propertyfinder.bh/property/a400536d0f7a7072d2aafefb1cbd2ac3/668/452/MODE/da6fb9/754789-477e2o.jpg?ctr=bh",
                "full": "https://www.propertyfinder.bh/property/a400536d0f7a7072d2aafefb1cbd2ac3/1312/894/MODE/11009b/754789-477e2o.jpg?ctr=bh",
                "classification_label": "Kitchen",
                "thumbnail": "https://www.propertyfinder.bh/property/a400536d0f7a7072d2aafefb1cbd2ac3/260/185/MODE/a76c20/754789-477e2o.jpg?ctr=bh"
            },
            {
                "small": "https://www.propertyfinder.bh/property/6d942958e22843ba9870877cc37eda00/416/272/MODE/78e602/754789-66958o.jpg?ctr=bh",
                "medium": "https://www.propertyfinder.bh/property/6d942958e22843ba9870877cc37eda00/668/452/MODE/62c940/754789-66958o.jpg?ctr=bh",
                "full": "https://www.propertyfinder.bh/property/6d942958e22843ba9870877cc37eda00/1312/894/MODE/a2261a/754789-66958o.jpg?ctr=bh",
                "classification_label": "Empty Room",
                "thumbnail": "https://www.propertyfinder.bh/property/6d942958e22843ba9870877cc37eda00/260/185/MODE/ee717b/754789-66958o.jpg?ctr=bh"
            },
            {
                "small": "https://www.propertyfinder.bh/property/9b2f41cb335030260433b33ed3d93b2a/416/272/MODE/b8cf9a/754789-e5598o.jpg?ctr=bh",
                "medium": "https://www.propertyfinder.bh/property/9b2f41cb335030260433b33ed3d93b2a/668/452/MODE/b66727/754789-e5598o.jpg?ctr=bh",
                "full": "https://www.propertyfinder.bh/property/9b2f41cb335030260433b33ed3d93b2a/1312/894/MODE/96b945/754789-e5598o.jpg?ctr=bh",
                "classification_label": "Empty Room",
                "thumbnail": "https://www.propertyfinder.bh/property/9b2f41cb335030260433b33ed3d93b2a/260/185/MODE/650e7d/754789-e5598o.jpg?ctr=bh"
            },
            {
                "small": "https://www.propertyfinder.bh/property/a89cbb803b5a5ea34f4c2dba5ceb51e6/416/272/MODE/8ebeea/754789-aed88o.jpg?ctr=bh",
                "medium": "https://www.propertyfinder.bh/property/a89cbb803b5a5ea34f4c2dba5ceb51e6/668/452/MODE/ebd9b5/754789-aed88o.jpg?ctr=bh",
                "full": "https://www.propertyfinder.bh/property/a89cbb803b5a5ea34f4c2dba5ceb51e6/1312/894/MODE/62bc39/754789-aed88o.jpg?ctr=bh",
                "classification_label": "Bathroom",
                "thumbnail": "https://www.propertyfinder.bh/property/a89cbb803b5a5ea34f4c2dba5ceb51e6/260/185/MODE/832745/754789-aed88o.jpg?ctr=bh"
            },
            {
                "small": "https://www.propertyfinder.bh/property/2870c45064d649c6324c16e2978a9c34/416/272/MODE/d0c01b/754789-694fao.jpg?ctr=bh",
                "medium": "https://www.propertyfinder.bh/property/2870c45064d649c6324c16e2978a9c34/668/452/MODE/ff8e0b/754789-694fao.jpg?ctr=bh",
                "full": "https://www.propertyfinder.bh/property/2870c45064d649c6324c16e2978a9c34/1312/894/MODE/6fde63/754789-694fao.jpg?ctr=bh",
                "classification_label": "Reception / Lobby",
                "thumbnail": "https://www.propertyfinder.bh/property/2870c45064d649c6324c16e2978a9c34/260/185/MODE/d7ba91/754789-694fao.jpg?ctr=bh"
            },
            {
                "small": "https://www.propertyfinder.bh/property/dde6d20e090842cb8dbeb5372c3fe9fd/416/272/MODE/257511/754789-6e582o.jpg?ctr=bh",
                "medium": "https://www.propertyfinder.bh/property/dde6d20e090842cb8dbeb5372c3fe9fd/668/452/MODE/dc56a5/754789-6e582o.jpg?ctr=bh",
                "full": "https://www.propertyfinder.bh/property/dde6d20e090842cb8dbeb5372c3fe9fd/1312/894/MODE/cf7ea1/754789-6e582o.jpg?ctr=bh",
                "classification_label": "Pool",
                "thumbnail": "https://www.propertyfinder.bh/property/dde6d20e090842cb8dbeb5372c3fe9fd/260/185/MODE/1dab6f/754789-6e582o.jpg?ctr=bh"
            }
        ],
        "community": [],
        "tower": []
    },
    "agent": {
        "id": "3644",
        "image": "https://www.propertyfinder.bh/images/pf_agent/picture/b79922a83feaf3e6eb48b11d8f4ad4922a544305/desktop",
        "is_super_agent": true,
        "name": "Husain Alsebea",
        "user_id": 3212,
        "email": "husain@beyondbestre.com",
        "social": "",
        "languages": [
            "English",
            "Arabic"
        ],
        "slug": "husain-alsebea",
        "avg_whatsapp_response_time": 145,
        "total_properties": 65,
        "position": "Founder",
        "years_of_experience": 10,
        "transactions_count": 0,
        "rating_breakdown": {
            "score1": 0,
            "score2": 0,
            "score3": 0,
            "score4": 0,
            "score5": 0
        },
        "detail_url": "/en/agent/husain-alsebea-3644"
    },
    "broker": {
        "id": "615",
        "logo": "https://www.propertyfinder.bh/broker/4/178/98/MODE/76f92e/615-logo.jpg?ctr=bh",
        "name": "Beyond Best Real Estate",
        "address": "Office 5048, Building 554, Manama, 144, Capital Governorate, PO Box 572",
        "email": "husain@beyondbestre.com",
        "phone": "+97339290113",
        "slug": "beyond-best-real-estate",
        "total_properties": 76,
        "license_number": "218181-3",
        "is_exclusive": false
    },
    "is_verified": false,
    "is_direct_from_developer": false,
    "is_new_construction": false,
    "is_available": true,
    "is_featured": false,
    "is_premium": false,
    "is_new_insert": false,
    "utilities_price_type": "exclusive",
    "live_viewing": null,
    "is_community_expert": false,
    "is_cts": false,
    "bedrooms": "2",
    "bathrooms": "3",
    "size": {
        "value": 145,
        "unit": "sqm"
    },
    "share_url": "https://www.propertyfinder.bh/en/plp/buy/apartment-for-sale-capital-governorate-manama-bahrain-financial-harbour-754789.html",
    "reference": "BYS-2-001",
    "listed_date": "2023-12-26T10:49:24Z",
    "contact_options": [
        {
            "type": "email",
            "value": "husain@beyondbestre.com",
            "link": "mailto:husain@beyondbestre.com",
            "is_did": false
        },
        {
            "type": "phone",
            "value": "+97339290113",
            "link": "tel:+97339290113",
            "is_did": false
        },
        {
            "type": "sms",
            "value": "+97339290113",
            "link": "sms:+97339290113",
            "is_did": false
        },
        {
            "type": "whatsapp",
            "value": "+97316191073",
            "link": "https://api.whatsapp.com/send?phone=+97316191073&text=Hello%2C%0AI+would+like+to+get+more+information+about+this+property%3A+%0A+%0AReference%3A+BYS-2-001%0AType%3A+Apartment%0APrice%3A+180%2C000+BHD+%0ALocation%3A+Bahrain+Financial+Harbour+%0ALink%3A+https%3A%2F%2Fwww.propertyfinder.bh%2Fto%2F754789%2Fen+%0A+%0AAny+changes+made+to+this+message+will+result+in+the+enquiry+not+being+sent+to+the+agent.",
            "is_did": false
        }
    ],
    "images_count": 10,
    "amenities": [
        {
            "code": "AC",
            "name": "Central A/C"
        },
        {
            "code": "BA",
            "name": "Balcony"
        },
        {
            "code": "SP",
            "name": "Shared Pool"
        },
        {
            "code": "SE",
            "name": "Security"
        },
        {
            "code": "CS",
            "name": "Concierge"
        },
        {
            "code": "CP",
            "name": "Covered Parking"
        },
        {
            "code": "BW",
            "name": "Built in Wardrobes"
        },
        {
            "code": "BK",
            "name": "Kitchen Appliances"
        },
        {
            "code": "VW",
            "name": "View of Water"
        },
        {
            "code": "PA",
            "name": "Pets Allowed"
        },
        {
            "code": "SY",
            "name": "Shared Gym"
        },
        {
            "code": "LB",
            "name": "Lobby in Building"
        },
        {
            "code": "BR",
            "name": "Barbecue Area"
        }
    ],
    "completion_status": "completed",
    "furnished": "PARTLY",
    "property_type_id": 1,
    "view_360": "",
    "rsp": 0,
    "rss": 0,
    "qs": 100,
    "is_exclusive": false,
    "is_broker_project_property": false,
    "rera": {
        "number": "00000",
        "permit_validation_url": ""
    },
    "offering_type": "Residential for Sale",
    "video_id": "",
    "is_smart_ad": false,
    "is_spotlight_listing": false,
    "is_claimed_by_agent": false,
    "is_under_offer_by_competitor": false,
    "listing_level": "standard",
    "listing_level_label": "standard",
    "location_tree": [
        {
            "id": "5",
            "name": "Capital Governorate",
            "type": "REGION",
            "slug": "capital-governorate",
            "slug_en": "capital-governorate"
        },
        {
            "id": "34",
            "name": "Manama",
            "type": "AREA",
            "slug": "manama",
            "slug_en": "manama"
        },
        {
            "id": "127",
            "name": "Bahrain Financial Harbour",
            "type": "COMMUNITY",
            "slug": "manama-bahrain-financial-harbour",
            "slug_en": "manama-bahrain-financial-harbour"
        }
    ],
    "description": "Brand new project in a very center of Bahrain.  \n\nInvest in a luxury brand new apartment in a Prestigious location of Bahrain Financial Harbor.  \nHarbor Row.\nThe 2 bedroom apartment, semi furnished flat with balcony and stunning sunsets and amazing sea view. \n\nApartments with  high-end facilities, premium appliances, comprising:\n\n- Open plan dining and kitchen\n- Balconies\n- Kitchen with high-end cabinets, BOSCH dishwasher and appliances\n- 2 Bedrooms all with en-suite bathrooms and fitted wardrobes\n- Guest bathroom\n\nFacilities:-\n\n- Indoor swimming pool \n- Gym\n- Tennis courts\n- Basketball courts\n- Paddle courts\n- Underground parking\n- Reception\n- Security\n\nCoffee shops and supermarket now open on site, walking area.\n\nA short drive will take you to City Centre and Seef Mall, Bahrain Bay and Four Seasons, the airport and Saudi Causeway.",
    "rental_availability_date": null,
    "payment_method": [],
    "floor_plans": [],
    "lead_value": 10,
    "similar_price_transactions": {
        "buy": [],
        "rent": []
    },
    "agent_license_no": "",
    "share_url_translated": "https://www.propertyfinder.bh/ar/plp/%D9%84%D9%84%D8%A8%D9%8A%D8%B9/%D8%B4%D9%82%D8%A9-%D9%84%D9%84%D8%A8%D9%8A%D8%B9-%D9%85%D8%AD%D8%A7%D9%81%D8%B8%D8%A9-%D8%A7%D9%84%D8%B9%D8%A7%D8%B5%D9%85%D8%A9-%D8%A7%D9%84%D9%85%D9%86%D8%A7%D9%85%D8%A9-%D9%85%D8%B1%D9%81%D8%A3-%D8%A7%D9%84%D8%A8%D8%AD%D8%B1%D9%8A%D9%86-%D8%A7%D9%84%D9%85%D8%A7%D9%84%D9%8A-754789.html",
    "bedrooms_value": 2,
    "bathrooms_value": 3,
    "licenses": [
        {
            "license_type": "bh_rera_certificate",
            "license_number": "",
            "license_url": "https://www.rera.gov.bh/DigiCert/DigiCert?p=hDtg7gmI7VOU8tXguL9FIQ%3d%3d"
        }
    ],
    "apify_input_url": "https://www.propertyfinder.bh/en/plp/buy/apartment-for-sale-capital-governorate-manama-bahrain-financial-harbour-754789.html"
}]
```

### ⚠️ Disclaimer

This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Propertyfinder FZ LLC or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

# Actor input Schema

## `startUrl` (type: `string`):

Search results page URL

## `maxItems` (type: `integer`):

Maximum number of items to scrape

## `enableFlattening` (type: `boolean`):

Flatten the results into a single level JSON structure

## Actor input object example

```json
{
  "startUrl": "https://www.propertyfinder.ae/en/search?c=2&pf=19000&pt=25000&fu=0&rp=y&ob=mr",
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
    "startUrl": "https://www.propertyfinder.ae/en/search?c=2&pf=19000&pt=25000&fu=0&rp=y&ob=mr",
    "maxItems": 2000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/propertyfinder-ads-search-results-pages-scraper").call(input);

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
    "startUrl": "https://www.propertyfinder.ae/en/search?c=2&pf=19000&pt=25000&fu=0&rp=y&ob=mr",
    "maxItems": 2000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/propertyfinder-ads-search-results-pages-scraper").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.propertyfinder.ae/en/search?c=2&pf=19000&pt=25000&fu=0&rp=y&ob=mr",
  "maxItems": 2000
}' |
apify call azzouzana/propertyfinder-ads-search-results-pages-scraper --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/propertyfinder-ads-search-results-pages-scraper",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
