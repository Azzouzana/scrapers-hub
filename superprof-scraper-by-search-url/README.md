# 🚀 Superprof Scraper - Global Teacher & Tutor Data Extractor

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Superprof Scraper - Global Teacher & Tutor Data Extractor. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/superprof-scraper-by-search-url?fpr=cbgdsf)

---

## Superprof Scraper - Global Teacher & Tutor Data Extractor

### 🚀 Overview

The **Superprof Scraper** is a powerful tool designed to extract detailed teacher and tutor profiles from **Superprof
domains worldwide** (e.g., `.com`, `.fr`, `.es`, `.co.uk`, `.ae`, etc.).

**Key Features:**

* **🌍 Global Support**: Works seamlessly on any Superprof domain, automatically handling country differences.
* **⚡ Fast & Efficient**: **Streaming output** means you get data item-by-item immediately as it flows in.
* **📄 Deep Details**: Flattens complex nested structures into a clean, easy-to-use format.
* **✅ Reliable**: Built to be robust and stable for large-scale data extraction.

### 📥 Input Parameters

The actor accepts the following input parameters:

| Parameter | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `startUrl` | String | **Required** | The Superprof search results URL (e.g., `https://www.superprof.ae/s/nutrition,United-Arab-Emirates,,,,.html`). |
| `maxPagesToScrape` | Integer | `1000` | Maximum number of pagination pages to traverse. |
| `fetchTeacherDetails` | Boolean | `false` | If `true`, visits each profile to scrape full details (experience, review, subjects etc.). |

### 📊 Sample Output

The actor delivers a **highly simplified, flattened, and sorted JSON** object for each teacher. Here is a real example
of the output structure:

- With `fetchTeacherDetails` set to `true`:

