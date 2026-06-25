# 🚀 Willhaben.at Scraper — Marktplatz, Jobs, Autos & Immobilien (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Willhaben.at Scraper — Marktplatz, Jobs, Autos & Immobilien (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/willhaben-suchseiten-scraper-marktplatz-jobs-immobilien-autos?fpr=cbgdsf)

---

## Willhaben.at Scraper — Marktplatz, Jobs, Autos & Immobilien (By Search URL)

### Deutsch Version

#### 🤩 Funktionen

🚀 Unser **blitzschneller Willhaben.at Scraper** 🏠 ermöglicht es dir, Inserate aus den Bereichen **Marktplatz**, **Jobs**, **Autos & Motor** sowie **Immobilien** auf [willhaben.at](https://www.willhaben.at) zu extrahieren und sie in verschiedenen Formaten (JSON, CSV, HTML usw.) zu exportieren.

🔥 Gib einfach deine Such-URLs an (optional mit angewendeten Filtern) – und schon kannst du loslegen!

👉 Du kannst äußerst detaillierte Anzeigeninformationen extrahieren – darunter Titel, Dokumente, E-Mails, Bilder, Adressen, Daten, Kontaktdetails und eine Vielzahl weiterer Angaben.

#### 📚 So verwendest du diesen Actor

1. 👉 [Registriere dich für ein kostenloses Apify-Konto](https://apify.com/sign-up?fpr=cbgdsf) – keine Kreditkarte erforderlich!
2. 🎉 Klicke einfach auf **„Get Started“** und schließe die schnelle Anmeldung ab.
3. 💰 Ein kostenloses Konto enthält genügend Credits, um diesen Actor zu testen.
4. Gib dem Actor eine gültige `startUrl` (eine Suchseiten-URL mit angewendeten Filtern) und klicke auf **„Run“**.
5. ⏳ Genieße das Scraping während der kostenlosen Testphase – ohne Verpflichtung oder Vorauszahlung.

Der Scraper benötigt den Parameter `startUrl`. Dabei handelt es sich um die URL einer Suchseite mit angewendeten Filtern.

- Beispiele für gültige URLs:
    - **Marktplatz**  
      Beispiel: `https://www.willhaben.at/iad/kaufen-und-verkaufen/marktplatz/mode-accessoires-3275/a/marke-louis-vuitton-4744?rows=30&isNavigation=true&ISPRIVATE=0`
    - **Jobs**  
      Beispiel: `https://www.willhaben.at/jobs/suche/freiberuflich`
    - **Immobilien**  
      Beispiel: `https://www.willhaben.at/iad/immobilien/mietwohnungen/mietwohnung-angebote?isNavigation=true&rows=30&page=1&PRICE_TO=400`
    - **Autos & Motor**  
      Beispiel: `https://www.willhaben.at/iad/gebrauchtwagen/auto/gebrauchtwagenboerse?isNavigation=true&CAR_TYPE=4&rows=30&page=1&YEAR_MODEL_FROM=2022&PRICE_TO=15000`

#### 🤑 Nutzungskosten

Dieser Actor funktioniert nach dem Prinzip **„Zahle nur für das, was du bekommst“**, keine versteckten Gebühren 🤩


##### Preisbeispiele (1,00 $ / 1.000 Elemente)

Du scrapst 2.000 Elemente.
*   Kosten: 2 * 1,00 $ = **2,00 $**


#### 🛠️ Eingabe

| Feld | Typ | Beschreibung | Standardwert / Beispiel |
|------|-----|--------------|-------------------------|
| `startUrl` | `URL` | Die Such-URL (Marktplatz, Jobs, Autos & Motor oder Immobilien) | Siehe Abschnitt **„So verwendest du diesen Actor“** für Beispiele |
| `maxItems` | `integer` | Maximale Anzahl der zu scrapenden Inserate | `25` (Der Actor kann pro Durchlauf maximal 10.000 Elemente scrapen) |

#### 🆓 Kostenlose Testversion Einschränkungen

Wir möchten, dass Sie sehen, wie dieser Actor funktioniert, bevor Sie sich festlegen. Um die Dinge für alle fair zu halten, die **kostenlose Testversion** normalerweise diese Testlimits:

- **Beispieldaten:** bis zu **5 Anzeigen** pro Durchlauf – ausreichend, um die Datenqualität zu prüfen.
- **Tägliches Limit:** **5 Durchläufe** pro Kalendertag (UTC).
- **Zwischen den Durchläufen:** mindestens **30 Minuten**, bevor Sie einen weiteren Durchlauf starten können.

> Die Limits können sich je nach Systemlast und Ihrem beabsichtigten Scraping-Volumen ändern.

##### Upgrade, wenn Sie bereit sind zu skalieren

Nutzen Sie die kostenlose Testversion, um zu entscheiden, ob dieser Actor zu Ihrem Projekt passt. Kostenpflichtige Apify-Pläne entfernen diese Wartezeiten und Obergrenzen, sodass Sie mit vollem Volumen arbeiten können – [**Upgrade auf einen kostenpflichtigen Plan**](https://apify.com/pricing?fpr=cbgdsf).

#### 🧐 Ausgabe

Die Ergebnisse werden in einem Dataset gespeichert. Jedes Element enthält Informationen zu einem extrahierten Inserat.

#### ⚠️ Haftungsausschluss

Dieser Actor ist ein unabhängiges Tool und steht in keiner Verbindung zu, wird nicht unterstützt oder gesponsert von der **willhaben internet service GmbH & Co KG** oder deren Tochtergesellschaften.  
Alle erwähnten Marken sind Eigentum der jeweiligen Rechteinhaber.

#### � SEO Keywords
`Willhaben Scraper`, `Willhaben Immobilien Scraper`, `Willhaben Auto Marktdaten`, `Willhaben Jobbörse Scraper`, `Willhaben Marktplatz Scraper`, `Willhaben Jobs Scraper`, `Willhaben Auto Scraper`.

#### �📬 Kontakt & Support

**Benötigst du eine maßgeschneiderte Lösung? Hast du einen Feature-Wunsch?**
Wir würden uns freuen, von dir zu hören!

- 💬 **Discord**: `@azzouzana`
- 📧 **E-Mail**: [labs@azzouzana.com](mailto:labs@azzouzana.com)

---


### English version

#### 🤩 Features


🚀 Our **blazing-fast Willhaben.at scraper** 🏠 lets you extract listings from the **Marketplace**, **Jobs**
, **Cars & Motor**, and **Properties** sections of [willhaben.at](https://www.willhaben.at), and export them in various
formats (JSON, CSV, HTML, etc.).

🔥 Simply provide your search URLs (optionally with filters applied) and you’re all set!

👉 It lets you extract highly detailed ad information — including titles, documents, emails, images, addresses, dates,
contact details, and a whole range of other data.

#### 📚 How to use this actor

1. 👉 [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required!
2. 🎉 Just click the **"Get Started"** button and complete a quick signup.
3. 💰 A free account includes enough credits to test this actor.
4. Feed the actor with a valid `startUrl` (a search page URL with filters applied) and click the **"Run"** button.
5. ⏳ Enjoy scraping for the free trial period, no commitment or upfront payment required.

The scraper has a required `startUrl` parameter which is a URL to a search page with filters applied.

- Examples of valid URLs:
    - Marketplace
      example: `https://www.willhaben.at/iad/kaufen-und-verkaufen/marktplatz/mode-accessoires-3275/a/marke-louis-vuitton-4744?rows=30&isNavigation=true&ISPRIVATE=0`
    - Jobs example: `https://www.willhaben.at/jobs/suche/freiberuflich`
    - Properties
      example `https://www.willhaben.at/iad/immobilien/mietwohnungen/mietwohnung-angebote?isNavigation=true&rows=30&page=1&PRICE_TO=400`
    - Cars & motor
      example: `https://www.willhaben.at/iad/gebrauchtwagen/auto/gebrauchtwagenboerse?isNavigation=true&CAR_TYPE=4&rows=30&page=1&YEAR_MODEL_FROM=2022&PRICE_TO=15000`

#### 🤑 Cost of usage

This actor operates on a **Pay-for-what-you-get** model, no hidden fees 🤩


##### Pricing Examples ($1.00 / 1,000 items)

You scrape 2,000 items.
*   Cost: 2 * $1.00 = **$2.00**


#### 🛠️ Input

| Field | Type | Description | Default value / Example                                                                                  |
| ----- | ---- | ----------- |----------------------------------------------------------------------------------------------------------|
| `startUrl` | `URL` | the search URL (Marketplace, jobs, Cars & Motors or Real estate properties search URL) |  See `How to use this actor` section for some examples |
| `maxItems` | `integer` | The maximum number of items to scrape. | `25` (The actor scrapes a maximum of 10K per execution) |

#### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

##### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

#### 🧐 Output

Output is stored in a dataset. Each item is information about an extracted job.

#### ⚠️ Disclaimer

This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by willhaben internet service
GmbH & Co KG or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

#### 🔎 SEO Keywords
`Willhaben Scraper`, `Willhaben immobiliens craper`, `Willhaben Cars Market Data`, `Willhaben Jobs Board Scraper`, `Willhaben real estate scraper`, `Willhaben Marketplatz scraper`, `Willhaben Jobs scraper`, `Willhaben Cars scraper`, `Willhaben Immobilien scraper`, `Willhaben scraper`, `Willhaben Immobilien scraper`

---

#### 📬 Contact & Support

**Need a custom solution? Have a feature request?**
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: [labs@azzouzana.com](mailto:labs@azzouzana.com)

---

# Actor input Schema

## `startUrl` (type: `string`):

URL der Suchergebnisseite | Search results page URL
## `maxItems` (type: `integer`):

Anzahl der Inserate, die gescraped werden sollen. | Number of items to scrape.

## Actor input object example

```json
{
  "startUrl": "https://www.willhaben.at/iad/immobilien/mietwohnungen/mietwohnung-angebote?NO_OF_ROOMS_BUCKET=10X&page=1&ESTATE_SIZE/LIVING_AREA_FROM=20",
  "maxItems": 5000
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
    "startUrl": "https://www.willhaben.at/iad/immobilien/mietwohnungen/mietwohnung-angebote?NO_OF_ROOMS_BUCKET=10X&page=1&ESTATE_SIZE/LIVING_AREA_FROM=20",
    "maxItems": 5000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/willhaben-suchseiten-scraper-marktplatz-jobs-immobilien-autos").call(input);

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
    "startUrl": "https://www.willhaben.at/iad/immobilien/mietwohnungen/mietwohnung-angebote?NO_OF_ROOMS_BUCKET=10X&page=1&ESTATE_SIZE/LIVING_AREA_FROM=20",
    "maxItems": 5000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/willhaben-suchseiten-scraper-marktplatz-jobs-immobilien-autos").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.willhaben.at/iad/immobilien/mietwohnungen/mietwohnung-angebote?NO_OF_ROOMS_BUCKET=10X&page=1&ESTATE_SIZE/LIVING_AREA_FROM=20",
  "maxItems": 5000
}' |
apify call azzouzana/willhaben-suchseiten-scraper-marktplatz-jobs-immobilien-autos --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/willhaben-suchseiten-scraper-marktplatz-jobs-immobilien-autos",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
