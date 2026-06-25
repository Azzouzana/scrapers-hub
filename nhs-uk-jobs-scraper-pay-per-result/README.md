# 🚀 NHS UK Jobs Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the NHS UK Jobs Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/nhs-uk-jobs-scraper-pay-per-result?fpr=cbgdsf)

---

## NHS UK Jobs Scraper (By Search URL)

A high-performance Apify Actor for scraping job listings from `jobs.nhs.uk`.

### Features
-   **Pay-Per-Event (PPE) Pricing**: Uses minimal resources, charged efficiently based on usage.
-   **Strict Capping**: Respects `maxItems` limits precisely to manage costs.

### Input Configuration

| Field | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| `startUrl` | String | A valid NHS Jobs search URL (e.g., filtered by location/keyword). | (Example URL) |
| `maxItems` | Integer | Maximum number of items to scrape. Stops fetching pages once reached. | 100 |

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

### Output

Data is stored in the default dataset. Example format:
```json
{
	"id": "J1234-26-5678",
	"url": "https://www.jobs.nhs.uk/candidate/jobadvert/J1234-26-5678",
	"title": "Clinical Nurse Specialist",
	"employer": "Central London NHS Foundation Trust",
	"closing_date_text": "15 March 2026",
	"closing_date": "20260315",
	"job_summary": "We are looking for an experienced Clinical Nurse Specialist to join our Cardiology team. You will be responsible for providing specialist nursing advice and support to patients...",
	"main_duties_of_the_job": "The post holder will act as a key worker for patients with heart failure, providing expert clinical care and management...",
	"about_us": "Central London NHS Foundation Trust is a leading provider of community and specialist health services...",
	"job_description": "Job responsibilities include conducting clinics, participating in MDT meetings, and contributing to service development...",
	"person_specification": [
		{
			"category": "Experience",
			"essentials": [
				"Significant experience in Cardiology nursing",
				"Experience in managing a caseload"
			]
		},
		{
			"category": "Qualifications",
			"essentials": [
				"Registered Nurse (NMC)",
				"Post-graduate qualification in Cardiology"
			]
		}
	],
	"employer_details": {
		"name": "Central London NHS Foundation Trust",
		"address": [
			"123 Hospital Way",
			"London",
			"SW1A 1AA"
		],
		"website": "https://www.sample-nhs-trust.nhs.uk/"
	},
	"contact_details": {
		"job_title": "Matron",
		"name": "Jane Doe",
		"email": "jane.doe@nhs.net",
		"phone": "020 7123 4567"
	},
	"date_posted": "20260201",
	"date_posted_text": "01 February 2026",
	"pay_scheme": "Agenda for change",
	"salary": "£43,742 to £50,056 a year",
	"contract_type": "Permanent",
	"working_pattern": "Full-time",
	"contract_duration": null,
	"reference_number": "J1234-26-5678",
	"supporting_documents": ["..."],
	"privacy_policy": null
}
````

# Actor input Schema

## `startUrl` (type: `string`):

Jobs Search results page URL

## `maxItems` (type: `integer`):

Maximum number of jobs to scrape.

## Actor input object example

```json
{
  "startUrl": "https://www.jobs.nhs.uk/candidate/search/results?keyword=agency&location=london&language=en&skipPhraseSuggester=true",
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
    "startUrl": "https://www.jobs.nhs.uk/candidate/search/results?keyword=agency&location=london&language=en&skipPhraseSuggester=true",
    "maxItems": 2000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/nhs-uk-jobs-scraper-pay-per-result").call(input);

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
    "startUrl": "https://www.jobs.nhs.uk/candidate/search/results?keyword=agency&location=london&language=en&skipPhraseSuggester=true",
    "maxItems": 2000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/nhs-uk-jobs-scraper-pay-per-result").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.jobs.nhs.uk/candidate/search/results?keyword=agency&location=london&language=en&skipPhraseSuggester=true",
  "maxItems": 2000
}' |
apify call azzouzana/nhs-uk-jobs-scraper-pay-per-result --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/nhs-uk-jobs-scraper-pay-per-result",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
