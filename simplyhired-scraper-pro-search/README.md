# 🚀 SimplyHired Scraper PRO 🚀 (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the SimplyHired Scraper PRO 🚀 (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/simplyhired-scraper-pro-search?fpr=cbgdsf)

---

## SimplyHired Scraper PRO 🚀 (By Search URL)

**Key Features:**
*   **🇺🇸 Global Coverage**: Works with **all SimplyHired domains** (`.com`, `.fr`, `.ca`, `.in`, etc.)
*   **⚡ Fast & Efficient**: Scrapes search results quickly, navigating pagination automatically.
*   **📄 Deep Details**: Optionally visits every job page to extract the
*   **Comprehensive Data**: Extracts a wide range of job details including company information, location, salary, benefits, job types, and much more.

### 📥 Input Parameters

The actor accepts the following input parameters:

| Parameter | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `searchUrl` | String | **Required** | The SimplyHired search URL (e.g., `https://www.simplyhired.com/search?q=manager&l=New+York`). |
| `fetchJobDetails` | Boolean | `false` | If `true`, visits each job profile to scrape comprehensive job's details |
| `maxPages` | Integer | `1` | Maximum number of pagination pages to traverse. |

### 🏆 Comparison

| Feature | 🚀 This Actor (Pro) | 🐢 Standard Scrapers |
| :--- | :--- | :--- |
| **⚡ Speed** | **Blazing Fast** | **Slow** (Full Browser Overhead) |
| **🧹 Duplicates** | **Auto-Deduplication** (Smart Filtering) | **High** (Repeated/Sponsored Listings) |
| **📊 Data Depth** | **Rich & Structured** (Have a look at output sample below) | **Shallow** (Misses hidden fields/meta) |
| **💰 Cost** | **Affordable & transparent - no hidden fees (`$1/1k`)** | **Expensive & Unpredictable** |

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

### 📊 Sample Output

The actor delivers a **clean, flattened JSON** object for each job. Here is an example of the output structure:

- With `fetchJobDetails` set to `true`
```json
{
	"auction": false,
	"beneficiaryName": "EPAM Systems",
	"benefits": ["..."],
	"city": "San Francisco",
	"company": "EPAM Systems, Inc.",
	"companyPageUrl": "https://www.simplyhired.com/browse-jobs/companies/Epam-Systems",
	"companyRating": 3.8,
	"compensation": "",
	"dateOnIndeed": "2025-12-30T12:38:35.909Z",
	"datePublished": "2025-12-28T10:00:00.000Z",
	"displayTitle": "Python Developer",
	"employerCompanyPageUrl": "https://www.simplyhired.com/browse-jobs/companies/Epam-Systems",
	"employerName": "EPAM Systems, Inc.",
	"employerOverallRating": 3.8,
	"employerSquareLogoUrl": "https://d2q79iu7y748jz.cloudfront.net/s/_squarelogo/128x128/89e1cba2407c644a211fdfb77316efc3",
	"encryptedEmail": "qs_vf6RRt5ml8IkVpYOcMLBaNdwEIN0v29rtLxMZnkQ",
	"expired": false,
	"formattedLocation": "San Francisco, CA",
	"indeedApply": false,
	"isIndeedApply": false,
	"jobCardTrackingKey": "5-yul1-0-1jdnk8pqmia6v800-7aa58cb8d95191f0",
	"jobDataResultTrackingKey": "5-yul1-3-1jdnk8t7b21c5i00",
	"jobDescriptionHtml": "<div><p>Join our Engineering team as a backend-focused <b>Software Engin ...",
	"jobFound": true,
	"jobKey": "SN6CyLHSmgAj7reDErWxJJryt9mXTFkghKLwOUetLHzvdWp-IX4lMA",
	"jobTitle": "Python Engineer with AWS experience",
	"jobTypes": ["..."],
	"latitude": 37.77493,
	"location": "San Francisco, CA",
	"longitude": -122.41942,
	"normalizedTitle": "python developer",
	"optionalRevenuePingURL": "",
	"qualifications": ["..."],
        "remoteAttributes": ["..."],
	"requirements": ["..."],
        "salaryInfo": "$180,000 - $300,000 a year",
	"scrapedAt": "2025-12-30T12:38:35.909Z",
	"snippet": "Design, develop, and maintain scalable microservices and APIs (Python preferred, Java secondary). Experience with payment systems, monitoring tools, or working…",
	"sponsored": false,
	"state": "CA",
	"title": "Python Engineer with AWS experience",
	"uncategorized": ["..."],
	"url": "https://www.simplyhired.com/job/SN6CyLHSmgAj7reDErWxJJryt9mXTFkghKLwOUetLHzvdWp-IX4lMA",
	"workSettings": ["..."]
}
````

- With `fetchJobDetails` set to `false`

```json
{
	"auction": false,
	"benefits": ["..."],
	"company": "MLabs",
	"companyPageUrl": "https://www.simplyhired.co.uk/browse-jobs/companies/Mlabs",
	"companyRating": 5,
	"dateOnIndeed": "2025-12-22T19:02:51.337Z",
	"indeedApply": true,
	"jobCardTrackingKey": "5-dub1-0-1jdntmk65kdr4800-4ca4106be9bc97b7",
	"jobKey": "MebGsOvO4rbcC1COSt7eX0Ii5i-RX6ItIdOtA-OMQGDW5w024IZ81g",
	"jobTypes": ["Full-time"],
	"location": "London",
	"remoteAttributes":  ["..."],
	"requirements": ["..."],
	"salaryInfo": "£250,000 - £300,000 a year",
	"scrapedAt": "2025-12-30T15:23:22.541Z",
	"snippet": "Work closely with Product, Mobile, Compliance, Risk, and Finance teams, driving features from initial concept through production deployment and iteration.",
	"sponsored": false,
	"title": "Blockchain Payments Engineer",
	"uncategorized": ["..."	],
	"url": "https://www.simplyhired.co.uk/job/MebGsOvO4rbcC1COSt7eX0Ii5i-RX6ItIdOtA-OMQGDW5w024IZ81g"
}
```

#### SEO Keywords

SimplyHired Scraper, Job Board API, Recruitment Data, HR Tech, Job Market Analysis, US Job Listings, Apify SimplyHired Actor.

#### 📬 Contact & Custom Solutions

Want to chat? Don't hesitate to reach out to us:

- **Discord**: `@azzouzana`
- **Email**: `labs@azzouzana.com`

# Actor input Schema

## `searchUrl` (type: `string`):

The SimplyHired search URL to start scraping from (e.g., https://www.simplyhired.com/search?q=java\&l=New+Braunfels%2C+TX).

## `maxPages` (type: `integer`):

Maximum number of pages to scrape.

## `fetchJobDetails` (type: `boolean`):

If enabled, the scraper will fetch the details page for each job.

## Actor input object example

```json
{
  "searchUrl": "https://www.simplyhired.com/search?q=java&l=New+Braunfels%2C+TX",
  "maxPages": 1,
  "fetchJobDetails": false
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
    "searchUrl": "https://www.simplyhired.com/search?q=java&l=New+Braunfels%2C+TX"
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/simplyhired-scraper-pro-search").call(input);

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
run_input = { "searchUrl": "https://www.simplyhired.com/search?q=java&l=New+Braunfels%2C+TX" }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/simplyhired-scraper-pro-search").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "searchUrl": "https://www.simplyhired.com/search?q=java&l=New+Braunfels%2C+TX"
}' |
apify call azzouzana/simplyhired-scraper-pro-search --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/simplyhired-scraper-pro-search",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
