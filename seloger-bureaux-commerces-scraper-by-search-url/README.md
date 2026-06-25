# 🚀 SeLoger Bureaux & Commerces Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the SeLoger Bureaux & Commerces Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/seloger-bureaux-commerces-scraper-by-search-url?fpr=cbgdsf)

---

## SeLoger Bureaux & Commerces Scraper (By Search URL)

### Version française

#### 🤩 Vue d'ensemble

🚀 Notre scraper ultra-rapide pour les annonces immobilières de masse **SeLoger bureaux-commerces** vous permet d'extraire les informations des biens depuis la page de résultats de `https://www.seloger-bureaux-commerces.com/` et de les exporter dans différents formats (JSON, CSV, HTML, etc.). 🔥 Apportez vos URLs et c'est parti !

 Il vous permet d'extraire des détails riches : titres, descriptions, photos, informations énergétiques, année de construction, prix, coordonnées de l'éditeur (email/téléphone si disponible), transports, etc.  

Le scraper nécessite un paramètre obligatoire `startUrl`, qui est le lien vers la page de recherche :
- Exemple : `https://www.seloger-bureaux-commerces.com/recherche?typeTransaction=2&typeBien=800&ci=590350&leaseType=&tri=0&page=2`

📝 Pour récupérer cette URL, effectuez une recherche sur [SeLoger bureaux-commerces](https://www.seloger-bureaux-commerces.com), appliquez vos filtres, puis copiez le lien de la barre d'adresse.

#### ⚠️ Est-il légal de scraper SeLoger bureaux-commerces ?

Scraper des données accessibles publiquement (titres, descriptions, prix, photos, transports, etc.) est légal. Consultez notre article sur [la légalité du web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) pour en savoir plus.

#### 🤔 Pourquoi scraper SeLoger bureaux-commerces ?

SeLoger bureaux-commerces est une plateforme majeure d'annonces immobilières commerciales en France, avec des millions de visiteurs chaque mois et une large base d'annonces.  

Voici ce que vous pouvez faire avec ces données :  
- Trouver des biens commerciaux à vendre ou à louer  
- Analyser les tendances du marché  
- Créer une base de données de contacts professionnels  
- Comparer les données collectées avec des indices du marché  
- Identifier des fonds de commerce à ne pas rater
- Mener des études immobilières  

Les possibilités sont infinies 🚀

#### 🤑 Coût d'utilisation

Le coût moyen du scraper **SeLoger bureaux-commerces** est **$2,00 pour 1000 annonces**. Pour les utilisateurs du plan gratuit, l'utilisation est limitée à 5 exécutions par jour avec un temps d'attente de 30 minutes entre chaque exécution.

📌 Le scraper utilise les proxies résidentiels d'Apify pour de meilleures performances.

#### 🛠️ Paramètres d'entrée

| Champ | Type | Description | Exemple / Valeur par défaut |
|-------|------|-------------|---------|
| `startUrl` | `lien` | Lien vers la page des résultats de recherche | `https://www.seloger-bureaux-commerces.com/recherche?...` |
| `maxItems` | `entier` | le nombre maximum d'annonces à scraper. | `5000` |
| `enableDataFlattening` | `booléen` | Activer l'aplatissement des données (clés triées alphabétiquement). | `false` |

##### ⚠️ Remarques

#### 🧐 Résultats

Les données sont stockées dans un dataset. Chaque élément contient des informations détaillées sur une annonce.

##### Exemple de sortie :

```json
{
	"id": "259513585",
	"idAnnonce": 259513585,
	"idSourceCouplage": 10,
	"detailUrl": "https://www.seloger-bureaux-commerces.com/annonces/achat/bureau/lille-59000/259513585",
	"codeTypeBien": 800,
	"idTypeTransaction": 2,
	"idTypeBien": 8,
	"idSousTypeBien": 0,
	"isAnnonceOr": false,
	"isBoostSuggestion": false,
	"isBoostHighlight": false,
	"isDivisible": false,
	"isImmediatelyAvailable": true,
	"hasTrafficData": false,
	"businessSold": {
		"isWallsIncluded": true,
		"businessType": 0,
		"subBusinessType": 0
	},
	"office": {},
	"cardTitle": "Bureau",
	"cardDescription": "Situé au coeur vibrant de Lille, sur la prestigieuse façade de l'Esplanade...",
	"description": "Situé au coeur vibrant de Lille, sur la prestigieuse façade de l'Esplanade...",
	"leaseTypes": [],
	"equipments": [
		1
	],
	"localisation": {
		"codeRegion": 2243,
		"codeDepartement": "59",
		"idSubDivision": 17665,
		"fakeCityCodeInsee": 0,
		"isArrondissement": false,
		"codeInsee": 590350,
		"codePostal": "59000",
		"nomVille": "Lille",
		"idQuartier": 115621,
		"nomQuartier": "Centre",
		"idIris": 281497,
		"adresse": "1 RUE MACQUART",
		"localisationPrecision": 2,
		"geoLocation": {
			"latitude": 50.63652,
			"longitude": 3.05136
		}
	},
	"mandat": {
		"isCoex": false,
		"isExclusive": false,
		"hasEmail": true,
		"hasTel": true,
		"mandataires": [
			{
				"name": "ARTHUR Loyd Nord Pas de Calais",
				"idAgence": 119453,
				"idRcu": "RC-061163",
				"idTiers": 178405,
				"isPrincipal": true,
				"logoUrl": "https://v.seloger.com/s/width/150/logos/2/7/z/k/27zkay5rn0ife4drjzyi1ant9gewq1l2z54pkkym0.jpg",
				"websiteUrl": "http://www.arthur-loyd-lille.com",
				"codePostal": "59130"
			}
		]
	},
	"photos": [
		"https://v.seloger.com/s/crop/500x240/visuels/0/b/b/q/0bbqs0njaodn1tnvr3xow5vo24h3litttzakpxveo.jpg"
	],
	"price": {
		"buy": {
			"price": {
				"type": 1,
				"value": 880000
			},
			"priceBySquareMeter": {
				"type": 1,
				"value": 4000
			}
		},
		"additionalCharges": {
			"isLeaseBack": false,
			"hasAgencyFeesIncluded": false,
			"hasOperatingCostIncluded": false,
			"hasTaxIncluded": true
		}
	},
	"publicationDateOnly": "2026-02-13T00:00:00",
	"publicationDateTime": "2026-02-13T10:10:00",
	"lastUpdateDateTime": "2026-02-13T10:16:00",
	"qualityIndex": 91,
	"refAnnonce": "ALLI-660247-0V-1",
	"space": 220
}
````

#### 💰 Estimation des coûts

L'acteur est facturé comme suit :

- **Prix pour 1 000 éléments** : 2,00 $

##### Exemple :

1. **Scraping standard**
   - Vous récupérez 10 000 annonces.
   - Coût : (10 000 / 1 000) \* 2,00 $ = **20,00 $**

#### 🆓 Limitations du Plan Gratuit

Nous voulons que vous voyiez comment cet acteur fonctionne avant de vous engager. Pour garder les choses équitables pour tout le monde, le **plan gratuit** inclut généralement ces limites d'essai :

- **Données d'échantillon :** jusqu'à **5 annonces** par exécution—suffisant pour vérifier la qualité des données.
- **Limite quotidienne :** **5 exécutions** par jour civil (UTC).
- **Entre les exécutions :** au moins **30 minutes** avant de pouvoir lancer une autre exécution.

> Les limites peuvent changer en fonction de la charge du système et de votre volume de scraping prévu.

##### Mettez à niveau quand vous êtes prêt à passer à l'échelle

Utilisez le plan gratuit pour décider si cet acteur correspond à votre projet. Les plans payants d'Apify suppriment ces temps d'attente et ces plafonds pour que vous puissiez exécuter à plein volume—[**passez à un plan payant**](https://apify.com/pricing?fpr=cbgdsf).

#### 📌 Mises à jour

Le scraper **SeLoger bureaux-commerces** est activement maintenu et régulièrement mis à jour

#### 📬 Contact & Support

**Besoin d'une solution personnalisée ? Une demande de fonctionnalité ?**
Nous serions ravis d'avoir de vos nouvelles !

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

***

### English version

#### 🤩 Overview

🚀 Our ultra-fast scraper for **SeLoger bureaux-commerces** real estate ads allows you to extract property information from the search results page of `https://www.seloger-bureaux-commerces.com/` and export it in various formats (JSON, CSV, HTML, etc.). 🔥 Just provide your URLs and you're good to go!

It allows you to extract rich details: titles, descriptions, photos, energy information, construction year, price, editor contact details (email/phone if available), transportation, etc.

The scraper requires a mandatory `startUrl` parameter, which is the link to the search results page:

- Example: `https://www.seloger-bureaux-commerces.com/recherche?typeTransaction=2&typeBien=800&ci=590350&leaseType=&tri=0&page=2`

📝 To retrieve this URL, perform a search on [SeLoger bureaux-commerces](https://www.seloger-bureaux-commerces.com), apply your filters, then copy the link from the address bar.

#### ⚠️ Is it legal to scrape SeLoger bureaux-commerces?

Scraping publicly accessible data (titles, descriptions, prices, photos, transport, etc.) is legal. Check out our article on [the legality of web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) to learn more.

#### 🤔 Why scrape SeLoger bureaux-commerces?

SeLoger bureaux-commerces is a major platform for commercial real estate ads in France, with millions of visitors every month and a large database of listings.

Here's what you can do with this data:

- Find commercial properties for sale or rent
- Analyze market trends
- Build a database of professional contacts
- Compare the collected data with market indices
- Identify commercial opportunities not to miss
- Conduct real estate studies

The possibilities are endless 🚀

#### 🤑 Usage Cost

The average cost of the **SeLoger bureaux-commerces** scraper is about **$2.00 per 1000 ads**.

> **Note**: For Apify users on the Free plan, the actor is limited to a maximum of **10 ads** per run.

📌 The scraper uses Apify's residential proxies for better performance.

#### 🛠️ Input Parameters

| Field | Type | Description | Example / Default Value |
|-------|------|-------------|-------------------------|
| `startUrl` | `link` | Link to the search results page | `https://www.seloger-bureaux-commerces.com/recherche?...` |
| `maxItems` | `integer` | The maximum number of items to scrape. | `5000` |
| `enableDataFlattening` | `boolean` | Enable data flattening (keys sorted alphabetically). | `false` |

##### ⚠️ Notes

#### 🧐 Results

The data is stored in a dataset. Each item contains detailed information about an ad.

##### Example output:

##### JSON (Flattening Disabled - Default)

```json
{
	"id": "259513585",
	"idAnnonce": 259513585,
	"idSourceCouplage": 10,
	"detailUrl": "https://www.seloger-bureaux-commerces.com/annonces/achat/bureau/lille-59000/259513585",
	"codeTypeBien": 800,
	"idTypeTransaction": 2,
	"idTypeBien": 8,
	"idSousTypeBien": 0,
	"isAnnonceOr": false,
	"isBoostSuggestion": false,
	"isBoostHighlight": false,
	"isDivisible": false,
	"isImmediatelyAvailable": true,
	"hasTrafficData": false,
	"businessSold": {
		"isWallsIncluded": true,
		"businessType": 0,
		"subBusinessType": 0
	},
	"office": {},
	"cardTitle": "Bureau",
	"cardDescription": "Situé au coeur vibrant de Lille, sur la prestigieuse façade de l'Esplanade...",
	"description": "Situé au coeur vibrant de Lille, sur la prestigieuse façade de l'Esplanade...",
	"leaseTypes": [],
	"equipments": [
		1
	],
	"localisation": {
		"codeRegion": 2243,
		"codeDepartement": "59",
		"idSubDivision": 17665,
		"fakeCityCodeInsee": 0,
		"isArrondissement": false,
		"codeInsee": 590350,
		"codePostal": "59000",
		"nomVille": "Lille",
		"idQuartier": 115621,
		"nomQuartier": "Centre",
		"idIris": 281497,
		"adresse": "1 RUE MACQUART",
		"localisationPrecision": 2,
		"geoLocation": {
			"latitude": 50.63652,
			"longitude": 3.05136
		}
	},
	"mandat": {
		"isCoex": false,
		"isExclusive": false,
		"hasEmail": true,
		"hasTel": true,
		"mandataires": [
			{
				"name": "ARTHUR Loyd Nord Pas de Calais",
				"idAgence": 119453,
				"idRcu": "RC-061163",
				"idTiers": 178405,
				"isPrincipal": true,
				"logoUrl": "https://v.seloger.com/s/width/150/logos/2/7/z/k/27zkay5rn0ife4drjzyi1ant9gewq1l2z54pkkym0.jpg",
				"websiteUrl": "http://www.arthur-loyd-lille.com",
				"codePostal": "59130"
			}
		]
	},
	"photos": [
		"https://v.seloger.com/s/crop/500x240/visuels/0/b/b/q/0bbqs0njaodn1tnvr3xow5vo24h3litttzakpxveo.jpg"
	],
	"price": {
		"buy": {
			"price": {
				"type": 1,
				"value": 880000
			},
			"priceBySquareMeter": {
				"type": 1,
				"value": 4000
			}
		},
		"additionalCharges": {
			"isLeaseBack": false,
			"hasAgencyFeesIncluded": false,
			"hasOperatingCostIncluded": false,
			"hasTaxIncluded": true
		}
	},
	"publicationDateOnly": "2026-02-13T00:00:00",
	"publicationDateTime": "2026-02-13T10:10:00",
	"lastUpdateDateTime": "2026-02-13T10:16:00",
	"qualityIndex": 91,
	"refAnnonce": "ALLI-660247-0V-1",
	"space": 220
}
```

#### 💰 Cost Estimation

The actor is priced as follows:

- **Price per 1,000 items**: $2.00

##### Examples:

1. **Standard Scraper**
   - Scrape 10,000 items.
   - Cost: (10,000 / 1,000) \* $2.00 = **$20.00**

#### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

##### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

#### 📌 Updates

The **SeLoger bureaux-commerces** scraper is actively maintained and regularly updated.

#### 📬 Contact & Support

**Need a custom solution? Have a feature request?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

***

# Actor input Schema

## `startUrl` (type: `string`):

Search results page URL / Lien vers la page résultat de recherche

## `maxItems` (type: `integer`):

Maximum number of listings to scrape

## `enableDataFlattening` (type: `boolean`):

Check this box to flatten the output data structure

## Actor input object example

```json
{
  "startUrl": "https://www.seloger-bureaux-commerces.com/recherche?typeTransaction=9&typeBien=1111&ci=590350&leaseType=&tri=0",
  "maxItems": 1000,
  "enableDataFlattening": false
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
    "startUrl": "https://www.seloger-bureaux-commerces.com/recherche?typeTransaction=9&typeBien=1111&ci=590350&leaseType=&tri=0",
    "maxItems": 1000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/seloger-bureaux-commerces-scraper-by-search-url").call(input);

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
    "startUrl": "https://www.seloger-bureaux-commerces.com/recherche?typeTransaction=9&typeBien=1111&ci=590350&leaseType=&tri=0",
    "maxItems": 1000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/seloger-bureaux-commerces-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.seloger-bureaux-commerces.com/recherche?typeTransaction=9&typeBien=1111&ci=590350&leaseType=&tri=0",
  "maxItems": 1000
}' |
apify call azzouzana/seloger-bureaux-commerces-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/seloger-bureaux-commerces-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
