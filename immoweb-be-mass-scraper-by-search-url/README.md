# 🚀 Immoweb.be Property Listings Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Immoweb.be Property Listings Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/immoweb-be-mass-scraper-by-search-url?fpr=cbgdsf)

---

## Immoweb.be Property Listings Scraper (By Search URL)

### Version française

#### 🤩 Vue d'ensemble

🚀 Notre scraper ultra-rapide pour les annonces immobilières ee masse immoweb.de vous permet d'extraire les informations des biens immobiliers depuis une page de résultat de recherche et de les exporter dans différents formats (JSON, CSV, HTML, etc.) 🔥 Apportez vos URLs et c'est parti !

👉 Il vous permet de récupérer des détails riches tels que: titres, descriptions, photos, prix, nombre de vues/favoris, informations énergétiques, date de construction, informations de l'éditeur (e-mail/numéro de téléphone si disponible) et bien plus encore.

#### 📚 Comment utiliser ce scraper

1. 👉 [Créez un compte gratuit sur Apify](https://apify.com/sign-up?fpr=cbgdsf) – aucune carte bancaire requise !
2. 🎉 Cliquez sur le bouton **"Get Started"** et complétez une inscription rapide.
3. 💰 Le compte gratuit inclut suffisamment de crédits pour tester cet actor.
4. ⏳ Profitez de la période d’essai gratuite – sans engagement ni paiement anticipé.

Le scraper a un paramètre requis `startUrl`, qui est le lien vers la page de recherche
- Exemple: `https://www.immoweb.be/en/search-3-rooms/apartment/for-rent?countries=BE&maxBedroomCount=3&minBedroomCount=3&maxPrice=500&page=1&orderBy=relevance`

📝 Pour récupérer cette url, lancer votre recherche sur Immoweb.be en appliquant vos filtres souhaités, puis copiez le lien dans la barre d'adresse.

#### Vous avez des liens directs vers des annonces immobilières et vous voulez les scraper?

Si vous avez plutôt des URL directes vers des annonces immobilières (de type `https://www.immoweb.be/en/classified/kot/for-rent/namur/5002/20368607`) et souhaitez en scraper les informations de manière structurée (JSON, Excel, XML, etc.), n'hésitez pas à consulter l'acteur [Immoweb.be ads scraper (by ads URLs) 🏠](https://apify.com/azzouzana/immoweb-be-ads-scraper-by-ads-urls?fpr=cbgdsf)

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

- **$1.50 / 1k annonces scrapées**. Pas de frais cachés.

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
| `startUrls` | `tableau` | les URL directes des biens immobiliers que l'acteur va scraper. | `https://www.immoweb.be/en/search-3-rooms/apartment/for-rent?countries=BE&maxBedroomCount=3&minBedroomCount=3&maxPrice=500&page=1&orderBy=relevance` |
| `maxItems` | `entier` | le nombre maximum d'annonces à scraper. | `999` |

#### 🧐 Résultats

Les résultats sont stockés dans un jeu de données (ou "dataset" en jargon Apify). Chaque élément contient des informations d'une annonce:

##### Exemples de résultats:

Le résultat du scraping rassemble à la capture ci-dessous:

###### Exemple
![immowebbe scraping result](https://i.ibb.co/RCsK27K/image.png)

& plein d'autres informations que les capture d'écrans ci-dessus ne montrent pas, venez explorer!

#### 🔍 **Vous cherchez autre chose ?**
N'hésitez pas à explorer les [+4 000 scrapers préconstruits sur Apify Store](https://apify.com/store?fpr=cbgdsf) pour plus d’options !

---

**Besoin d'une solution personnalisée ? Une demande de fonctionnalité ou juste envie de discuter ?**
Nous serions ravis de vous entendre !

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: [labs@azzouzana.com](mailto:labs@azzouzana.com)

### English version

#### 🤩 Features

🚀 Our blazing fast immoweb.be mass real estate items scraper lets you extract real estate items' information and export them to various format (JSON, CSV, HTML etc..) 🔥 Bring your search URLs and you're good to go!

👉 It enables you to scrape rich details as title, descriptions, popularity, views, photos, energy information, various dates, price, publisher information (email/phone number included when available) and a lot more.

#### 📚 How to use this actor

1. 👉 [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required!
2. 🎉 Just click the **"Get Started"** button and complete a quick signup.
3. 💰 A free account includes enough credits to test this actor.
4. ⏳ Enjoy scraping for the free trial period, no commitment or upfront payment required.

The scraper has a required `startUrl` parameter which holds the value of the search result page's link:
- Example: `https://www.immoweb.be/en/search-3-rooms/apartment/for-rent?countries=BE&maxBedroomCount=3&minBedroomCount=3&maxPrice=500&page=1&orderBy=relevance`

#### Do you have direct links to real estate listings and want to scrape them?

If you have direct URLs to real estate listings (e.g., `https://www.immoweb.be/en/classified/kot/for-rent/namur/5002/20368607`) and want to scrape their information in a structured format (JSON, Excel, XML, etc.), feel free to check out the actor [Immoweb.be ads scraper (by ads URLs) 🏠](https://apify.com/azzouzana/immoweb-be-ads-scraper-by-ads-urls?fpr=cbgdsf).

#### ⚠️ Is it legal to scrape Immoweb.be?

It is legal to scrape publicly available data such as real estate descriptions, prices, photos, nearby transportation etc. Read our blog post on [the legality of web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) to learn more.

#### 🤔 Why scrape Immoweb.be?

Immoweb.be is the largest real estate website in Belgium. With over 7 million visitors per month and more than 1 million real estate listings, there's definitely something for you!

So what could you do with all that products listings data?

- Find real estate for sale nearby
- Do market data analysis
- Build a real estate agent email list
- Collect housing data for research or personal purposes
- Compare collected data with home value index
- Use the data for overall real estate data analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

#### 🤑 Cost of usage

- **$1.50 / 1K listings scraped.** No hidden fees.

#### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

##### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

#### 🛠️ Input

| Field | Type | Description | Default value / Example |
| ----- | ---- | ----------- | ------------- |
| `startUrl` | `array` | the search page's result link | `https://www.immoweb.be/en/search-3-rooms/apartment/for-rent?countries=BE&maxBedroomCount=3&minBedroomCount=3&maxPrice=500&page=1&orderBy=relevance` |
| `maxItems` | `integer` | The maximum number of items to scrape. | `999` |

#### 🧐 Output

##### Output examples

The scraping result may look like this
###### Example
![immowebbe scraping result](https://i.ibb.co/RCsK27K/image.png)

& many more details that the screenshots above don't show, come and explore!

---

**Need a custom solution? Have a feature request or just want to chat?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: [labs@azzouzana.com](mailto:labs@azzouzana.com)

# Actor input Schema

## `startUrl` (type: `string`):

The search URL to start with.
## `maxItems` (type: `integer`):

Maximum number of listings to scrape

## Actor input object example

```json
{
  "startUrl": "https://www.immoweb.be/en/search/office/for-rent?countries=BE&maxPrice=50&priceType=MONTHLY_RENTAL_PRICE&page=1&orderBy=relevance",
  "maxItems": 2000
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
    "startUrl": "https://www.immoweb.be/en/search/office/for-rent?countries=BE&maxPrice=50&priceType=MONTHLY_RENTAL_PRICE&page=1&orderBy=relevance",
    "maxItems": 2000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/immoweb-be-mass-scraper-by-search-url").call(input);

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
    "startUrl": "https://www.immoweb.be/en/search/office/for-rent?countries=BE&maxPrice=50&priceType=MONTHLY_RENTAL_PRICE&page=1&orderBy=relevance",
    "maxItems": 2000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/immoweb-be-mass-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.immoweb.be/en/search/office/for-rent?countries=BE&maxPrice=50&priceType=MONTHLY_RENTAL_PRICE&page=1&orderBy=relevance",
  "maxItems": 2000
}' |
apify call azzouzana/immoweb-be-mass-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/immoweb-be-mass-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
