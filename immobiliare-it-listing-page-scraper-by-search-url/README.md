# 🚀 Immobiliare.it Property Listings Scraper (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Immobiliare.it Property Listings Scraper (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/immobiliare-it-listing-page-scraper-by-search-url?fpr=cbgdsf)

---

## Immobiliare.it Property Listings Scraper (By Search URL)

### Versione italiana

#### 🤩 Panoramica

🚀 Il nostro scraper ultraveloce per gli annunci immobiliari di massa di immobiliare.it ti permette di estrarre informazioni sugli immobili da una pagina dei risultati di ricerca e di esportarle in diversi formati (JSON, CSV, HTML, ecc.) 🔥 Fornisci gli URL e sei pronto a partire!
👉 Ti consente di recuperare dettagli completi come titoli, descrizioni, foto, informazioni energetiche, data di costruzione, prezzo, foto e molto altro.

#### 📚 Come utilizzare questo actor

1. 👉 [Registrati per un account gratuito su Apify](https://apify.com/sign-up?fpr=cbgdsf) – non è necessaria la carta di credito!
2. 🎉 Clicca sul pulsante **"Get Started"** e completa una rapida registrazione.
3. 💰 L'account gratuito include abbastanza crediti per provare questo actor.
4. ⏳ Inizia a fare scraping durante il periodo di prova gratuito – nessun impegno o pagamento anticipato richiesto.

Lo scraper richiede un parametro obbligatorio `startUrl`, che è il link alla pagina di ricerca.
- Esempio: `https://www.immobiliare.it/vendita-case/roma/roma-70/?superficieMinima=60&mapCenter=41.840473%2C12.546644&zoom=13`

📝 Per ottenere questo URL, avvia la tua ricerca su `https://www.immobiliare.it` applicando i filtri desiderati, quindi copia il link generato dalla barra degli indirizzi.

#### ⚠️ È legale scrapare immobiliare.it?

È legale scrapare i dati pubblicamente disponibili, come descrizioni degli immobili, prezzi, foto, trasporti nelle vicinanze, ecc. Leggi il nostro articolo sul blog sulla [legalità del web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) per saperne di più.

#### 🤔 Perché scrappare immobiliare.it?

immobiliare.it è uno dei siti immobiliari più popolari in Italia ed Europa. Con decine di migliaia di annunci, c'è sicuramente qualcosa per te!

Quindi, cosa potresti fare con tutti questi dati sugli annunci immobiliari?

- Trovare immobili in vendita nelle vicinanze
- Fare un'analisi dei dati del mercato
- Creare un elenco di email di agenti immobiliari
- Raccogliere dati sugli alloggi per ricerche o esigenze personali
- Confrontare i dati raccolti con un indice di valore delle case
- Utilizzare i dati per un'analisi complessiva del mercato immobiliare

Queste sono solo alcune idee per aiutarti a riflettere su come il web scraping possa fornirti i dati di cui hai bisogno. Le possibilità sono infinite 🚀

#### 🤑 Costo di utilizzo

La fatturazione è in **Pay Per Event (PPE)** : paghi in base al numero di annunci inviati al dataset. La limite effettiva rispetta il tuo `maxItems`, il budget del run e il limite per utenti gratuiti (5 annunci).

Con il credito gratuito mensile di $5 di Apify puoi provare l'actor; per volumi maggiori consulta [Apify pricing](https://apify.com/pricing?fpr=cbgdsf).

#### 🆓 Limitazioni del piano gratuito

Vogliamo che tu possa vedere come funziona questo actor prima di impegnarti. Per mantenere le cose eque per tutti, il **piano gratuito** include di solito questi limiti di prova:

- **Dati di prova:** fino a **5 annunci** per run—sufficienti per verificare la qualità dei dati.
- **Limite giornaliero:** **5 run** al giorno di calendario (UTC).
- **Tra un run e l’altro:** almeno **30 minuti** prima di poterne avviare un altro.

> I limiti possono cambiare in base al carico della piattaforma, al carico del sistema e al tipo di scraping previsto.

##### Quando sei pronto a scalare

Usa il piano gratuito per capire se questo actor fa al caso tuo. I piani Apify a pagamento rimuovono tempi di attesa e limiti così puoi lavorare a pieno regime—[**passa a un piano a pagamento**](https://apify.com/pricing?fpr=cbgdsf).

#### 🛠️ Parametri di ingresso:

| Campo               | Tipo     | Descrizione                                                                  | Valore predefinito / Esempio                                                                 |
|---------------------|----------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| `startUrl`          | `link`   | (obbligatorio) gli URL diretti degli immobili che l'attore scrapperà         | `https://www.immobiliare.it/vendita-case/roma/roma-70/?prezzoMinimo=70000&superficieMinima=60` |
| `maxItems`          | `integer` | Numero massimo di annunci da estrarre (PPE: la limite effettiva considera anche budget e piano gratuito). | `2000` (max `5000`) |

#### 🧐 Risultato

I risultati sono salvati in un dataset (o "dataset" nel gergo di Apify). Ogni elemento contiene informazioni di un annuncio:

##### Esempio di risultato:

Un esempio di risultato potrebbe somigliare alla schermata qui sotto:

![screenshot](https://i.ibb.co/whZWvNT/image.png)

& molte altre informazioni che non appaiono nella schermata, vieni a esplorare!

#### 🔍 **Cerchi qualcos'altro?**
Sentiti libero di esplorare i [+4.000 scraper preconfigurati su Apify Store](https://apify.com/store?fpr=cbgdsf) per altre opzioni!

#### 📬 Contattaci

**Serve una soluzione su misura, una modifica o vuoi solo scriverci?**
Saremo lieti di risponderti.

- 💬 **Discord** : `@azzouzana`
- 📧 **Email** : [labs@azzouzana.com](mailto:labs@azzouzana.com)

#### ⚠️ Disclaimer
Questo Actor è uno strumento indipendente e non è affiliato, approvato o sponsorizzato da Immobiliare.it Group o da una qualsiasi delle sue consociate. Tutti i marchi commerciali menzionati sono di proprietà dei rispettivi titolari.

### English version

#### 🤩 Features

🚀 Our fast Immobiliare.it listing page scraper (by search URL) 🏠 lets you extract real estate items' information and export them to various formats (JSON, CSV, HTML, etc.). 🔥 Paste your search URL and you're good to go!
👉 It enables you to scrape rich details as title, descriptions, photos, prices, photos and a lot more!

#### 📚 How to use this actor

1. 👉 [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required!
2. 🎉 Just click the **"Get Started"** button and complete a quick signup.
3. 💰 A free account includes enough credits to test this actor.
4. ⏳ Enjoy scraping for the free trial period, no commitment or upfront payment required.

The scraper has a required `startUrl` parameter which holds the value of the search result page's link:
- Example:  `https://www.immobiliare.it/vendita-case/roma/roma-70/?superficieMinima=60&mapCenter=41.840473%2C12.546644&zoom=13`

#### ⚠️ Is it legal to scrape immobiliare.it?

It is legal to scrape publicly available data such as real estate descriptions, prices, photos, nearby transportation etc. Read our blog post on [the legality of web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) to learn more.

#### 🤔 Why scrape immobiliare.it?

immobiliare.it is one of the most popular real estate websites in Italy and Europe, with hundreds of thousand of ads, there's definitely something for you out there!

So what could you do with all these ads?

- Find real estate for sale nearby
- Do market data analysis
- Build a real estate agent email list
- Collect housing data for research or personal purposes
- Compare collected data with home value index
- Use the data for overall real estate data analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

#### 🤑 Cost of usage

Billing is **Pay Per Event (PPE)** — you pay per number of listings pushed to the dataset. The effective limit respects your `maxItems`, the run budget, and the free-tier cap (5 listings).

Use Apify's $5 free monthly credit to try the actor; see [Apify pricing](https://apify.com/pricing?fpr=cbgdsf) for higher volumes.

#### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping.

##### Upgrade when you’re ready to scale

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

#### 🛠️ Input

| Field | Type | Description | Default value / Example
| ----- | ---- | ----------- |-------------------------------------------------------------------------------------|
| `startUrl`  | `link` (required) | the direct URLs of the properties that the scraper will process. | `https://www.immobiliare.it/vendita-case/roma/roma-70/?superficieMinima=60&zoom=13` |
| `maxItems` | `integer` | Maximum number of listings to scrape (PPE: effective limit also respects budget and free-tier). | `2000` (max `5000`) |

#### 🧐 Output

Output is stored in a dataset. Each item is information about a real estate item:

##### Sample output

An output might look like the below screenshot:

![screenshot](https://i.ibb.co/whZWvNT/image.png)

& a lot more information  that the screenshot does not show, come & explore!

#### 🔍 **Looking for something else?**
Feel free to explore [+4,000 pre-built scrapers on Apify Store](https://apify.com/store?fpr=cbgdsf) for more options!

#### 📬 Contact us

**Need a custom solution, a feature request, or just want to chat?**
We'd love to hear from you.

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: [labs@azzouzana.com](mailto:labs@azzouzana.com)

#### ⚠️ Disclaimer
This Actor is an independent tool and is not affiliated with, endorsed by, or sponsored by Immobiliare.it Group or any of its subsidiaries. All trademarks mentioned are the property of their respective owners.

---

##### SEO Keywords
immobiliare.it scraper, scrape immobiliare.it, scrapare immobiliare.it, immobiliare.it API, real estate scraper Italy, Italian property scraper, annunci immobiliari scraper, export annunci immobiliare, Apify immobiliare, real estate data Italy, case in vendita scraper, affitti scraper Italia, scraper immobiliari Italia, dati immobiliare.it

# Actor input Schema

## `startUrl` (type: `string`):

URL to start with.
## `maxItems` (type: `integer`):

Maximum number of listings to scrape

## Actor input object example

```json
{
  "startUrl": "https://www.immobiliare.it/vendita-case/roma/roma-70/?prezzoMassimo=11000&superficieMinima=50",
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
    "startUrl": "https://www.immobiliare.it/vendita-case/roma/roma-70/?prezzoMassimo=11000&superficieMinima=50",
    "maxItems": 1000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/immobiliare-it-listing-page-scraper-by-search-url").call(input);

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
    "startUrl": "https://www.immobiliare.it/vendita-case/roma/roma-70/?prezzoMassimo=11000&superficieMinima=50",
    "maxItems": 1000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/immobiliare-it-listing-page-scraper-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.immobiliare.it/vendita-case/roma/roma-70/?prezzoMassimo=11000&superficieMinima=50",
  "maxItems": 1000
}' |
apify call azzouzana/immobiliare-it-listing-page-scraper-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/immobiliare-it-listing-page-scraper-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
