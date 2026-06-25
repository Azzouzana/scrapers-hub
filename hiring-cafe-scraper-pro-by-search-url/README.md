# 🚀 Hiring.cafe Job Listings Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Hiring.cafe Job Listings Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/hiring-cafe-scraper-pro-by-search-url?fpr=cbgdsf)

---

## Hiring.cafe Job Listings Scraper (By Search URL)

### ⚡ Features

Input a search URL to automate exports to Excel, Google Sheets, or custom AI/LLM workflows. The system handles automated pagination and duplicate filtering for up to **10,000 jobs** per execution.

* **High-Speed Extraction**: Processes hundreds of records in seconds with optimized execution.
* **Granular Data Schema**: Captures over 120 data points per job, including compensation hints, company context, and workplace type.
* **Rich Metadata**: Provides comprehensive field coverage for complex reporting and spreadsheet-based analysis.
* **Operational Integrity**: Engineered for stability and reliability by specialists in advanced web scraping and reverse engineering.

### 🛠️ How to use this actor

1. [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) — no credit card required.  
2. Open the actor, fill in **Input**, start a run.  
3. Free tier is enough to sanity-check field coverage.

**startUrl:** On Hiring.cafe, apply your filters, then copy the entire address bar URL from the hiring.cafe site.  
- Example: `https://hiring.cafe/?searchState=%7B%22licensesAndCertifications%22%3A%5B%22registered+nurse+%28rn%29%22%5D%7D`

**maxItems** caps how many jobs to collect.

**fetchDescriptions** (checkbox, default **off**): fetches the full job posting text for each listing and merges it into `job_information_description`. Disable it to skip the extra per-job API calls and run faster.

### 💰 Cost of usage

**$1 per 1,000 jobs** scraped, no hidden fees.

| Jobs scraped | Cost |
| :-------: | :---: |
| 250 | ~$0.25 |
| 1,000 | ~$1.00 |

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

