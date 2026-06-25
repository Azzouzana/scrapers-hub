# 🚀 SeLoger Scraper — List & Classified Search (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the SeLoger Scraper — List & Classified Search (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/seloger-mass-products-scraper-by-search-url?fpr=cbgdsf)

---

## SeLoger Scraper — List & Classified Search (By Search URL)

> Scrapez des milliers d'annonces immobilières depuis les pages de recherche SeLoger (list ou classified). Export JSON, CSV, Excel. Données détaillées : prix, photos, DPE, contact éditeur, transports. Facturation à l'usage (PPE).

---

### 🔍 SEO Keywords

**English:** SeLoger scraper, SeLoger API, France real estate scraper, French property listings, SeLoger search scraper, Paris real estate data, Immobilier France API, SeLoger list scraper, Apify SeLoger actor, scrape SeLoger.

**Français :** scraper SeLoger, API SeLoger, annonces immobilières France, données immobilières SeLoger, extraction annonces SeLoger, scraper immobilier France.

---

### Version française

#### 🤩 Vue d'ensemble

🚀 Notre scraper ultra-rapide pour les annonces immobilières de masse SeLoger vous permet d'extraire les informations des biens immobiliers depuis une page de résultat de recherche et de les exporter dans différents formats (JSON, CSV, HTML, etc.) 🔥 Apportez vos URLs et c'est parti !

👉 Il vous permet de récupérer des détails riches : titres, descriptions, photos, informations énergétiques (DPE), date de construction, prix & much more!

#### 📚 Comment utiliser cet actor

