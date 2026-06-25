# 🚀 Actor input object example

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Actor input object example. This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/rumble-all-inclusive-scraper?fpr=cbgdsf)

---

### 🤩 Features

🚀 Our blazing fast Rumble All-inclusive scraper lets you extract:

- **Channels**: Details (stats, social links, emails, joined date & much more) by providing a channel URL.
- **Channel Videos**: Scrape all videos from a channel.
- **Channel Playlists**: Scrape all playlists from a channel.
- **Videos**: Details (comments, reactions, publisher, revenue & much more) by providing video URLs.
- **Search**: Top search results (Channels, Users, Videos & much more) with enriched metadata.
- **Playlists**: Playlist metadata or all videos within a playlist.
- **Trending & Editor Picks**: Scrape trending and curated video lists.

### 🤔 Why scrape Rumble?

1. **Content Aggregation**
   Collect video data, descriptions, tags, and categories to create a centralized database or catalog of content for analytics, comparisons, or integrations with other platforms.

2. **Competitive Analysis**
   Monitor trending videos, creators, and engagement metrics (likes, views, comments) to analyze content strategies and audience preferences on the platform.

3. **Market Research**
   Extract data to study popular topics, niches, and user behavior on Rumble, which can be valuable for marketers or businesses targeting video-based advertising or partnerships.

4. **Sentiment Analysis**
   Scrape comments and engagement data to perform sentiment analysis on audience reactions, helping understand opinions and trends in specific topics or videos.

5. **Content Discovery for Reposting/Ideas**
   Identify unique or trending videos that can inspire content creation or repurposing ideas for other platforms, such as YouTube, TikTok, or blogs.

6. **Trend Spotting**
   Keep track of viral videos, creators, or categories to stay ahead of emerging trends and adapt content or business strategies accordingly.

Sky is the limit 🚀

### 🛠️ Input

| Field | Type | Description | Default value / Example |
| ----- | ---- | ----------- | -------------|
| `startUrls` | `array` | Either Channel URLs, Video URLs, Playlist URLs, or Search URLs | `https://rumble.com/v5k5rcr-donald-trump-tells-joe-rogan-his-nfl-best-bets-for-this-weekend.html` |
| `scrapeChannelVideos` | `boolean` | **Channel URLs Only**: If true, scrapes *only* videos from the channel. If false (default), scrapes *only* channel metadata. | `false` |
| `scrapeChannelPlaylists` | `boolean` | **Channel URLs Only**: If true, scrapes *only* playlists from the channel. Overrides metadata scraping if `scrapeChannelVideos` is false. | `false` |
| `maxVideoToScrapeFromChannel` | `number` | The maximum number of videos to scrape. Only applies when `scrapeChannelVideos` is true. | `10` |
| `scrapePlaylistVideos` | `boolean` | **Playlist URLs Only**: If true, scrapes *only* videos from the playlist. If false (default), scrapes *only* playlist metadata. | `false` |
| `maxVideoToScrapeFromPlaylist` | `number` | The maximum number of videos to scrape. Only applies when `scrapePlaylistVideos` is true. | `10` |
| `maxSearchResults` | `number` | The maximum number of results to scrape. Applies to Search, Trending, and Editor Picks URLs. | `20` |

#### Input Logic
To ensure clarity, the scraper uses strict exclusive modes for Channels and Playlists:
*   **Channels**:
    *   Default: Scrapes **Channel Metadata** (including flattened socials, email, stats).
    *   `scrapeChannelVideos = true`: Scrapes **Videos** only.
    *   `scrapeChannelPlaylists = true`: Scrapes **Playlist Metadata** only.
*   **Playlists**:
    *   Default: Scrapes **Playlist Metadata**.
    *   `scrapePlaylistVideos = true`: Scrapes **Videos** only.

### 🧐 Output

Output is stored in a dataset. Each item is information about a channel, video, user, or playlist. The output is **flat**, meaning no nested lists of items.

#### Sample output

An output might look like the below screenshot:

- Video:

![video screenshot](https://i.ibb.co/Trwkrq0/image.png)

- Channel:

![channel screenshot](https://i.ibb.co/R2xRFf3/image.png)

- Playlist:

![playlist screenshot](https://i.ibb.co/vh3LZSf/image.png)

### Updates

The **Rumble scraper All-inclusive scraper** actor is actively maintained and regularly updated.

### 🔎 SEO Keywords
`Rumble Scraper`, `Rumble Video Downloader`, `Rumble Channel Crawler`, `Social Media Data Extraction`, `Marketing Intelligence Tool`, `Sentiment Analysis`, `Apify Actor`, `Rumble Playlists`, `Video Metadata`, `Competitor Analysis`.

#### 📬 Contact & Custom Solutions
Want to chat? Don't hesitate to reach out to us:
- **Discord**: `@azzouzana`
- **Email**: `labs@azzouzana.com`

# Actor input Schema

## `startUrls` (type: `array`):

URLs to start with. Supports Channels, Videos, Playlists, or Search URLs.
## `maxSearchResults` (type: `integer`):

The maximum number of results to scrape. Applies to Search, Trending, and Editor Picks URLs.
## `scrapeChannelVideos` (type: `boolean`):

Channel URLs Only: If true, scrapes *only* videos from the channel. If false (default), scrapes *only* channel metadata.
## `scrapeChannelPlaylists` (type: `boolean`):

Channel URLs Only: If true, scrapes *only* playlists from the channel. Overrides metadata scraping if `scrapeChannelVideos` is false.
## `maxVideoToScrapeFromChannel` (type: `integer`):

The maximum number of videos to scrape. Only applies when `scrapeChannelVideos` is true.
## `scrapePlaylistVideos` (type: `boolean`):

Playlist URLs Only: If true, scrapes *only* videos from the playlist. If false (default), scrapes *only* playlist metadata.
## `maxVideoToScrapeFromPlaylist` (type: `integer`):

The maximum number of videos to scrape. Only applies when `scrapePlaylistVideos` is true.

## Actor input object example

```json
{
  "startUrls": [
    "https://rumble.com/c/c-6547556"
  ],
  "maxSearchResults": 20,
  "scrapeChannelVideos": false,
  "scrapeChannelPlaylists": false,
  "maxVideoToScrapeFromChannel": 10,
  "scrapePlaylistVideos": false,
  "maxVideoToScrapeFromPlaylist": 10
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
        "https://rumble.com/c/c-6547556"
    ]
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/rumble-all-inclusive-scraper").call(input);

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
run_input = { "startUrls": ["https://rumble.com/c/c-6547556"] }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/rumble-all-inclusive-scraper").call(run_input=run_input)

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
    "https://rumble.com/c/c-6547556"
  ]
}' |
apify call azzouzana/rumble-all-inclusive-scraper --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/rumble-all-inclusive-scraper",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
