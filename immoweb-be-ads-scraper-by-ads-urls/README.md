# 🚀 Immoweb.be Ads Scraper (By Listings URLs)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Immoweb.be Ads Scraper (By Listings URLs). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/immoweb-be-ads-scraper-by-ads-urls?fpr=cbgdsf)

---

## Immoweb.be Ads Scraper (By Listings URLs)

### Version française

#### 🤩 Vue d'ensemble

🚀 Extraire les informations des annonces à partir de leurs URLs et les exporter dans différents formats (JSON, CSV, HTML, etc.) 🔥 Apportez vos URLs et c'est parti !

👉 Il vous permet de récupérer des détails riches tels que: titres, descriptions, photos, prix, nombre de vues/favoris, informations énergétiques, attributes, informations de l'éditeur (e-mail/numéro de téléphone si disponible) et bien plus encore.

Tout ce dont vous avez besoin, c'est sont les liens directs vers les annonces:
- Exemple: `https://www.immoweb.be/en/classified/kot/for-rent/namur/5002/20368607`

#### Vous avez besoin de scraper les résultats de la page de recherche?

Si vous n'avez pas des liens directs vers des biens et vous avez besoin de scraper les résultats de la page de recherche (de type `https://www.immoweb.be/en/search-3-rooms/apartment/for-rent?countries=BE&maxBedroomCount=3&minBedroomCount=3&maxPrice=500&page=1&orderBy=relevance`) en uns seule fois et souhaitez en scraper les informations de manière structurée (JSON, Excel, XML, etc.), n'hésitez pas à consulter l'acteur [Immoweb.be mass scraper (by search URL) 🏠](https://apify.com/azzouzana/immoweb-be-mass-scraper-by-search-url)

#### ⚠️ Est-il légal de scraper immoweb.be ?

Il est légal de scraper les données publiquement disponibles telles que les descriptions de biens immobiliers, les prix, les photos, les transports à proximité, etc. Lisez notre article de blog sur la [légalité du web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) pour en savoir plus.

#### 🤔 Pourquoi scraper immoweb.be ?

Immoweb.be est le plus grand site immobilier en Belgique. Avec plus de 7 millions de visiteurs par mois et +1M d'annonces immobilières, il y a certainement quelque chose pour vous!

Alors, que pourriez-vous faire avec toutes ces données sur les annonces immobilières ?

- Trouver des biens immobiliers à vendre à proximité
- Faire une analyse des données du marché
- Créer une liste d'emails d'agents immobiliers
- Collecter des données sur le logement pour la recherche ou des besoins personnels
- Comparer les données collectées avec un indice de valeur des maisons
- Utiliser les données pour une analyse globale du marché immobilier

Ce ne sont que quelques idées pour vous faire réfléchir à la manière dont le web scraping peut vous fournir les données dont vous avez besoin. Les possibilités sont infinies 🚀

#### 🤑 Coût d'utilisation

Le coût d'utilisation de ce scraper est de **1.50 $ pour chaque 1000 annonces immobilières scrappées**. No hidden fees.

#### 🆓 Limites de la version gratuite

Nous voulons que vous puissiez voir comment cet acteur fonctionne avant de vous engager. Pour des raisons d'équité, la **version gratuite** inclut généralement ces limites d'essai :

- **Exemples de données :** jusqu'à **5 annonces** par exécution—assez pour vérifier la qualité des données.
- **Plafond quotidien :** **5 exécutions** par jour calendaire (UTC).
- **Entre les exécutions :** au moins **30 minutes** avant de pouvoir relancer.

> Les limites peuvent varier en fonction de la charge de la plateforme et de l'usage prévu.

##### Passez à la version supérieure quand vous êtes prêt