1. 👉 [Créez un compte gratuit sur Apify](https://apify.com/sign-up?fpr=cbgdsf) – aucune carte bancaire requise !
2. 🎉 Cliquez sur le bouton **"Get Started"** et complétez une inscription rapide.
3. 💰 Le compte gratuit inclut suffisamment de crédits pour tester cet actor.
4. ⏳ Profitez de la période d'essai gratuite – sans engagement ni paiement anticipé.

Le scraper a un paramètre requis `startUrl`, qui est le lien vers la page de recherche :

- **List (liste classique)** : `https://www.seloger.com/list.htm?projects=2&types=2,1&natures=1&places=[{%22divisions%22:[2238]},{%22inseeCodes%22:[130208]}]&rooms=3&mandatorycommodities=0&pool=1&enterprise=0&qsVersion=1.0&m=search_refine-redirection-search_results`
- **Classified** : `https://www.seloger.com/classified-search?classifiedBusiness=Private&distributionTypes=Buy,Buy_Auction&estateTypes=House,Apartment&locations=AD08FR1977&priceMax=300000&priceMin=100000&order=DateDesc&m=classifed_search_results_map_switch_button_to_classified_search_results`

📝 Pour récupérer cette URL : lancez votre recherche sur [SeLoger](https://www.seloger.com) en appliquant vos filtres, puis copiez le lien dans la barre d'adresse (format `https://www.seloger.com/list.htm?...` ou `.../classified-search?...`).

#### Vous avez des liens directs vers des annonces ?

Si vous avez des URL directes vers des annonces (`https://www.seloger.com/annonces/...`) et souhaitez en extraire les données de manière structurée, consultez l'acteur [SeLoger mass products scraper (by ads URLs) ⚡](https://apify.com/azzouzana/seloger-mass-products-scraper-by-items-urls).

#### ⚠️ Est-il légal de scraper SeLoger ?

Il est légal de scraper les données publiquement disponibles (descriptions, prix, photos, transports, etc.). Pour en savoir plus : [légalité du web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf).

#### 🤔 Pourquoi scraper SeLoger.com ?

SeLoger.com est le plus grand site immobilier en France : plus de 20 millions de visiteurs par mois et près de 2 millions d'annonces. Que faire avec ces données ?

- Trouver des biens à vendre ou louer à proximité
- Analyser le marché immobilier
- Constituer une liste de contacts d'agents ou de particuliers
- Collecter des données pour la recherche ou des projets perso
- Comparer avec des indices de prix
- Alimenter des tableaux de bord ou des applications

Les possibilités sont infinies 🚀

#### 🤑 Coût d'utilisation

La facturation est en **Pay Per Event (PPE)** : vous payez selon le nombre d'annonces poussées dans le dataset.

##### Tarif : **$1.5 / 1 000 annonces** (plat, quel que soit le plan Apify)

##### Exemples de coûts

| Annonces scrapées | Coût indicatif |
|------------------|--------------|
| 100              | ~ $0.15 |
| 1,000            | ~ $1.50 |
| 5,000            | ~ $7.50 |
| 10,000           | ~ $15.00 |

#### 🆓 Limitations du Plan Gratuit

Nous voulons que vous voyiez comment cet acteur fonctionne avant de vous engager. Pour garder les choses équitables pour tout le monde, le **plan gratuit** inclut généralement ces limites d'essai :

- **Données d'échantillon :** jusqu'à **5 annonces** par exécution—suffisant pour vérifier la qualité des données.
- **Limite quotidienne :** **5 exécutions** par jour civil (UTC).
- **Entre les exécutions :** au moins **30 minutes** avant de pouvoir lancer une autre exécution.

> Les limites peuvent changer en fonction de la charge du système et de votre volume de scraping prévu.

##### Mettez à niveau quand vous êtes prêt à passer à l'échelle

Utilisez le plan gratuit pour décider si cet acteur correspond à votre projet. Les plans payants d'Apify suppriment ces temps d'attente et ces plafonds pour que vous puissiez exécuter à plein volume—[**passez à un plan payant**](https://apify.com/pricing?fpr=cbgdsf).

#### 🛠️ Paramètres d'entrée

| Champ      | Type      | Description | Valeur par défaut / Exemple |
|-----------|-----------|-------------|-----------------------------|
| `startUrl` | `string`  | URL de la page de résultats de recherche SeLoger (list ou classified). | Obligatoire. Ex. : `https://www.seloger.com/list.htm?...` |
| `maxItems` | `integer` | Nombre maximum d'annonces à scraper. | `1000` (optionnel) |

**PPE** : la limite effective prend en compte votre `maxItems` et le plafond gratuit (5 annonces pour les utilisateurs non abonnés).

#### 🧐 Résultats

Les résultats sont stockés dans un **dataset** Apify. Chaque élément correspond à une annonce (titre, prix, description, photos etc.).

Et bien d'autres champs : venez explorer le dataset !

#### 🔍 Vous cherchez autre chose ?

Découvrez les [plus de 4 000 scrapers sur Apify Store](https://apify.com/store?fpr=cbgdsf).

---

#### 📬 Nous contacter

**Besoin d'une solution sur mesure, d'une évolution ou juste envie d'échanger ?**  
On sera ravis de vous répondre.

- 💬 **Discord** : `@azzouzana`
- 📧 **Email** : [labs@azzouzana.com](mailto:labs@azzouzana.com)

---

#### ⚠️ Clause de non-responsabilité

Cet acteur est un outil indépendant et n'est ni affilié, ni approuvé, ni sponsorisé par Digital Classifieds France SAS ou ses filiales. Toutes les marques mentionnées appartiennent à leurs propriétaires respectifs.

---

### English version

#### 🤩 Features

🚀 Our fast SeLoger mass real estate scraper extracts listing data from search result pages and exports to JSON, CSV, HTML, and more 🔥 Paste your search URL and you're good to go.

👉 You get rich details: titles, descriptions, photos, energy info (DPE), construction date, price and much more!

#### 📚 How to use this actor

1. 👉 [Sign up for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required.
2. 🎉 Click **"Get Started"** and complete signup.
3. 💰 The free account includes enough credits to try this actor.
4. ⏳ Use the free trial with no commitment or upfront payment.

The scraper requires a `startUrl` pointing to a SeLoger search page:

- **List (standard search)** : `https://www.seloger.com/list.htm?projects=2&types=2,1&natures=1&places=[...]&rooms=3&...`
- **Classified** : `https://www.seloger.com/classified-search?classifiedBusiness=Private&...`

📝 To get the URL: run your search on [SeLoger](https://www.seloger.com) with your filters, then copy the address bar link (`list.htm` or `classified-search`).

#### Have direct listing URLs?

If you have direct ad URLs (`https://www.seloger.com/annonces/...`) and want structured data, check out [SeLoger mass products scraper (by ads URLs) ⚡](https://apify.com/azzouzana/seloger-mass-products-scraper-by-items-urls).

#### ⚠️ Is it legal to scrape SeLoger?

Scraping publicly available data (descriptions, prices, photos, transport, etc.) is legal. Read more: [web scraping legality](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf).

#### 🤔 Why scrape SeLoger.com?

SeLoger.com is France's largest real estate site: 20+ million visitors per month and around 2 million listings. What can you do with this data?

- Find properties for sale or rent nearby
- Run market analysis
- Build agent or private advertiser contact lists
- Collect housing data for research or side projects
- Compare with price indices
- Feed dashboards or apps

Sky's the limit 🚀

#### 🤑 Cost of usage

Billing is **Pay Per Event (PPE)** — you pay per number of listings pushed to the dataset.

##### Rate: **$1.5 / 1,000 listings** (flat, regardless of Apify plan)

##### Pricing examples

| Listings scraped | Approx. cost |
|------------------|--------------|
| 100              | ~ $0.15 |
| 1,000            | ~ $1.50 |
| 5,000            | ~ $7.50 |
| 10,000           | ~ $15.00 |

#### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

##### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

#### 🛠️ Input

| Field      | Type      | Description | Default / Example |
|-----------|-----------|-------------|-------------------|
| `startUrl` | `string`  | SeLoger search results page URL (list or classified). | Required. e.g. `https://www.seloger.com/list.htm?...` |
| `maxItems` | `integer` | Maximum number of listings to scrape. | `1000` (optional) |

**PPE billing** : the effective limit respects your `maxItems` and the free-tier cap (5 listings for non-subscribers).

#### 🧐 Output

Output is stored in an Apify **dataset**. Each item is one listing (title, price, description, photos, DPE, contact, transport, etc.).

Plus many more fields — explore the dataset to see everything.

#### 🔍 Looking for something else?

Browse [4,000+ scrapers on Apify Store](https://apify.com/store?fpr=cbgdsf).

---

#### 📬 Contact us

**Need a custom solution, a feature request, or just want to chat?**  
We'd love to hear from you.

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: [labs@azzouzana.com](mailto:labs@azzouzana.com)

---

#### ⚠️ Disclaimer

This actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Digital Classifieds France SAS or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

# Actor input Schema

## `startUrl` (type: `string`):

SeLoger search page URL (list.htm or classified-search).
## `maxItems` (type: `integer`):

Maximum number of listings to scrape. Leave empty for no limit.

## Actor input object example

```json
{
  "startUrl": "https://www.seloger.com/classified-search?classifiedBusiness=Private&distributionTypes=Buy,Buy_Auction&estateTypes=House,Apartment&locations=AD08FR1977&priceMax=300000&priceMin=100000&order=DateDesc&m=classifed_search_results_map_switch_button_to_classified_search_results",
  "maxItems": 1000
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
    "startUrl": "https://www.seloger.com/classified-search?classifiedBusiness=Private&distributionTypes=Buy,Buy_Auction&estateTypes=House,Apartment&locations=AD08FR1977&priceMax=300000&priceMin=100000&order=DateDesc&m=classifed_search_results_map_switch_button_to_classified_search_results",
    "maxItems": 1000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/seloger-mass-products-scraper-by-search-url").call(input);

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
    "startUrl": "https://www.seloger.com/classified-search?classifiedBusiness=Private&distributionTypes=Buy,Buy_Auction&estateTypes=House,Apartment&locations=AD08FR1977&priceMax=300000&priceMin=100000&order=DateDesc&m=classifed_search_results_map_switch_button_to_classified_search_results",
    "maxItems": 1000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/seloger-mass-products-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.seloger.com/classified-search?classifiedBusiness=Private&distributionTypes=Buy,Buy_Auction&estateTypes=House,Apartment&locations=AD08FR1977&priceMax=300000&priceMin=100000&order=DateDesc&m=classifed_search_results_map_switch_button_to_classified_search_results",
  "maxItems": 1000
}' |
apify call azzouzana/seloger-mass-products-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/seloger-mass-products-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
