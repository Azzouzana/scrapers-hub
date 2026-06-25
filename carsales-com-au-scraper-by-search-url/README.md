# 🚀 Carsales.com.au Scraper — Dealer & Private Listings (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Carsales.com.au Scraper — Dealer & Private Listings (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/carsales-com-au-scraper-by-search-url?fpr=cbgdsf)

---

## Carsales.com.au Scraper — Dealer & Private Listings (By Search URL)

Extract comprehensive vehicle data from **Carsales.com.au** in seconds. Whether you are conducting automotive market research, tracking competitor pricing, or building a car dealership database, this high-performance scraper delivers structured data at scale for **less than the price of a coffee**.

### 🚀 Why choose this scraper?
* **Comprehensive Data:** Get everything from prices, high-res photos, and technical specs to seller notes and contact info.
* **Cost-Effective:** Professional-grade data extraction for just **$1 per 1,000 listings**.
* **Zero Coding Required:** Simply paste your search URL from Carsales and let the actor do the rest.
* **Developer-Ready:** Export results in **JSON, CSV, XML, or Excel**, or integrate directly via **API**.

### How to use this actor 🚀

1. [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required.
2. Open the actor, add your **Input**, and start a run.
3. A free account includes enough credits to try the scraper and check the data.
4. Use the free tier to see if the output fits your project before scaling up.

The scraper needs a **`startUrl`**: a valid **cars** search URL from carsales.com.au (with your filters already applied in the browser).

- It should start with: `https://www.carsales.com.au/cars`
- Example:
    - `https://www.carsales.com.au/cars/?q=%28And.Make.BMW._.PriceIndicator.Low.%29`

Copy the URL from the site after you set make, price, location, fuel type, and anything else you need.

### Why scrape carsales.com.au?

carsales.com.au is one of Australia’s largest car marketplaces, with dealer and private listings.

* **Market Intelligence:** Watch price fluctuations over time to identify the best time to buy or sell.
* **Price Comparison:** Bulk-compare similar models across different regions to find undervalued gems.
* **Lead Generation & Reports:** Build comprehensive inventory lists or market reports for dealerships and private collectors.
* **Bypasses the 20-pages limit, scraping way more than 440 results
* **Regional Stock Analysis:** Map out vehicle availability within specific budgets or geographic zones.
* **AI & Machine Learning:** Feed clean, structured data into **LLMs (like GPT-4 or Gemini)** or custom models to build car-buying assistants, price prediction engines, or automated valuation tools.

### Cost of usage

Simple, **$1 per 1,000 listings** scraped. No hidden fees.

| Listings | Estimated cost |
| -------: | -------------: |
| 100 | ~$0.10 |
| 1,000 | ~$1.00 |
| 5,000 | ~$5.00 |
| 10,000 | ~$10.00 |

### Free tier limitations

On the **free tier**, runs are usually limited as follows:

- **Sample size:** up to **5 listings** per run.
- **Daily cap:** about **5 runs** per calendar day (UTC).
- **Between runs:** about **30 minutes** before you can start another run.

> Limits can change based on platform rules and fair use.

#### Upgrade when you're ready

If the actor works for you, a **paid Apify plan** lifts those caps so you can run more often and scrape more listings. [Apify pricing](https://apify.com/pricing?fpr=cbgdsf).

### Input

| Field | Type | Description | Default value / Example |
| ----- | ---- | ----------- | ----------------------- |
| `startUrl` | `string` | Your cars search URL from carsales.com.au | `https://www.carsales.com.au/cars/?q=…` |
| `maxItems` | `number` | How many listings to collect | `10` |

### Output

Results go to the **dataset**. Each row is one vehicle listing with the fields the scraper could collect for that ad.

Example listing:

```json
{
    "adId": "SSE-AD-19119170",
    "adType": "used",
    "badge": "gt",
    "bodyStyle": "suv",
    "bodyType": "SUV",
    "canonicalUrl": "https://www.carsales.com.au/cars/details/2018-mazda-cx-5-gt-kf-series-auto-i-activ-awd/SSE-AD-19119170/",
    "categoryType": "wagon",
    "clearance": "false",
    "colour": "snowflake white pearl",
    "condition": "UsedCondition",
    "doors": "5",
    "driveType": "4x4",
    "engineDisplacementCc": 2488,
    "featureTags": [
        "Full service history",
        "Sunroof",
        "Bluetooth",
        "..."
    ],
    "floorplan": "cx-5",
    "fuelType": "Petrol",
    "gallery360Count": 0,
    "galleryImageCount": 16,
    "galleryVideoCount": 1,
    "hasImages": "true",
    "heading": "2018 Mazda CX-5 GT KF Series Auto i-ACTIV AWD",
    "imageUrls": [
        "https://carsales.pxcrush.net/carsales/cars/private/dg27x5stn4kusccklo7es8w49.jpg?pxc_method=gravityfill&pxc_bgtype=self&pxc_size=900,600",
        "..."
    ],
    "key_body_type": "SUV",
    "key_fuel": "Petrol",
    "key_odometer": "132,000km",
    "key_transmission": "Automatic",
    "location": "QLD • Private",
    "make": "Mazda",
    "model": "CX-5",
    "networkId": "sse-ad-19119170",
    "newAndUsed": "used",
    "odometer": "132000",
    "pageImageUrl": "https://carsales.pxcrush.net/carsales/cars/private/dg27x5stn4kusccklo7es8w49.jpg?pxc_format=jpeg&pxc_method=crop&pxc_size=1200,630",
    "pageMetaDescription": "KF4WLA GT Wagon 5dr SKYACTIV-Drive 6sp i-ACTIV AWD 2.5i (5yr warranty)",
    "photoCount": 16,
    "postcode": "4223",
    "price": 24300,
    "priceCurrency": "AUD",
    "priceIndicatorBadges": [
        "Around market price"
    ],
    "priceType": "egc",
    "primaryImageUrl": "https://carsales.pxcrush.net/carsales/cars/private/dg27x5stn4kusccklo7es8w49.jpg",
    "publishDate": "2018-08-02t07:11:17",
    "region": "gold coast",
    "saleStatus": "for sale",
    "searchCardPath": "/cars/details/2018-mazda-cx-5-gt-kf-series-auto-i-activ-awd/SSE-AD-19119170/",
    "seats": "5",
    "sellerComment": "The Mazda CX5 Grand Touring (GT) is second only to the Akera in specs. \nBRAND NEW BATTERY THIS WEEK WITH 2 year warranty\nAll log-book services and the manufacturers manual is included. \nNew smart windscreen due to a stone-chip about 12 months ago.\nIt is a great car with plenty of extras:\nLeather seats, \nBose speakers\nSunroof \nPush-button locking and unlocking front doors so you don't have to get the key-fob out when your hands are full of shopping. \nPower liftgate  or automatic boot with push-button operation \nMultiple device charging options with 2 USB slots and one lighter to adaptor options. \n\nThe blind-spot warnings on the side mirrors are great and save you twisting to look behind and beside and momentarily losing forward vision.  \nBoth of the front leather seats are heated with separate controls and electric adjustments  \nDrivers seat has lumbar adjustment and settings memory. \nThe dual zone climate control also lets you choose between what areas to cool or heat on each side separately. \nCustom Mazda floor covers and a brand new woolen seat-belt comforter will be thrown in for free. \nMazda Radar Cruise Control (MRCC) and Lane Departure Warning (LDW) \nReversing camera \nSpeed zone reminder - road sign recognition, \nAutomatic wipers and automatic headlight on-off so you won't lose battery if you forget to turn the lights off!\n\nThere are a couple of small trolley dents low down on the side back door but they have not scratched the paint and are barely noticeable. A photo is attached. \n\nSelling due to car upgrade for work.\n\nDELIVERS GREAT VALUE\nThis Mazda CX-5 SUV has cruise control, side airbags, keyless start and central locking. This car has front parking sensors, USB audio input, iPod connectivity and blue-tooth. It has 6 airbags to protect you and your family with an ANCAP safety rating of 5. Only travelled 118,000 km of mostly highway driving.\n\nYOU WILL LOVE THESE FEATURES\n- Storage compartment in centre console\n- Front cup holders\n- Remote central locking\n- Rear vision camera\n- Satellite navigation (GPS)\n- Power tailgate/boot\n- Forward collision alert/warning \n- Dual zone climate control air conditioning\n- Leather seats\n\n\n6 airbags to give you added protection with an ANCAP safety rating of 5. This Mazda CX-5 GT SUV has leather gear knob, front cup holders, digital radio (DAB+) and remote central locking.",
    "sellerId": "sse-seller-19119170",
    "sellerPhones": [],
    "sellerType": "Person",
    "slug": "2018-mazda-cx-5-gt-kf-series-auto-i-activ-awd",
    "spec_airbags": "Driver\nPassenger\nHead for 1st row seats (front)\nHead for 2nd row seats\nSide for 1st row occupants (front)",
    "spec_ancap_rating": "5",
    "spec_ancap_safety_rating": "5/1",
    "spec_body_coloured": "Bumpers\nDoor handles\nExterior mirrors partial",
    "spec_body_type": "SUV, 5 doors, 5 seats",
    "spec_build_date": "July 2018",
    "spec_carsales_network_id": "SSE-AD-19119170",
    "spec_climate": "Climate control 2 zone",
    "spec_compliance_date": "July 2018",
    "spec_country_of_origin": "JAPAN",
    "spec_display": "Information display - head up\nTrip computer",
    "spec_engine": "4 cylinders, Petrol Aspirated, 2.5L",
    "spec_engine_description": "Drive by wire (electronic throttle control)",
    "spec_engine_type": "Piston",
    "spec_exterior_colour": "Snowflake White Pearl",
    "spec_front": "Ventilated",
    "spec_front_row_seats": "Height adjustable driver\nHeight adjustable passenger",
    "spec_fuel_consumption_combined": "7.4 L/100km",
    "spec_fuel_type": "Petrol",
    "spec_fuel_use_reduction": "Engine - cylinder shutdown (fuel economy)\nEngine - stop start system (when at idle)",
    "spec_gears": "6",
    "spec_headlights": "Active (cornering/steering)\nAutomatic (light sensitive)\nLED",
    "spec_inputs": "Aux input socket (MP3/CD/cassette)\nAux input USB socket\nInput for iPod",
    "spec_interior_colour": "Black",
    "spec_leather": "Gear knob\nSeats - partial\nSteering wheel",
    "spec_length": "4550mm",
    "spec_location": "Currumbin, QLD 4223",
    "spec_new_south_wales": "Allowed",
    "spec_odometer_132_000km": "Body type SUV",
    "spec_operation": "Multi-function steering wheel",
    "spec_power_sockets": "12V sockets - auxiliary",
    "spec_powerplant_type": "Internal Combustion Engine (ICE)",
    "spec_registration_expiry": "5 months/September 2026",
    "spec_registration_plate": "Check with seller",
    "spec_rim_material": "Alloy",
    "spec_rims": "19\" alloy wheels",
    "spec_roadworthy_certificate": "Provided at pick-up by seller",
    "spec_steering": "Rack and Pinion",
    "spec_transmission": "6 speed Automatic",
    "spec_vehicle_description": "KF4WLA GT Wagon 5dr SKYACTIV-Drive 6sp i-ACTIV AWD 2.5i (5yr warranty)",
    "spec_warranty_in_years_from_first_registration": "5yr",
    "startUrl": "https://www.carsales.com.au/cars/mazda/cx-5/new-south-wales-state/automatic-transmission/petrol-fueltype/under-25000/",
    "state": "qld",
    "subtitle": "KF4WLA GT Wagon 5dr SKYACTIV-Drive 6sp i-ACTIV AWD 2.5i (5yr warranty)",
    "suburb": "currumbin",
    "tabFeature_audio_visual_communication_inputs": "Aux input socket (MP3/CD/cassette)\nAux input USB socket\nInput for iPod",
    "tabFeature_brakes_front": "Ventilated",
    "tabFeature_comfort_convenience_climate": "Climate control 2 zone",
    "tabFeature_electrical_power_sockets": "12V sockets - auxiliary",
    "tabFeature_engine_engine_description": "Drive by wire (electronic throttle control)",
    "tabFeature_exterior_body_coloured": "Bumpers\nDoor handles\nExterior mirrors partial",
    "tabFeature_fuel_fuel_use_reduction": "Engine - cylinder shutdown (fuel economy)\nEngine - stop start system (when at idle)",
    "tabFeature_instruments_controls_display": "Information display - head up\nTrip computer",
    "tabFeature_interior_leather": "Gear knob\nSeats - partial\nSteering wheel",
    "tabFeature_lights_windows_headlights": "Active (cornering/steering)\nAutomatic (light sensitive)\nLED",
    "tabFeature_safety_security_airbags": "Driver\nPassenger\nHead for 1st row seats (front)\nHead for 2nd row seats\nSide for 1st row occupants (front)",
    "tabFeature_seating_front_row_seats": "Height adjustable driver\nHeight adjustable passenger",
    "tabFeature_steering_operation": "Multi-function steering wheel",
    "tabFeature_wheels_tyres_rims": "19\" alloy wheels",
    "tabOverview_ancap_safety_rating": "5/1",
    "tabOverview_body_type": "SUV, 5 doors, 5 seats",
    "tabOverview_build_date": "July 2018",
    "tabOverview_carsales_network_id": "SSE-AD-19119170",
    "tabOverview_compliance_date": "July 2018",
    "tabOverview_engine": "4 cylinders, Petrol Aspirated, 2.5L",
    "tabOverview_exterior_colour": "Snowflake White Pearl",
    "tabOverview_fuel_consumption_combined": "7.4 L/100km",
    "tabOverview_interior_colour": "Black",
    "tabOverview_powerplant_type": "Internal Combustion Engine (ICE)",
    "tabOverview_registration_expiry": "5 months/September 2026",
    "tabOverview_registration_plate": "Check with seller",
    "tabOverview_roadworthy_certificate": "Provided at pick-up by seller",
    "tabOverview_transmission": "6 speed Automatic",
    "tabOverview_vehicle_description": "KF4WLA GT Wagon 5dr SKYACTIV-Drive 6sp i-ACTIV AWD 2.5i (5yr warranty)",
    "tabSpec_dimensions_weights_length": "4550mm",
    "tabSpec_engine_engine_type": "Piston",
    "tabSpec_fuel_fuel_type": "Petrol",
    "tabSpec_other_country_of_origin": "JAPAN",
    "tabSpec_probationary_plate_status_new_south_wales": "Allowed",
    "tabSpec_safety_security_ancap_rating": "5",
    "tabSpec_steering_steering": "Rack and Pinion",
    "tabSpec_transmission_drivetrain_gears": "6",
    "tabSpec_warranty_service_warranty_in_years_from_first_registration": "5yr",
    "tabSpec_wheels_tyres_rim_material": "Alloy",
    "title": "2018 Mazda CX-5 GT KF Series Auto i-ACTIV AWD",
    "transmission": "Automatic",
    "url": "https://www.carsales.com.au/cars/details/2018-mazda-cx-5-gt-kf-series-auto-i-activ-awd/SSE-AD-19119170/",
    "year": "2018"
}
````

### Looking for something else?

Browse [scrapers on the Apify Store](https://apify.com/store?fpr=cbgdsf) for other sites and use cases.

### Search keywords

carsales scraper, carsales.com.au scraper, carsales API, scrape carsales, carsales data extraction, carsales crawler, carsales listings scraper, Australia car scraper, used cars Australia data, car price scraper Australia, carsales vehicle data, carsales search scraper, car marketplace scraper, automotive data Australia, car listings API, carsales export, carsales to CSV, carsales to JSON, car dealer scraper Australia, Apify carsales

#### 📬 Contact & Custom Solutions

Want to chat? Don't hesitate to reach out to us:

- **Discord**: `@azzouzana`
- **Email**: `labs@azzouzana.com`

### Disclaimer

This actor is an **independent tool**. It is not affiliated with, endorsed by, or sponsored by carsales.com.au, Carsales Network, or related companies. Trademarks belong to their owners.

# Actor input Schema

## `startUrl` (type: `string`):

Must start with https://www.carsales.com.au/cars/?q= (encoded search predicate).

## `maxItems` (type: `integer`):

Maximum listings to scrape

## Actor input object example

```json
{
  "startUrl": "https://www.carsales.com.au/cars/?q=%28And.Make.BMW._.PriceIndicator.Low.%29",
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
    "startUrl": "https://www.carsales.com.au/cars/?q=%28And.Make.BMW._.PriceIndicator.Low.%29",
    "maxItems": 10
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/carsales-com-au-scraper-by-search-url").call(input);

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
    "startUrl": "https://www.carsales.com.au/cars/?q=%28And.Make.BMW._.PriceIndicator.Low.%29",
    "maxItems": 10,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/carsales-com-au-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.carsales.com.au/cars/?q=%28And.Make.BMW._.PriceIndicator.Low.%29",
  "maxItems": 10
}' |
apify call azzouzana/carsales-com-au-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/carsales-com-au-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