Paid plans remove those caps. [Subscribe to enjoy unliomited scraping!](https://apify.com/pricing?fpr=cbgdsf)!

### 📥 Input

| Field | Type | Description | Example |
| ----- | ---- | ----------- | ------- |
| `startUrl` | Text | Full search URL from the browser | `https://hiring.cafe/?searchState=…` |
| `fetchDescriptions` | Checkbox | Fetch full job description text per listing (default **off**) | `false` |
| `maxItems` | Number | Max jobs to extract (up to **10,000** on a single run) | `50` |

### 📦 Output

One dataset row per job.

Example (field set varies by listing):

```json
{
	"id": "workable___visium_sa___101d0825-fcae-4f18-8d5e-682671f71e6f",
	"board_token": "visium_sa",
	"source": "workable",
	"apply_url": "https://jobs.workable.com/view/2ZpwuJNZFNGys2BMY711yg/ai-software-engineer-in-barcelona-at-visium-sa",
	"source_and_board_token": "workable_visium_sa",
	"job_information_title": "AI Software Engineer",
	"job_information_job_title_raw": "AI Software Engineer",
	"job_information_description": "Title: AI Software EngineerType: Full-timeLocation: BarcelonaStart date: June 2026About usAt Visium, we enable enterprise executives in defining their AI & Data strategy, execute large scale transformations and implement AI across operations, ensuring their organization becomes future-proof.With expertise in strategy, architecture, cloud engineering, analytics, artificial intelligence and machine learning, we empower our clients to unleash and scale the power of their data.We’re on a mission to pioneer a bright future and build future-proof and ethical organizations . Join the curious, the ambitious, the doers, the good-hearted, the ones who build a world we’re all in awe of – our Visiumees.Ready to become one?RoleAs an AI Software Engineer at Visium, you will be the driving force behind designing, developing, and productionalising AI solutions that deliver real business value to our clients. You are the engineering authority on the team - setting the bar for code quality, architectural decisions, and modern AI patterns while actively growing the people around you.As an AI Software Engineer you will:Lead complex, end-to-end AI software engineering projects from scoping through production deployment.Collaborate closely with senior client stakeholders to translate business objectives into sound technical trade-offs.Mentor colleagues through code reviews, pair programming, and hands-on guidance.Champion and actively drive the adoption of best practices in software engineering across all practice areas.Contribute to internal knowledge sharing through tech talks, documentation, and community-of-practice sessions.Support internal R&D initiatives and contribute to Visiumee's capability development.",
	"v5_processed_job_data_core_job_title": "AI Software Engineer",
	"v5_processed_job_data_requirements_summary": "5+ years software engineering; Python core; AI/ML productiona lization; cloud infra; strong communication.",
	"v5_processed_job_data_technical_tools": [
		"Python",
		"AI/ML frameworks",
		"AWS",
		"Azure",
		"GCP"
	],
	"v5_processed_job_data_licenses_or_certifications": [],
	"v5_processed_job_data_associates_degree_requirement": "Not Mentioned",
	"v5_processed_job_data_associates_degree_fields_of_study": [],
	"v5_processed_job_data_bachelors_degree_requirement": "Not Mentioned",
	"v5_processed_job_data_bachelors_degree_fields_of_study": [],
	"v5_processed_job_data_masters_degree_requirement": "Not Mentioned",
	"v5_processed_job_data_masters_degree_fields_of_study": [],
	"v5_processed_job_data_doctorate_degree_requirement": "Not Mentioned",
	"v5_processed_job_data_doctorate_degree_fields_of_study": [],
	"v5_processed_job_data_licenses_or_certifications_not_mentioned": true,
	"v5_processed_job_data_min_industry_and_role_yoe": 5,
	"v5_processed_job_data_401k_matching": false,
	"v5_processed_job_data_is_min_industry_and_role_yoe_not_mentioned": false,
	"v5_processed_job_data_min_management_and_leadership_yoe": null,
	"v5_processed_job_data_is_min_management_and_leadership_yoe_not_mentioned": true,
	"v5_processed_job_data_job_category": "Software Development",
	"v5_processed_job_data_role_activities": [
		"Lead projects",
		"Collaborate with stakeholders",
		"Mentor teammates"
	],
	"v5_processed_job_data_commitment": [
		"Full Time"
	],
	"v5_processed_job_data_role_type": "Individual Contributor",
	"v5_processed_job_data_seniority_level": "Senior Level",
	"v5_processed_job_data_workplace_countries": [
		"ES"
	],
	"v5_processed_job_data_boundless_workplace_states": [],
	"v5_processed_job_data_boundless_workplace_countries": [],
	"v5_processed_job_data_boundless_workplace_continents": [],
	"v5_processed_job_data_workplace_continents": [
		"Europe"
	],
	"v5_processed_job_data_workplace_states": [
		"Catalonia, ES"
	],
	"v5_processed_job_data_workplace_cities": [
		"Barcelona, Catalonia, ES"
	],
	"v5_processed_job_data_workplace_counties": [
		"/ County, Catalonia, ES"
	],
	"v5_processed_job_data_workplace_type": "Onsite",
	"v5_processed_job_data_workplace_physical_environment": "Office",
	"v5_processed_job_data_oral_communication_level": "High",
	"v5_processed_job_data_physical_labor_intensity": "Low",
	"v5_processed_job_data_physical_position": "Sitting",
	"v5_processed_job_data_computer_usage": "High",
	"v5_processed_job_data_cognitive_demand": "High",
	"v5_processed_job_data_air_travel_requirement": "None",
	"v5_processed_job_data_land_travel_requirement": "None",
	"v5_processed_job_data_morning_shift_work": "Not Indicated",
	"v5_processed_job_data_evening_shift_work": "Not Indicated",
	"v5_processed_job_data_overnight_work": "Not Indicated",
	"v5_processed_job_data_formatted_workplace_location": "Barcelona, Catalonia, Spain",
	"v5_processed_job_data_on_call_requirement": "None",
	"v5_processed_job_data_weekend_availability_required": false,
	"v5_processed_job_data_holiday_availability_required": false,
	"v5_processed_job_data_generous_paid_time_off": false,
	"v5_processed_job_data_four_day_work_week": false,
	"v5_processed_job_data_overtime_required": false,
	"v5_processed_job_data_is_workplace_worldwide_ok": false,
	"v5_processed_job_data_language_requirements": [
		"English"
	],
	"v5_processed_job_data_num_language_requirements": 1,
	"v5_processed_job_data_number_of_workplace_cities": 1,
	"v5_processed_job_data_number_of_workplace_counties": 1,
	"v5_processed_job_data_number_of_workplace_states": 1,
	"v5_processed_job_data_number_of_workplace_countries": 1,
	"v5_processed_job_data_number_of_workplace_continents": 1,
	"v5_processed_job_data_yearly_max_compensation": null,
	"v5_processed_job_data_yearly_min_compensation": null,
	"v5_processed_job_data_monthly_max_compensation": null,
	"v5_processed_job_data_monthly_min_compensation": null,
	"v5_processed_job_data_weekly_max_compensation": null,
	"v5_processed_job_data_weekly_min_compensation": null,
	"v5_processed_job_data_hourly_max_compensation": null,
	"v5_processed_job_data_hourly_min_compensation": null,
	"v5_processed_job_data_bi-weekly_min_compensation": null,
	"v5_processed_job_data_bi-weekly_max_compensation": null,
	"v5_processed_job_data_daily_min_compensation": null,
	"v5_processed_job_data_daily_max_compensation": null,
	"v5_processed_job_data_estimated_publish_date": "2026-04-30T07:39:32.095Z",
	"v5_processed_job_data_estimated_publish_date_millis": 1777534772095,
	"v5_processed_job_data_fair_chance": false,
	"v5_processed_job_data_visa_sponsorship": false,
	"v5_processed_job_data_relocation_assistance": false,
	"v5_processed_job_data_military_veterans": false,
	"v5_processed_job_data_tuition_reimbursement": false,
	"v5_processed_job_data_retirement_plan": false,
	"v5_processed_job_data_generous_parental_leave": false,
	"v5_processed_job_data_is_high_school_required": false,
	"v5_processed_job_data_is_driver_license_required": false,
	"v5_processed_job_data_is_compensation_transparent": false,
	"v5_processed_job_data_listed_compensation_currency": "",
	"v5_processed_job_data_listed_compensation_frequency": "Yearly",
	"v5_processed_job_data_security_clearance": "None",
	"v5_processed_job_data_position_employer_type": "External Position",
	"v5_processed_job_data_company_name": "Visium SA",
	"v5_processed_job_data_company_website": "visium.ch",
	"v5_processed_job_data_company_sector_and_industry": "Information Technology",
	"v5_processed_job_data_company_activities": [
		"AI consulting",
		"Data transformation"
	],
	"v5_processed_job_data_company_tagline": "A fast-growing AI and data transformation consultancy.",
	"enriched_company_data_enriched_at": "2026-03-11T19:53:07.761Z",
	"enriched_company_data_status": "VALID_COMPANY",
	"enriched_company_data_name": "Visium",
	"enriched_company_data_homepage_uri": "visium.ch",
	"enriched_company_data_hq_country": "CH",
	"enriched_company_data_parent_company": null,
	"enriched_company_data_subsidiaries": [
		"Visium Labs"
	],
	"enriched_company_data_industries": [
		"Artificial Intelligence",
		"IT Services"
	],
	"enriched_company_data_activities": [
		"Artificial Intelligence Consulting",
		"Data Engineering",
		"Machine Learning Development",
		"Cloud Computing Services",
		"Software Development"
	],
	"enriched_company_data_nb_employees": 80,
	"enriched_company_data_year_founded": 2018,
	"enriched_company_data_tagline": "Swiss specialized consultancy providing production-grade artificial intelligence solutions.",
	"enriched_company_data_organization_type": "Private",
	"enriched_company_data_latest_funding_investors": null,
	"enriched_company_data_latest_funding_type": null,
	"enriched_company_data_latest_funding_year": null,
	"enriched_company_data_latest_funding_amount": null,
	"enriched_company_data_stock_exchange": null,
	"enriched_company_data_stock_symbol": null,
	"_geoloc": [
		{
			"lat": 41.3879,
			"lon": 2.16992
		}
	],
	"requisition_id": "s9jsvp921heg35z7",
	"collapse_key": "e961b334fa5fefc5c0599ced6a874194baf08ae189ff01d6ece3e8798bb411e8",
	"is_expired": false,
	"objectID": "workable___visium_sa___101d0825-fcae-4f18-8d5e-682671f71e6f"
}
````

### ⚠️ Limitations

- One search URL tops out around **10,000** unique jobs per run on paid tiers; free tier is lower. Split filters or run again if you need more.
- Hiring.cafe can change; message us if something breaks.
- Only **public** data from normal search.
- **Not affiliated** with Hiring.cafe (see disclaimer).

### 🔍 SEO keywords

Hiring.cafe scraper, hiringcafe, hiringcafe scraper, hiring cafe jobs, scrape hiring cafe, Hiring cafe api, hiring cafe CSV, hiring cafe JSON, Apify hiring cafe, job listings scraper, tech jobs dataset

***

**Need a custom solution? Have a feature request or just want to chat?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

### ⚖️ Disclaimer

Independent tool, not affiliated with or endorsed by Hiring.cafe. Names and trademarks belong to their owners.

# Actor input Schema

## `startUrl` (type: `string`):

Copy the browser URL for the hiring.cafe search you want

## `fetchDescriptions` (type: `boolean`):

When enabled, loads the full job description text from hiring.cafe's job-description API and merges it into each row (extra request per job). Disable for faster runs.

## `maxItems` (type: `integer`):

How many unique jobs to extract

## Actor input object example

```json
{
  "startUrl": "https://hiring.cafe/?searchState=%7B%22sortBy%22%3A%22date%22%2C%22dateFetchedPastNDays%22%3A2%7D",
  "fetchDescriptions": false,
  "maxItems": 5000
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
    "startUrl": "https://hiring.cafe/?searchState=%7B%22sortBy%22%3A%22date%22%2C%22dateFetchedPastNDays%22%3A2%7D",
    "maxItems": 5000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/hiring-cafe-scraper-pro-by-search-url").call(input);

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
    "startUrl": "https://hiring.cafe/?searchState=%7B%22sortBy%22%3A%22date%22%2C%22dateFetchedPastNDays%22%3A2%7D",
    "maxItems": 5000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/hiring-cafe-scraper-pro-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://hiring.cafe/?searchState=%7B%22sortBy%22%3A%22date%22%2C%22dateFetchedPastNDays%22%3A2%7D",
  "maxItems": 5000
}' |
apify call azzouzana/hiring-cafe-scraper-pro-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/hiring-cafe-scraper-pro-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