```json
{
  "badge": "Experienced",
  "city": "Ojodu Berger",
  "contact_label": "Book a class",
  "contact_url": "https://www.superprof.ae/connections-your-request-7237127.html?src=app_v2",
  "country": "",
  "creation_date": "2020-12-16 04:49:47",
  "cv": "",
  "department": "Lagos",
  "distance": "",
  "emails": [],
  "experience": "I am a Quantity Surveyor but I derive pleasure in adding value through skin care and body relaxation to people...",
  "explications": "",
  "faceToFace": true,
  "firstFreeDuration": "1hr",
  "firstHourFree": 1,
  "gallery": [
    "https://c.superprof.com/i/a/14210001/7237127/300/20220718092409/choose-live-healthy-with-ravishing-skin-and-healthy-mind-set-each-day.jpg"
  ],
  "has_all_levels": true,
  "has_interview": false,
  "has_valid_diploma": false,
  "has_video": false,
  "id_annonce": "7237127",
  "interview": {
    "questions": []
  },
  "is_ambassador": false,
  "is_available": true,
  "is_feminin": 1,
  "is_star": false,
  "is_superprof": true,
  "is_verified_member": true,
  "landing_url": "https://www.superprof.ae/lessons/nutrition/united-arab-emirates/",
  "lat": null,
  "lng": null,
  "levels": [
    "Beginner",
    "Intermediate",
    "Advanced",
    "Children"
  ],
  "native_language": false,
  "offer_lesson_first_is_free": true,
  "offer_lesson_first_lesson_duration": "60",
  "offers": {
    "lesson": {
      "first_is_free": true,
      "first_lesson_duration": "60"
    }
  },
  "price": "1",
  "price_1H": 500,
  "price_5H": 0,
  "price_10H": 0,
  "price_webcam": 0,
  "price_with_travel": 0,
  "prices": {
    "1H": 500,
    "5H": 0,
    "10H": 0,
    "webcam": 0,
    "with_travel": 0
  },
  "rating_count": 4,
  "rating_label": "4 Reviews",
  "rating_score": 5,
  "responseTime": 1,
  "responseTimeDesc": "Responds in 1 hour",
  "response_rate": "100.00",
  "response_time_sec": 0,
  "reviews": [
    {
      "id": "1719159",
      "author": "Ummuhani",
      "avatar": "https://c.superprof.com/i/m/13253883/50/20220419122700/13253883.jpg",
      "comment": "She is very nice and took her time to answer all my questions...",
      "rating": 5,
      "date": "2025-06-20 14:06:30",
      "answers": [
        {
          "id": "1713820",
          "comment": "She is a respectful and ready-to-learn individual",
          "relative_date": "7 months ago",
          "date": "2025-06-13 13:42:46",
          "stars": "5"
        }
      ]
    }
  ],
  "search_url": "https://www.superprof.ae/s/nutrition,United-Arab-Emirates,,,,.html",
  "senior": false,
  "sex": "F",
  "stat_count_favorite": "1",
  "stat_count_recommendations": "1",
  "stat_count_reviews": "3",
  "stat_count_total_links": 13,
  "stat_stars": 5,
  "status": "1",
  "subjects": [
    "Nutrition",
    "Weightloss",
    "Learning to eat well",
    "Dietetics",
    "Alternative Medicine"
  ],
  "teacherCity": "Ojodu Berger",
  "teacherName": "Mary",
  "teacherPhoto": "https://c.superprof.com/i/a/14210001/7237127/600/20220718092409/choose-live-healthy-with-ravishing-skin-and-healthy-mind-set-each-day.jpg",
  "teaching": "My teaching method is by approaching each topic with practical and physical examination...",
  "title": "Choose to live healthy with ravishing skin and healthy mindset each day",
  "type": "webcam",
  "update_date": "2022-07-18 09:24:10",
  "url": "choose-live-healthy-with-ravishing-skin-and-healthy-mind-set-each-day",
  "url_mer": "https://www.superprof.ae/connections-your-request-7237127.html",
  "venue_can_move": true,
  "venue_can_receive": true,
  "venue_can_receive_individually": false,
  "venue_can_receive_several_students": true,
  "venue_max_distance": "10",
  "verified": 1,
  "video": false,
  "webcam": true
}
````

- With `fetchTeacherDetails` set to `false`:

```json
{
  "badge": "Erfahrene Lehrkraft",
  "distance": "",
  "faceToFace": true,
  "firstFreeDuration": "1h",
  "firstHourFree": 1,
  "gallery": [
    "https://c.superprof.com/i/m/10384745/30/20251208172134/10384745.jpg",
    "https://c.superprof.com/i/m/10384745/50/20251208172134/10384745.jpg",
    "https://c.superprof.com/i/m/10384745/100/20251208172134/10384745.jpg",
    "https://c.superprof.com/i/m/10384745/140/20251208172134/10384745.jpg",
    "https://c.superprof.com/i/m/10384745/160/20251208172134/10384745.jpg",
    "https://c.superprof.com/i/m/10384745/200/20251208172134/10384745.jpg",
    "https://c.superprof.com/i/m/10384745/300/20251208172134/10384745.jpg",
    "https://c.superprof.com/i/m/10384745/500/20251208172134/10384745.jpg",
    "https://c.superprof.com/i/m/10384745/600/20251208172134/10384745.jpg"
  ],
  "id_annonce": "16784482",
  "is_feminin": 0,
  "price": "70",
  "rating_count": 3,
  "rating_label": "3 Bewertungen",
  "rating_score": 5,
  "responseTime": 1,
  "responseTimeDesc": "Antwortet innerhalb 1 Stunde",
  "senior": false,
  "teacherCity": "Berlin",
  "teacherName": "Marcel",
  "teacherPhoto": "https://c.superprof.com/i/a/10384745/16784482/600/20251208172134/kreuzband-und-wirbelsaulenrehabilitation-ich-helfe-dir-wieder-auf-die-beine-mit-einem-individuellen-und-wissenschaftlich-fundierten.jpg",
  "title": "Kreuzband- und Wirbelsäulenrehabilitation! Ich helfe dir wieder auf die Beine mit...",
  "type": "webcam",
  "url": "https://www.superprof.de/kreuzband-und-wirbelsaulenrehabilitation-ich-helfe-dir-wieder-auf-die-beine-mit-einem-individuellen-und-wissenschaftlich-fundierten.html",
  "url_mer": "https://www.superprof.de/vermittlung-ihre-anfrage-16784482.html",
  "verified": 1,
  "webcam": true
}
```

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

***

#### SEO Keywords

Superprof Scraper, Tutor Data Extractor, Teacher Lead Generation, Education Scraper, Apify Superprof Actor, Global Tutor
Database.

# Actor input Schema

## `startUrl` (type: `string`):

The initial search URL from Superprof (e.g., https://www.superprof.co.in/s/biology,India,,,,.html?s=1\&l=1)

## `maxPagesToScrape` (type: `integer`):

Maximum number of pages to scrape (default: 1).

## `fetchTeacherDetails` (type: `boolean`):

If true, fetches detailed information (reviews, experiences, prices etc.) for each teacher. Increases scraping time.

## Actor input object example

```json
{
  "startUrl": "https://www.superprof.co.in/s/biology,India,,,,.html?s=1&l=1",
  "maxPagesToScrape": 1,
  "fetchTeacherDetails": false
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
    "startUrl": "https://www.superprof.co.in/s/biology,India,,,,.html?s=1&l=1"
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/superprof-scraper-by-search-url").call(input);

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
run_input = { "startUrl": "https://www.superprof.co.in/s/biology,India,,,,.html?s=1&l=1" }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/superprof-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.superprof.co.in/s/biology,India,,,,.html?s=1&l=1"
}' |
apify call azzouzana/superprof-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/superprof-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
