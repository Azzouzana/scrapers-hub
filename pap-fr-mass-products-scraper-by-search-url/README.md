# 🚀 Pap.fr Scraper — Vente & Location (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Pap.fr Scraper — Vente & Location (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/pap-fr-mass-products-scraper-by-search-url?fpr=cbgdsf)

---

## Pap.fr Scraper — Vente & Location (By Search URL)

### Version française

#### 🤩 Vue d'ensemble

🚀 Notre scraper ultra-rapide pour les annonces immobilières de masse pap.fr vous permet d'extraire les informations des
biens immobiliers depuis une page de résultats de recherche et de les exporter dans différents formats (JSON, CSV, HTML,
etc.) 🔥 Apportez vos URLs et c'est parti !

👉 Il vous permet de récupérer des détails riches tels que les titres, descriptions, photos, informations énergétiques,
date de construction, prix, informations de l'éditeur (e-mail/numéro de téléphone inclus), transports à proximité et
bien plus encore

#### 📚 Comment utiliser ce scraper

1. 👉 [Créez un compte gratuit sur Apify](https://apify.com/sign-up?fpr=cbgdsf) – aucune carte bancaire requise !
2. 🎉 Cliquez sur le bouton **"Get Started"** et complétez une inscription rapide.
3. 💰 Le compte gratuit inclut suffisamment de crédits pour tester cet actor.
4. ⏳ Profitez de la période d’essai gratuite – sans engagement ni paiement anticipé.

Le scraper a un paramètre requis `startUrl`, qui est le lien vers la page de recherche

- Exemple: `https://www.pap.fr/annonce/locations-appartement-paris-11e-g37778-a-partir-de-6-chambres-jusqu-a-9-m2`

📝 Pour récupérer cette url, lancer votre recherche sur `https://www.pap.fr` en appliquant vos filtres souhaités, puis
copiez le lien généré dans la barre d'adresse.

#### Vous avez des liens directs vers des annonces immobilières et vous voulez les scraper?

Si vous avez plutôt des URL directes vers des annonces immobilières et souhaitez en scraper les informations de manière
structurée (JSON, Excel, XML, etc.), n'hésitez pas à consulter
l'acteur [Pap.fr mass products scraper (by items URLs) ⚡](https://apify.com/azzouzana/pap-fr-mass-products-scraper-by-items-urls)

#### ⚠️ Est-il légal de scraper pap.fr ?

Il est légal de scraper les données publiquement disponibles telles que les descriptions de biens immobiliers, les prix,
les photos, les transports à proximité, etc. Lisez notre article de blog sur
la [légalité du web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) pour en savoir plus.

#### 🤔 Pourquoi scraper pap.frm ?

pap.fr est l'un des sites immobiliers les plus populaires en France. Avec des centaines de milliers d'annonces, il y a
forcément quelque chose pour vous !

Alors, que pourriez-vous faire avec toutes ces données sur les annonces immobilières ?

- Trouver des biens immobiliers à vendre à proximité
- Faire une analyse des données du marché
- Créer une liste d'emails d'agents immobiliers
- Collecter des données sur le logement pour la recherche ou des besoins personnels
- Comparer les données collectées avec un indice de valeur des maisons
- Utiliser les données pour une analyse globale du marché immobilier

Ce ne sont que quelques idées pour vous faire réfléchir à la manière dont le web scraping peut vous fournir les données
dont vous avez besoin. Les possibilités sont infinies 🚀

#### 🤑 Coût d'utilisation

Le coût d'utilisation du scraper ppa.fr est de **$1.2 pour chaque 1000 annonces immobilières scrappées**.

#### 🛠️ Paramètres d'entrée:

| Champ | Type | Description | Valeur par défaut / Exemple |
| ----- | ---- | ----------- | ------------- |
| `startUrl` | `lien` (obligatoire) | les URLs directes des biens immobiliers que l'acteur va scraper. | `https://www.pap.fr/annonce/locations-appartement-paris-11e-g37778-a-partir-de-6-chambres-jusqu-a-9-m2` |
| `maxItemsToScrape ` | `nombre` (optionnel) | Nombre maximal des annonces à scraper | 1

#### 🧐 Résultats

Un exemple de résultat pourrait ressembler à cette structure :

```json
{
    "id": 461001892,
    "produit": "vente",
    "typebien": "appartement",
    "typebien_slug": "appartement",
    "typebien_label": "Appartement",
    "prix": "510.000 €",
    "nb_pieces": 5,
    "nb_chambres_max": 3,
    "marker": {
        "lat": 48.883958,
        "lng": 2.130591
    },
    "titre": "Le Vésinet (78110)",
    "caracteristiques": "Appartement / 5 pièces / 3 chambres / 88 m² / 5.795 € le m²",
    "video": null,
    "visite_virtuelle": null,
    "date": "31 janvier 2026",
    "classe_energie": {
        "lettre": "d",
        "description": "Logement avec une consommation annuelle d'énergie comprise entre 181 et 250 kWh/m²/an."
    },
    "classe_ges": {
        "lettre": "e",
        "description": "Logement avec une émission de gaz à effet de serre comprise entre 51 et 70 kgéqCO2/m²/an."
    },
    "texte": "Découvrez cet appartement **spacieux, lumineux et traversant** situé dans le quartier Princesse du Vésinet, au début de la rue de Verdun.\nSuperficie de 88 m², cet espace comprend 3 chambres, un grand salon salle à manger de 30 m2, une cuisine aménagée et une salle de bains, idéal pour une famille cherchant confort et praticité. **Plan idéal**.\n\nÀ l'extérieur, profitez d'un **joli balcon filant de 4 m² orienté plein sud**.\nLe bien est également doté  d'un emplacement de parking souterrain, un atout précieux pour la vie quotidienne et d'un garage à vélo commun intérieur. Situé au sein d'un immeuble de quatre étages avec ascenseur, cet appartement assure un accès facile et agréable.\n\nEn matière de transports, vous êtes à seulement 80 m d'un arrêt de bus et à 700 m de la gare Le Vésinet Centre, facilitant vos déplacements. Les commodités ne manquent pas, avec un supermarché bio à 100 m , une boulangerie, une pharmacie, un tabac, plusieurs restaurants et commerces de proximité. A moins d'un kilomètre, un Hyper U et une station essence. Pour les familles, une école maternelle et primaire se trouvent en face ainsi qu'un parc aménagé, parfait pour les enfants, à seulement 100 m.\n\nCet appartement représente une opportunité rare de vivre dans un cadre familial, alliant confort et accessibilité. N'attendez plus pour visiter et découvrir votre futur chez-vous !",
    "texte_accroche": "",
    "texte_contact": "",
    "telephones": [
        "01 40 56 35 45"
    ],
    "has_email": true,
    "photos": [
        "https://cdn.pap.fr/photos/pap/39/d6/39d6f23401ccf18ac22164071e26d56e/3-p1.jpg",
        "https://cdn.pap.fr/photos/pap/ce/39/ce39867e630a54a357eb00c387065589/c-p1.jpg",
        "https://cdn.pap.fr/photos/pap/ad/99/ad9945a23610b8ea0244b961bca89132/a-p1.jpg",
        "https://cdn.pap.fr/photos/pap/a9/5a/a95a3ae36dbd9d13c65afd281b597be3/a-p1.jpg",
        "https://cdn.pap.fr/photos/pap/de/a1/dea154c2cc89de22024b1759cd0f5dee/d-p1.jpg",
        "https://cdn.pap.fr/photos/pap/02/13/02131787aba8803854678fb6dd4a9dc5/0-p1.jpg",
        "https://cdn.pap.fr/photos/pap/c8/65/c8659c9f8c52b8e9ebe2777c5fdb00f2/c-p1.jpg",
        "https://cdn.pap.fr/photos/pap/22/88/22884f3f07951d8aae8b4a0c6d8bef00/2-p1.jpg",
        "https://cdn.pap.fr/photos/pap/f3/a5/f3a556823cfa356ea5cc46e130631ea3/f-p1.jpg",
        "https://cdn.pap.fr/photos/pap/6e/1c/6e1c88ad0918ae9f85dd7dbecb4f6ed3/6-p1.jpg",
        "https://cdn.pap.fr/photos/pap/08/86/08869e358567bac6e4ff93b57e9c131c/0-p1.jpg",
        "https://cdn.pap.fr/photos/pap/38/0b/380beb6639f39cb2a86d87b68e3829ad/3-p1.jpg"
    ],
    "transports": [
        {
            "label": "Le Vésinet - Centre",
            "pictos": [
                "rer-0",
                "rer-a"
            ]
        },
        {
            "label": "Le Vésinet - Le Pecq",
            "pictos": [
                "rer-0",
                "rer-a"
            ]
        },
        {
            "label": "Chatou - Croissy",
            "pictos": [
                "rer-0",
                "rer-a"
            ]
        }
    ],
    "prix_valide": false,
    "affiche_demarchage_refuse": true,
    "appel_video": null,
    "reference_courte": "G10/1892",
    "site_perso": null,
    "url": "https://www.pap.fr/annonces/-r461001892",
    "favori": false,
    "deja_contacte": null,
    "avant_premiere": false,
    "has_pass_avant_premiere": false,
    "__isFound": true,
    "__scrapedAt": "2026-01-31T21:27:29.131Z"
}
````

Venez explorer!

#### 🆓 Limitations du plan gratuit

Nous voulons que vous puissiez voir comment fonctionne cet actor avant de vous engager. Pour que tout reste équitable, le **plan gratuit** inclut généralement ces limites d'essai :

- **Données d'essai :** jusqu'à **5 annonces** par run — suffisant pour vérifier la qualité des données.
- **Limite quotidienne :** **5 runs** par jour calendaire (UTC).
- **Entre les runs :** au moins **30 minutes** avant de pouvoir en lancer un autre.

> Les limites peuvent changer en fonction de la charge de la plateforme, du système et du type de scraping prévu.

##### Prêt à passer à l'échelle ?

Utilisez le plan gratuit pour décider si cet actor convient à votre projet. Les plans payants Apify suppriment les temps d'attente et les limites pour que vous puissiez travailler à plein régime — [**passez à un plan payant**](https://apify.com/pricing?fpr=cbgdsf).

#### 🔍 **Vous cherchez autre chose ?**

N'hésitez pas à explorer les [+4 000 scrapers préconstruits sur Apify Store](https://apify.com/store?fpr=cbgdsf) pour plus
d’options !

### English version

#### 🤩 Features

🚀 Our blazing fast pap.fr mass real estate items scraper lets you extract real estate items' information and export
them to various format (JSON, CSV, HTML etc..) 🔥 Bring your search URLs and you're good to go!
👉 It enables you to scrape rich details as title, descriptions, photos, energy information, construction date, price,
publisher information (email/phone number included) nearby transportation and a lot more.

#### 📚 How to use this actor

1. 👉 [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required!
2. 🎉 Just click the **"Get Started"** button and complete a quick signup.
3. 💰 A free account includes enough credits to test this actor.
4. ⏳ Enjoy scraping for the free trial period, no commitment or upfront payment required.

The scraper has a required `startUrl` parameter which holds the value of the search result page's link:

- Example: `https://www.pap.fr/annonce/locations-appartement-paris-11e-g37778-a-partir-de-6-chambres-jusqu-a-9-m2`

#### ⚠️ Is it legal to scrape pap.fr?

It is legal to scrape publicly available data such as real estate descriptions, prices, photos, nearby transportation
etc. Read our blog post on [the legality of web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) to learn more.

#### Do you need to scrape search results pages instead?

If you don’t have direct links to properties and need to scrape search page results all at once while wanting to gather
information in a structured format (JSON, Excel, XML, etc.), feel free to check out
the [Pap.fr mass products scraper (by items URLs)) ⚡](https://apify.com/azzouzana/pap-fr-mass-products-scraper-by-items-urls)

#### 🤔 Why scrape pap.fr?

pap.fr is one of the most popular real estate websites in France, with hundreds of thousand of ads, there's definitely
something for you out there!

So what could you do with all these ads?

- Find real estate for sale nearby
- Do market data analysis
- Build a real estate agent email list
- Collect housing data for research or personal purposes
- Compare collected data with home value index
- Use the data for overall real estate data analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

#### 🤑 Cost of usage

The cost of using this scraper is **$1.2 for every 1000 real estate scraped**. No hidden fees.

#### 🛠️ Input

| Field | Type | Description | Default value / Example
| ----- | ---- | ----------- | ------------- |
| `startUrl`  | `link` (required) | the direct URLs of the properties that the scraper will process. | `https://www.pap.fr/annonce/locations-appartement-paris-11e-g37778-a-partir-de-6-chambres-jusqu-a-9-m2` |
| `maxItemsToScrape ` | `number` (optional) | Maximum number of ads to scrape | 1

#### 🧐 Output

Output is stored in a dataset. Each item is information about a real estate item:

##### Sample output

An output might look like the below data structure:

```json
{
    "id": 461001892,
    "produit": "vente",
    "typebien": "appartement",
    "typebien_slug": "appartement",
    "typebien_label": "Appartement",
    "prix": "510.000 €",
    "nb_pieces": 5,
    "nb_chambres_max": 3,
    "marker": {
        "lat": 48.883958,
        "lng": 2.130591
    },
    "titre": "Le Vésinet (78110)",
    "caracteristiques": "Appartement / 5 pièces / 3 chambres / 88 m² / 5.795 € le m²",
    "video": null,
    "visite_virtuelle": null,
    "date": "31 janvier 2026",
    "classe_energie": {
        "lettre": "d",
        "description": "Logement avec une consommation annuelle d'énergie comprise entre 181 et 250 kWh/m²/an."
    },
    "classe_ges": {
        "lettre": "e",
        "description": "Logement avec une émission de gaz à effet de serre comprise entre 51 et 70 kgéqCO2/m²/an."
    },
    "texte": "Découvrez cet appartement **spacieux, lumineux et traversant** situé dans le quartier Princesse du Vésinet, au début de la rue de Verdun.\nSuperficie de 88 m², cet espace comprend 3 chambres, un grand salon salle à manger de 30 m2, une cuisine aménagée et une salle de bains, idéal pour une famille cherchant confort et praticité. **Plan idéal**.\n\nÀ l'extérieur, profitez d'un **joli balcon filant de 4 m² orienté plein sud**.\nLe bien est également doté  d'un emplacement de parking souterrain, un atout précieux pour la vie quotidienne et d'un garage à vélo commun intérieur. Situé au sein d'un immeuble de quatre étages avec ascenseur, cet appartement assure un accès facile et agréable.\n\nEn matière de transports, vous êtes à seulement 80 m d'un arrêt de bus et à 700 m de la gare Le Vésinet Centre, facilitant vos déplacements. Les commodités ne manquent pas, avec un supermarché bio à 100 m , une boulangerie, une pharmacie, un tabac, plusieurs restaurants et commerces de proximité. A moins d'un kilomètre, un Hyper U et une station essence. Pour les familles, une école maternelle et primaire se trouvent en face ainsi qu'un parc aménagé, parfait pour les enfants, à seulement 100 m.\n\nCet appartement représente une opportunité rare de vivre dans un cadre familial, alliant confort et accessibilité. N'attendez plus pour visiter et découvrir votre futur chez-vous !",
    "texte_accroche": "",
    "texte_contact": "",
    "telephones": [
        "01 40 56 35 45"
    ],
    "has_email": true,
    "photos": [
        "https://cdn.pap.fr/photos/pap/39/d6/39d6f23401ccf18ac22164071e26d56e/3-p1.jpg",
        "https://cdn.pap.fr/photos/pap/ce/39/ce39867e630a54a357eb00c387065589/c-p1.jpg",
        "https://cdn.pap.fr/photos/pap/ad/99/ad9945a23610b8ea0244b961bca89132/a-p1.jpg",
        "https://cdn.pap.fr/photos/pap/a9/5a/a95a3ae36dbd9d13c65afd281b597be3/a-p1.jpg",
        "https://cdn.pap.fr/photos/pap/de/a1/dea154c2cc89de22024b1759cd0f5dee/d-p1.jpg",
        "https://cdn.pap.fr/photos/pap/02/13/02131787aba8803854678fb6dd4a9dc5/0-p1.jpg",
        "https://cdn.pap.fr/photos/pap/c8/65/c8659c9f8c52b8e9ebe2777c5fdb00f2/c-p1.jpg",
        "https://cdn.pap.fr/photos/pap/22/88/22884f3f07951d8aae8b4a0c6d8bef00/2-p1.jpg",
        "https://cdn.pap.fr/photos/pap/f3/a5/f3a556823cfa356ea5cc46e130631ea3/f-p1.jpg",
        "https://cdn.pap.fr/photos/pap/6e/1c/6e1c88ad0918ae9f85dd7dbecb4f6ed3/6-p1.jpg",
        "https://cdn.pap.fr/photos/pap/08/86/08869e358567bac6e4ff93b57e9c131c/0-p1.jpg",
        "https://cdn.pap.fr/photos/pap/38/0b/380beb6639f39cb2a86d87b68e3829ad/3-p1.jpg"
    ],
    "transports": [
        {
            "label": "Le Vésinet - Centre",
            "pictos": [
                "rer-0",
                "rer-a"
            ]
        },
        {
            "label": "Le Vésinet - Le Pecq",
            "pictos": [
                "rer-0",
                "rer-a"
            ]
        },
        {
            "label": "Chatou - Croissy",
            "pictos": [
                "rer-0",
                "rer-a"
            ]
        }
    ],
    "prix_valide": false,
    "affiche_demarchage_refuse": true,
    "appel_video": null,
    "reference_courte": "G10/1892",
    "site_perso": null,
    "url": "https://www.pap.fr/annonces/-r461001892",
    "favori": false,
    "deja_contacte": null,
    "avant_premiere": false,
    "has_pass_avant_premiere": false,
    "__isFound": true,
    "__scrapedAt": "2026-01-31T21:27:29.131Z"
}
```

Come & explore!

#### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

##### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

***

**Need a custom solution? Have a feature request or just want to chat?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

#### 🔍 **Looking for something else?**

Feel free to explore [+4,000 pre-built scrapers on Apify Store](https://apify.com/store?fpr=cbgdsf) for more options!

# Actor input Schema

## `startUrl` (type: `string`):

Search URL / Lien vers la page de recherche

## `maxItemsToScrape` (type: `integer`):

maxItemsToScrape

## Actor input object example

```json
{
  "startUrl": "https://www.pap.fr/annonce/vente-appartements-paris-7e-g37774-studio-a-partir-de-1-chambres-jusqu-a-150000-euros",
  "maxItemsToScrape": 1000
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
    "startUrl": "https://www.pap.fr/annonce/vente-appartements-paris-7e-g37774-studio-a-partir-de-1-chambres-jusqu-a-150000-euros"
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/pap-fr-mass-products-scraper-by-search-url").call(input);

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
run_input = { "startUrl": "https://www.pap.fr/annonce/vente-appartements-paris-7e-g37774-studio-a-partir-de-1-chambres-jusqu-a-150000-euros" }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/pap-fr-mass-products-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.pap.fr/annonce/vente-appartements-paris-7e-g37774-studio-a-partir-de-1-chambres-jusqu-a-150000-euros"
}' |
apify call azzouzana/pap-fr-mass-products-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/pap-fr-mass-products-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
