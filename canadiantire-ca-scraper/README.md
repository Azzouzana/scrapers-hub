# 🚀 Canadian Tire Products Scraper — Search, Categories & Product URLs

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Canadian Tire Products Scraper — Search, Categories & Product URLs. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/canadiantire-ca-scraper?fpr=cbgdsf)

---

## Canadian Tire Products Scraper — Search, Categories & Product URLs

### Features

Our Canadiantire scraper lets you extract products details from search results, from categories pages and from direct product URLs
on [Canadiantire.ca](https://www.canadiantire.ca/). It enables you to scrape rich products details as titles, descriptions, images, availabilities, ratings, prices, and all other available information.


The scraper has a requried `startUrls` parameter which is an array that should contain any combination of:
- Category page URL (plus a store) as input. It scrapes and returns category's products with their information. In terms of speed, this feature returns around 3.8K products/minute
- Search URL (plus a store) as input. It scrapes and returns search pages results products with their information. In terms of speed, this feature returns around 4K products/minute
- Direct product URL(s) (plus a store) as input. Since these are direct product URLs, the scraping speed is around 800 products/minute still fast but it's relatively slower than categories & search results pages scraping's speed.

Sample output:
![Sample Output](https://iili.io/HGrA58v.png)

### Is it legal to scrape Canadiantire?

It is legal to scrape publicly available data such as products descriptions, prices, or ratings. Read our blog post
on [the legality of web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) to learn more.

### Why scrape Canadiantire?

Canadiantire canada owns chains of 500+ retail stores, has millions of products in its database and has more than 25
million monthly unique visitors.

So what could you do with all that products listings data?

- Use the data to add value to your ecommerce/marketing business by providing extra information to your visitors.
- Marketing insights: You can use the data scraped to gather marketing insights, such as identifying popular products,
  trending items, and customer behavior.
- Price monitoring: Scraping can be used to track the prices of products, helping you to stay up-to-date with pricing
  trends and adjust your own pricing strategies.
- Improved customer experience: You can use the data scraped to identify customer preferences, enabling you to
  personalize your offerings and improve the overall customer experience.
- Train AI models to predict future trends and act fast when opportunities arise.

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

### Input

| Field | Type | Description | Default value
| ----- | ---- | ----------- | -------------|
| startUrls | array | the URLs that the scraper will scrape. For categories and search results pages, it will scrape products which show up there. For direct products URLs, it will scrape them one by one. | `[{url: https://www.canadiantire.ca/en/search-results.html?q=shirts}]` |
| store | number | The store ID against which to do the search load category's page or open product's page. To get this value, open the [store locator page](https://www.canadiantire.ca/en/store-locator.html), search/find your store & click `view store details`. Grab the digits at the end of the url & paste it here. For example, you navigated to this store: `https://www.canadiantire.ca/en/store-details/nl/carbonear-nl-217.html`, you have to grab `217`. | none | 
| deepSearch | checkbox | Whether to scrape products data from the listing pages (catgeories/search results pages) or follow the products links and scrape their deep data. Please see below note about his field. | `false` |
| language | EN or FR | In which language to scrape results | `en` |

## How to get startsUrls
- To get search results page URL: 
open canadiantire's website, locate the search bar, type (choose your filter(s)), trigger the search & note the resulting url in the navigation bar. Make sure that it looks similar to  `https://www.canadiantire.ca/en/search-results.html?......`


- To get category's page URL: 
access canadiantire's website and open a category's page then make sure to copy the address in the navigation bar. Make sure that it looks similar to `https://www.canadiantire.ca/en/cat/home-pets-DC0000001.html`

- To get direct product URL: 
open canadiantire's website, open a product's page and copy the address in the navigation bar. Make sure that the url looks similar to `https://www.canadiantire.ca/en/cat/toys-sports-recreation/team-sports/soccer/soccer-balls-DC0002528.html`

## How to set the store ID?

The `store` parameter has to be specified either in the `startUrls` or in the `store` field. To specify the store ID in the url, please use this format `;store=123`. If there's no store specified in a URL, the value specified in the seperate `store` parameter will be used.
If, an URL does not includes the store ID as specified previously, and when there's no global store ID parametr, the URL will be skipped.

### Output

Output is stored in a dataset. Each item is information about a product. 

#### ⚠️ Note about `deepSearch`
Note that `deepSearch` parameter only makes sense when scraping categories and/or search results pages; if it's checked (true) then the scraper would open each product result item's page and scrape it, otherwise (the default) it will scrape product's information which are available in categries/search results pages, which in most cases (99%) sufffisant. 
If the `deepSearch` attribute is checked, an example result may look like [this](https://pastebin.com/Xe3NdriJ). 
If the `deepSearch` attribute is not checked, an example result may look like [this](https://pastebin.com/YFz3E0q3).

### Changelog

This Canadiantire scraper is at version 1.0.0.

It's actively maintained and regularly updated. The list of changes would be noted in this section upon scraper's updates.

# Actor input Schema

## `startUrls` (type: `array`):

URLs to start with
## `store` (type: `string`):

The store ID
## `deepSearch` (type: `boolean`):

If true, the scraper will follow the product links in the result page(s) and then scrape all available details. If false, it will only scrape the products at the results pages's level
## `language` (type: `string`):

Select language / Choisir la langue

## Actor input object example

```json
{
  "startUrls": [
    {
      "url": "https://www.canadiantire.ca/en/pdp/mastercraft-8-gallon-oil-free-portable-air-compressor-150-psi-1-5hp-0589316p.html?loc=plph;store=650"
    }
  ],
  "language": "en"
}
````

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
        {
            "url": "https://www.canadiantire.ca/en/pdp/mastercraft-8-gallon-oil-free-portable-air-compressor-150-psi-1-5hp-0589316p.html?loc=plph;store=650"
        }
    ]
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/canadiantire-ca-scraper").call(input);

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
run_input = { "startUrls": [{ "url": "https://www.canadiantire.ca/en/pdp/mastercraft-8-gallon-oil-free-portable-air-compressor-150-psi-1-5hp-0589316p.html?loc=plph;store=650" }] }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/canadiantire-ca-scraper").call(run_input=run_input)

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
    {
      "url": "https://www.canadiantire.ca/en/pdp/mastercraft-8-gallon-oil-free-portable-air-compressor-150-psi-1-5hp-0589316p.html?loc=plph;store=650"
    }
  ]
}' |
apify call azzouzana/canadiantire-ca-scraper --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/canadiantire-ca-scraper",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