Utilisez la version gratuite pour décider si cet acteur correspond à votre projet. Les plans Apify payants suppriment ces délais d'attente et ces limites pour vous permettre d'exécuter à plein volume—[**passez à un plan payant**](https://apify.com/pricing?fpr=cbgdsf).

#### 🛠️ Paramètres d'entrée:

| Champ | Type | Description | Valeur par défaut / Exemple |
| ----- | ---- | ----------- | ------------- |
| `startUrls` | `tableau` | les URLs directes des biens immobiliers que l'acteur va scraper. | `https://www.immoweb.be/en/classified/kot/for-rent/namur/5002/20368607` |

#### 🧐 Résultat

Les résultats sont stockés dans un jeu de données (ou "dataset" en jargon Apify). Chaque élément contient des informations d'une annonce:

##### Exemple de résultat:

Un exemple de résultat pourrait ressembler à la capture d'écran ci-dessous :

![immowebbe scraping result](https://i.ibb.co/RCsK27K/image.png)

& plein d'autres informations que la capture d'écran ne montre pas, venez explorer!

### English version

#### 🤩 Features

🚀 Our blazing fast immoweb.be mass real estate items scraper lets you extract real estate items' information and export them to various format (JSON, CSV, HTML etc..) 🔥 Bring your URLs and you're good to go!

👉 It enables you to scrape rich details as title, descriptions, photos, energy information, construction date, price, publisher information, phone number, nearby transportation and a lot more.

The scraper has a required `startUrls` parameter which is an array containing direct URLs to real estate items:
- Example: `https://www.immoweb.be/en/classified/kot/for-rent/namur/5002/20368607`

#### ⚠️ Is it legal to scrape immoweb.be?

It is legal to scrape publicly available data such as real estate descriptions, prices, photos, nearby transportation etc. Read our blog post on [the legality of web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) to learn more.

#### Do you need to scrape search results pages instead?
If you don’t have direct links to properties and need to scrape search page results (Like `https://www.immoweb.be/en/search-3-rooms/apartment/for-rent?countries=BE&maxBedroomCount=3&minBedroomCount=3&maxPrice=500&page=1&orderBy=relevance`) all at once while wanting to gather information in a structured format (JSON, Excel, XML, etc.), feel free to check out the [immoweb.be mass products scraper (by search URL) ⚡](https://apify.com/azzouzana/pap-fr-mass-products-scraper-by-search-url)

#### 🤔 Why scrape immoweb.be?

Immoweb.be is the largest real estate website in Belgium. With over 7 million visitors per month and more than 2 million real estate listings, there's definitely something for you!

So what could you do with all these ads?

- Find real estate for sale nearby
- Do market data analysis
- Build a real estate agent email list
- Collect housing data for research or personal purposes
- Compare collected data with home value index
- Use the data for overall real estate data analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

#### 🤑 Cost of usage

The cost of usage is **$1.50 for every 1000 real estate items scraped**. No hidden fees.

#### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

##### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

#### 🛠️ Input

| Field | Type | Description | Default value / Example
| ----- | ---- | ----------- | -------------|
| `startUrls` | `array` | the direct URLs of the real estate items that the actor will scrape. | `https://www.immoweb.be/en/classified/kot/for-rent/namur/5002/20368607` |

#### 🧐 Output

Output is stored in a dataset. Each item is information about a real estate item:

##### Sample output

An output might look like the below screenshot:

![immowebbe scraping result](https://i.ibb.co/RCsK27K/image.png)

& a lot more information that the screenshot does not show, come & explore!

# Actor input Schema

## `startUrls` (type: `array`):

ads URLs

## Actor input object example

```json
{
  "startUrls": [
    "https://www.immoweb.be/en/classified/outdoor-parking-space/for-sale/genval/1332/21230269404"
  ]
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
        "https://www.immoweb.be/en/classified/outdoor-parking-space/for-sale/genval/1332/21230269404"
    ]
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/immoweb-be-ads-scraper-by-ads-urls").call(input);

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
run_input = { "startUrls": ["https://www.immoweb.be/en/classified/outdoor-parking-space/for-sale/genval/1332/21230269404"] }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/immoweb-be-ads-scraper-by-ads-urls").call(run_input=run_input)

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
    "https://www.immoweb.be/en/classified/outdoor-parking-space/for-sale/genval/1332/21230269404"
  ]
}' |
apify call azzouzana/immoweb-be-ads-scraper-by-ads-urls --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/immoweb-be-ads-scraper-by-ads-urls",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
