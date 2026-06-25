# 🚀 SeLoger Ads Scraper (By Listings URLs)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the SeLoger Ads Scraper (By Listings URLs). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/seloger-mass-products-scraper-by-items-urls?fpr=cbgdsf)

---

## SeLoger Ads Scraper (By Listings URLs)

### Version française

#### 🤩 Vue d'ensemble

🚀 Notre scraper ultra-rapide pour les annonces immobilières de masse SeLoger vous permet d'extraire les informations des biens immobiliers et de les exporter dans différents formats (JSON, CSV, HTML, etc.) 🔥 Apportez vos URLs et c'est parti !
👉 Il vous permet de récupérer des détails riches tels que les titres, descriptions, photos, informations énergétiques, date de construction, prix, informations de l'éditeur (e-mail/numéro de téléphone inclus), transports à proximité et bien plus encore
Tout ce dont vous avez besoin c'est le liens directs vers les annonces:
- Exemple: `https://www.seloger.com/annonces/achat/appartement/paris-9eme-75/lorette-martyrs/219635585.htm`

#### Vous avez besoin de scraper les résultats de la page de recherche?

Si vous n'avez pas des liens directs vers des biens et vous avez besoin de scrpaer les résultats de la page de recherche à la place, (de type `https://www.seloger.com/list?...`) et souhaitez en scraper les informations de manière structurée (JSON, Excel, XML, etc.), n'hésitez pas à consulter l'acteur [seloger mass products scraper (by search URL) ⚡](https://apify.com/azzouzana/seloger-mass-products-scraper-by-search-url)

#### ⚠️ Est-il légal de scraper SeLoger ?

Il est légal de scraper les données publiquement disponibles telles que les descriptions de biens immobiliers, les prix, les photos, les transports à proximité, etc. Lisez notre article de blog sur la [légalité du web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) pour en savoir plus.

#### 🤔 Pourquoi scraper SeLoger.com ?

SeLoger.com est le plus grand site immobilier français. Avec plus de 20 millions de visiteurs par mois et environ 200 000 annonces immobilières, il y a certainement quelque chose pour vous!

Alors, que pourriez-vous faire avec toutes ces données sur les annonces immobilières ?

- Trouver des biens immobiliers à vendre à proximité
- Faire une analyse des données du marché
- Créer une liste d'emails d'agents immobiliers
- Collecter des données sur le logement pour la recherche ou des besoins personnels
- Comparer les données collectées avec un indice de valeur des maisons
- Utiliser les données pour une analyse globale du marché immobilier

Ce ne sont que quelques idées pour vous faire réfléchir à la manière dont le web scraping peut vous fournir les données dont vous avez besoin. Les possibilités sont infinies 🚀

#### 🆓 Limitations du Plan Gratuit

Nous voulons que vous voyiez comment cet acteur fonctionne avant de vous engager. Pour garder les choses équitables pour tout le monde, le **plan gratuit** comprend généralement ces limites d'essai :

- **Données d'échantillon :** jusqu'à **5 annonces** par exécution—suffisant pour vérifier la qualité des données.
- **Limite quotidienne :** **5 exécutions** par jour civil (UTC).
- **Entre les exécutions :** au moins **30 minutes** avant de pouvoir lancer une autre exécution.

> Les limites peuvent changer en fonction de la charge du système et de votre volume de scraping prévu.

##### Mettez à niveau quand vous êtes prêt à passer à l'échelle

