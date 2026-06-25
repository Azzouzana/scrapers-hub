# 🚀 RentCafe Apartment Listings Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the RentCafe Apartment Listings Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/rentcafe-search-pages-scraper?fpr=cbgdsf)

---

## RentCafe Apartment Listings Scraper (By Search URL)

Fast & cheap Apify actor designed to scrape apartment listings from [RentCafe.com](https://www.rentcafe.com/). This scraper extracts detailed property information including pricing, availability, address, phones numbers, amenities, and photos.

### Features

- **Automated Pagination**: Handles search results spanning multiple pages.
- **Detailed Property Data**: Extracts addresses, contact info, pricing, floor plans, phones numbers, amenities, and much more.
- **Configurable Input**: Easily customize the target URL and maximum number of items to scrape.

### Usage

#### Input Parameters

| Field | Type | Description | Default |
|-------|------|-------------|---------|
| `startUrl` | String | The URL of the RentCafe search results page to scrape. | (Required) |
| `maxItems` | Number | Maximum number of items to scrape. | 100 |

#### Example Input

```json
{
    "startUrl": "https://www.rentcafe.com/apartments-for-rent/us/az/?PropertyType=Apartment,Condo",
    "maxItems": 200
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

#### Sample Output

```json
{
	"PropertyId": "57867",
	"Name": "Desert Sands",
	"IsRentCafeListing": true,
	"DetailsUrl": "https://www.rentcafe.com/apartments/az/casa-grande/desert-sands/default.aspx",
	"ContactUrl": null,
	"Phone": "(833) 515-1627",
	"Address": {
		"Address": "720 W. Oneil Dr.",
		"City": "Casa Grande",
		"State": "AZ",
		"ZipCode": "85122",
		"PrettyAddress": "720 W. Oneil Dr., Casa Grande, AZ 85122"
	},
	"AddressFormatted": "720 W. Oneil Dr., Casa Grande, AZ 85122",
	"FallbackAltText": "720 W. Oneil Dr. 1-3 Beds Apartment for Rent",
	"IsCompanyImg": false,
	"ShowPrice": true,
	"PriceValue": "$1,114 - $1,685",
	"PriceLink": null,
	"Beds": "1-3 Beds",
	"FloorplanBedPrice": [
		{
			"Beds": "1 BED",
			"Rent": "$1,114+",
			"RentCssClass": "",
			"DisplayPrice": true
		},
		{
			"Beds": "2 BEDS",
			"Rent": "$1,225+",
			"RentCssClass": "",
			"DisplayPrice": true
		},
		{
			"Beds": "3 BEDS",
			"Rent": "$1,413+",
			"RentCssClass": "",
			"DisplayPrice": true
		}
	],
	"HasPrice": true,
	"Baths": "1-2 Baths",
	"Area": "759 - 1,197 Sqft",
	"Latitude": 32.8984,
	"Longitude": -111.7626,
	"PropertyType": null,
	"HasActionButton": true,
	"CompanyDisplayName": "HSL Asset Management LLC",
	"CompanyLogo": null,
	"IsMatrixListing": false,
	"IsFavoriteListing": false,
	"FavoriteCount": "21",
	"PropertyShortName": "desert-sands",
	"SpecialsAvailable": false,
	"FeaturedType": 5,
	"IsPremiumFeatured": true,
	"PhotoGallery": [
		"https://cdngeneral.rentcafe.com/dmslivecafe/2/58822/Large%20Living%20Rooms.jpg?width=480&quality=90",
		"https://cdngeneral.rentcafe.com/dmslivecafe/2/58822/Spacious%20Kitchen(1).jpg?width=480&quality=90",
		"https://cdngeneral.rentcafe.com/dmslivecafe/2/58822/Spacious%20Bedrooms(1).jpg?width=480&quality=90",
		"https://cdngeneral.rentcafe.com/dmslivecafe/2/58822/Dining%20Area(2).jpg?width=480&quality=90",
		"https://cdngeneral.rentcafe.com/dmslivecafe/2/58822/Sparkling%20Pool(4).jpg?width=480&quality=90"
	],
	"PhotoGalleryImagesCount": 41,
	"Amenities": [
		"air-conditioner",
		"washer-dryer",
		"dishwasher",
		"pool",
		"patio-balcony",
		"large-closets"
	],
	"HasAvailabilityLabel": true,
	"HasPhoneNumber": true,
	"IsCampaign": 0,
	"UseLazyLoadForImage": false,
	"IsContactUsDisabled": false,
	"LastUpdatedDate": "Today",
	"StarRating": 0,
	"UnitsAvailable": "",
	"ReviewsCount": 0,
	"ShowReviews": false,
	"TopRatedLabel": null,
	"VerifiedListingText": "This listing is provided by <b>HSL Asset Management LLC</b>, a reputable property management company with verified listings on RentCafe.",
	"Reviews": null,
	"HasVideo": false,
	"IsClone": false,
	"CafeType": 0,
	"Index": 2,
	"NumberOfRentals": 0,
	"GroupName": null,
	"GroupId": null,
	"IsContacted": false,
	"IsNotAFit": false,
	"LeadContext": "SearchPage",
	"ActionButton": null,
	"IsLiveContent": false,
	"AerielViewVideoId": "CX0lDmh_34SqMTvYv5eSt3",
	"ILSEnableScheduleTour": false,
	"EnableSGTScheduleTour": false,
	"ILSShowTourForm": true,
	"OnlineLeasingUrl": "https://www.rentcafe.com/onlineleasing/apartmentsforrent/oleapplication.aspx?propleadsource_57867=rentcafe&stepname=Floorplan&myOlePropertyid=57867",
	"CssClass": null,
	"IsPartiallyAffordable": false,
	"IsFullyAffordable": false,
	"IsContactedAndUnitsAreAvailable": false,
	"RecommId": null,
	"IsNonYardiListing": false,
	"NonVoyImportCode": 100,
	"IsRewardsPartner": false
}
```

### 📬 Contact & Support

**Need a custom solution? Have a feature request?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

***

<center><i>Made with ❤️ for the data community.</i></center>

# Actor input Schema

## `startUrl` (type: `string`):

The RentCafe search URL to scrape.

## `maxItems` (type: `integer`):

Maximum number of items to scrape.

## Actor input object example

```json
{
  "startUrl": "https://www.rentcafe.com/apartments-for-rent/us/az/?PropertyType=Apartment,Condo",
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
    "startUrl": "https://www.rentcafe.com/apartments-for-rent/us/az/?PropertyType=Apartment,Condo"
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/rentcafe-search-pages-scraper").call(input);

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
run_input = { "startUrl": "https://www.rentcafe.com/apartments-for-rent/us/az/?PropertyType=Apartment,Condo" }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/rentcafe-search-pages-scraper").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.rentcafe.com/apartments-for-rent/us/az/?PropertyType=Apartment,Condo"
}' |
apify call azzouzana/rentcafe-search-pages-scraper --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/rentcafe-search-pages-scraper",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