Utilisez le plan gratuit pour décider si cet acteur correspond à votre projet. Les plans payants d'Apify suppriment ces temps d'attente et ces plafonds pour que vous puissiez exécuter à plein volume—[**passez à un plan payant**](https://apify.com/pricing?fpr=cbgdsf).

#### 🛠️ Paramètres d'entrée:

| Champ | Type | Description | Valeur par défaut / Exemple |
| ----- | ---- | ----------- | ------------- |
| `startUrls` | `tableau` | les URL directes des biens immobiliers que l'acteur va scraper. | `https://www.seloger.com/annonces/achat/appartement/paris-9eme-75/lorette-martyrs/219635585.htm` |

#### 🧐 Résultat

Les résultats sont stockés dans un jeu de données (ou "dataset" en jargon Apify). Chaque élément contient des informations d'une annonce:

##### Exemple de résultat:

Un exemple de résultat pourrait ressembler à la capture d'écran ci-dessous :

![screenshot](https://i.imghippo.com/files/oNfw51724631266.png)

& beaucoup d'autres informations que la capture d'écran ne montre pas, venez explorer!

#### Updates

L'acteur *seloger mass products scraper (by items URLs)* est activement maintenu et régulièrement mis à jour.


#### ⚠️ Clause de non-responsabilité
Cet acteur est un outil indépendant et n'est ni affilié, ni approuvé, ni sponsorisé par Digital Classifieds France SAS ou l'une de ses filiales. Toutes les marques déposées mentionnées sont la propriété de leurs propriétaires respectifs.


### English version

#### 🤩 Features

🚀 Our blazing fast SeLoger mass real estate items scraper lets you extract real estate items' informations and export them to various format (JSON, CSV, HTML etc..) 🔥 Bring your URLs and you're good to go!

👉 It enables you to scrape rich details as title, descriptions, photos, energy information, construction date, price, publisher information (email/phone number included) nearby transaportations and a lot more. 

The scraper has a requried `startUrls` parameter which is an array containg direct URLs to real estate items:
- Example: ["https://www.seloger.com/annonces/achat/appartement/paris-9eme-75/lorette-martyrs/219635585.htm"]

#### ⚠️ Is it legal to scrape SeLoger?

It is legal to scrape publicly available data such as real estate descriptions, prices, photos, nearby transportation etc. Read our blog post on [the legality of web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) to learn more.

#### 🤔 Why scrape SeLoger.com?

SeLoger.com is the largest real estate french website. With over 20 millions visitor/month and around 200K real estate items offering, there's definitely something for you out there!

So what could you do with all that products listings data?

- Find real estate for sale nearby
- Do market data analysis
- Build a real estate agent email list
- Collect housing data for research or personal purposes
- Compare collected data with home value index
- Use the data for overall real estate data analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

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
| `startUrls` | `array` | the direct URLs of the real estate items that the actor will scrape. | `https://www.seloger.com/annonces/achat/appartement/paris-9eme-75/lorette-martyrs/219635585.htm`

#### 🧐 Output

Output is stored in a dataset. Each item is information about a real estate item:  

##### Sample output

An output might look like the below screenshot:

![screenshot](https://i.imghippo.com/files/oNfw51724631266.png)

& a lot more informations that the screenshot does not show, come & explore!

#### Updates

The seloger mass products scraper (by items URLs) actor is actively maintained and regularly updated.


#### ⚠️ Disclaimer
This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Digital Classifieds France SAS or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

# Actor input Schema

## `startUrls` (type: `array`):

Real estate items direct links / Liens directs vers les biens immobiliers à scraper

## Actor input object example

```json
{
  "startUrls": [
    "https://www.seloger.com/annonces/achat/maison/drancy-93/economie/210757703.htm"
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
        "https://www.seloger.com/annonces/achat/maison/drancy-93/economie/210757703.htm"
    ]
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/seloger-mass-products-scraper-by-items-urls").call(input);

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
run_input = { "startUrls": ["https://www.seloger.com/annonces/achat/maison/drancy-93/economie/210757703.htm"] }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/seloger-mass-products-scraper-by-items-urls").call(run_input=run_input)

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
    "https://www.seloger.com/annonces/achat/maison/drancy-93/economie/210757703.htm"
  ]
}' |
apify call azzouzana/seloger-mass-products-scraper-by-items-urls --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/seloger-mass-products-scraper-by-items-urls",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
