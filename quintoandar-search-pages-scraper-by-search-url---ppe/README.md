# 🚀 QuintoAndar Real Estate Scraper (By search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the QuintoAndar Real Estate Scraper (By search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/quintoandar-search-pages-scraper-by-search-url---ppe?fpr=cbgdsf)

---

## QuintoAndar Real Estate Scraper (By search URL)

A ferramenta mais poderosa e eficiente para extrair dados imobiliários do [QuintoAndar](https://www.quintoandar.com.br). Seja para analisar tendências de mercado, monitorar preços ou construir um portal imobiliário, este actor fornece dados estruturados e de alta qualidade **em segundos**.

### 🚀 Principais Funcionalidades

- **Desempenho Ultra Rápido**: Otimizado para velocidade máxima.
- **Modo de Raspagem Profunda**: Vá além dos resultados de pesquisa. Extraia detalhes completos da propriedade, incluindo comodidades quarto por quarto, instalações do prédio, insights profundos do bairro, endereço e muito mais.
- **Fácil de Usar**: Basta inserir o URL de pesquisa do QuintoAndar e deixar o actor fazer o resto. Sem necessidade de conhecimento técnico ou configuração complexa.

---

### 🔍 Como Começar

1.  **Pesquisar**: Vá para [QuintoAndar.com.br](https://www.quintoandar.com.br) e execute sua pesquisa normalmente.
2.  **Copiar URL**: Copie o URL da barra de endereços do seu navegador. Exemplo `https://www.quintoandar.com.br/alugar/imovel/sao-paulo-sp-brasil/de-500-a-1000-aluguel/de-20-a-30-m2`
3.  **Executar**: Cole o URL no campo `searchUrl` deste actor e clique em **Iniciar**.

---

### 🛠️ Configuração

| Campo | Tipo | Padrão | Descrição |
| :--- | :--- | :--- | :--- |
| `searchUrl` | String | (Obrigatório) | O URL dos resultados de pesquisa do QuintoAndar. |
| `maxItems` | Número | `12` | Número máximo de itens a processar |

---

<a name="sample-output-pt"></a>
### 📊 Exemplo de Saída

O actor fornece um conjunto de dados rico. Abaixo está uma entrada de exemplo de propriedade:

```json
{
	"acceptsPets": false,
	"address": {
		"city": "São Paulo",
		"country": "Brasil",
		"countryCode": "BR",
		"countryName": "Brasil",
		"lat": -23.5273021,
		"lng": -46.4672914,
		"neighborhood": "Cidade Antônio Estêvão de Carvalho",
		"stateAcronym": "SP",
		"stateName": "São Paulo",
		"street": "Avenida Caititu",
		"zipCode": "08223-000"
	},
	"allowDirectOffer": true,
	"amenities": [
        {
			"key": "VARANDA",
			"optional": false,
			"text": "Varanda",
			"value": "NAO"
		},
		{
			"key": "PISCINA_PRIVATIVA",
			"optional": false,
			"text": "Piscina privativa",
			"value": "NAO"
		},
		{
			"key": "ARMARIOS_EMBUTIDOS_NO_QUARTO",
			"optional": false,
			"text": "Armários no quarto",
			"value": "NAO"
		}
        ...
	],
	"condoPrice": 0,
	"condoType": "IncluidoNoAluguel",
	"condominium": {
		"error": {
			"details": {
				"code": 404,
				"message": "Not found exception. Entity id: dyosw9xryk"
			},
			"response": {}
		}
	},
	"constructionYear": null,
	"displayId": "1330901",
	"error": false,
	"forRent": true,
	"forSale": false,
	"generatedDescription": {},
	"hasFurniture": false,
	"homeProtection": 12,
	"houseAgent": {
		"alreadyOpenedByQueryParam": false,
		"isDialogOpen": false
	},
	"houseVisitStatus": "ACCEPT_NEW",
	"id": "894030901",
	"installations": [
		{
			"key": "PISCINA",
			"text": "Piscina",
			"value": "NAO"
		},
		{
			"key": "CHURRASQUEIRA",
			"text": "Churrasqueira",
			"value": "NAO"
		},
		{
			"key": "SAUNA",
			"text": "Sauna",
			"value": "NAO"
		}
        ...
	],
	"iptu": 0,
	"iptuType": "NaoInformado",
	"isGalleryModalOpen": false,
	"isNearSubway": false,
	"isNewOrRenovated": false,
	"isPrimaryMarket": false,
	"isReserved": false,
	"lastPublishedDate": "2025-12-18T17:49:01.000Z",
	"listingPublication": "not_stranded",
	"listingTags": [],
	"listings": [
		{
			"businessContext": "RENT",
			"firstPublicationDate": "2023-04-14T21:24:10.000+0000",
			"imovelId": 894030901,
			"isEarlyRelisting": true,
			"lastPublicationDate": "2025-12-18T17:49:01.000+0000",
			"listingRentModel": {
				"listingBusinessContextId": 1555934,
				"rentalAdministrator": "QUINTOANDAR"
			},
			"ownership": "STANDARD",
			"relistingDetailsDTO": {
				"isEarlyRelisting": true,
				"isOwnerInRelistingExperiment": true,
				"isRelistingPublished": true,
				"isRelistingScheduled": false,
				"isUnderTermination": true,
				"newContractCreatedId": null,
				"possibleMovingDate": "2026-01-27T00:00:00.000+0000",
				"publishAllowed": true,
				"relistingPublishDate": "2025-12-18T17:49:01.000+0000",
				"underTerminationContractId": 543001
			},
			"status": "publicado",
			"statusReason": "RELISTING_OFFER",
			"suspensionReason": "RELISTING"
		}
	],
	"loaded": true,
	"loading": false,
	"loadingCategorizedRooms": false,
	"macroRegion": {
		"id": 2767,
		"name": "SPOO13"
	},
	"mortgageFirstInstallment": 0,
	"parkingSpaces": 0,
	"photos": [
		{
			"cover": true,
			"id": 37657938,
			"subtitle": "Quarto Suíte",
			"url": "894030901-451.57199404263616AvenidaCaititu1268Casa41.JPG"
		},
		{
			"cover": false,
			"id": 37657941,
			"subtitle": "Quarto Suíte",
			"url": "894030901-465.0701435281591AvenidaCaititu1268Casa42.JPG"
		}
        ...
	],
	"photosCategorizedByRooms": [],
	"placesNearby": [
		{
			"name": "SESI Cidade AE Carvalho",
			"slug": "sesi-cidade-ae-carvalho-artur-alvim-sao-paulo-sp",
			"type": "SCHOOL"
		},
		{
			"name": "Shopping Metrô Itaquera",
			"slug": "shopping-metro-itaquera-itaquera-sao-paulo-sp",
			"type": "SHOPPING_MALL"
		},
		{
			"name": "Centro Social Santa Luzia",
			"slug": "centro-social-santa-luzia-artur-alvim-sao-paulo-sp",
			"type": "SCHOOL"
		}
	],
	"practicalityCommodities": [
        {
			"key": "BOX",
			"optional": false,
			"text": "Box",
			"value": "NAO"
		},
		{
			"key": "ARMARIOS_EMBUTIDOS_NO_QUARTO",
			"optional": false,
			"text": "Armários no quarto",
			"value": "NAO"
		},
        ...
	],
	"promotions": [],
	"rangeFloor": {},
	"region": {
		"hub": {
			"enabled": false,
			"isPrimaryMarket": false,
			"loading": "UNSET"
		},
		"id": 2368,
		"name": "Itaquera"
	},
	"regionParameters": {
		"RENT": {
			"talkToAgentEnabled": false,
			"visitsEnabled": true
		},
		"SALE": {
			"talkToAgentEnabled": false,
			"visitsEnabled": true
		},
		"loaded": false,
		"loading": false
	},
	"relevantRegions": [],
	"remarks": "",
	"rentOnTermination": true,
	"rentPrice": 700,
	"rentalGuarantee": {
		"loaded": true,
		"maxValue": 525,
		"minValue": 175,
		"value": 0
	},
	"reservationAvailability": null,
	"salePrice": 0,
	"selectedMedia": "tenant/HouseMedia/GALLERY_PHOTOS",
	"showUrlHasBeenCopiedSnackbar": false,
	"specialConditions": [
		"Exclusivity"
	],
	"status": "published",
	"suites": 1,
	"tenantServiceFee": 18,
	"terminationDate": "2026-01-05",
	"totalCost": 730,
	"type": "Casa",
	"video": "",
	"visitStatusReason": null,
	"visitsUnavailable": false
}
````

### 🆓 Limitações do Plano Gratuito

Queremos que você veja como este actor funciona antes de se comprometer. Para manter as coisas justas para todos, o **plano gratuito** geralmente inclui estes limites de teste:

- **Dados de amostra:** até **5 anúncios** por execução—o suficiente para verificar a qualidade dos dados.
- **Limite diário:** **5 execuções** por dia civil (UTC).
- **Entre execuções:** pelo menos **30 minutos** antes de poder iniciar outra execução.

> Os limites podem mudar com a carga da plataforma, dependendo da carga do sistema e do seu volume de raspagem planejado.

#### Atualize quando estiver pronto para escalar

Use o plano gratuito para decidir se este actor se encaixa no seu projeto. Os planos pagos da Apify removem esses tempos de espera e limites para que você possa executar em volume total—[**atualize para um plano pago**](https://apify.com/pricing?fpr=cbgdsf).

***

### 📬 Contato e Soluções Personalizadas

Precisa de um raspador personalizado, entrega de dados históricos ou integração de API?

- **Discord**: `@azzouzana`
- **Email**: `labs@azzouzana.com`

***

***

## QuintoAndar Real Estate Scraper

The most powerful and efficient tool for extracting real estate data from [QuintoAndar](https://www.quintoandar.com.br). Whether you are analyzing market trends, monitoring prices, or building a property portal, this actor provides high-quality, structured data **in seconds**

### 🚀 Key Features

- **Blazing Fast Performance**: Optimized for maximum speed.
- **Deep Scraping Mode**: Go beyond search results. Extract full property details including room-by-room amenities, building installations, and deep neighborhood insights, addtresse & much more
- **Easy to Use**: Just plug in your QuintoAndar search URL and let the actor do the rest. No technical knowledge or complex configuration required

***

### 🔍 How to Start

1. **Search**: Go to [QuintoAndar.com.br](https://www.quintoandar.com.br) and execute your search as usual.
2. **Copy URL**: Copy the URL from your browser's address bar. Example `https://www.quintoandar.com.br/alugar/imovel/sao-paulo-sp-brasil/de-500-a-1000-aluguel/de-20-a-30-m2`
3. **Run**: Paste the URL into the `searchUrl` input field of this actor and click **Start**.

***

### 🛠️ Configuration

| Field | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `searchUrl` | String | (Required) | The QuintoAndar search results URL. |
| `maxItems` | Number | `12` | Maximum number of items to process |

***

### 📊 Sample Output

The actor provides a rich dataset. Below is a sample property entry:

> *([See JSON output in the Portuguese section above](#exemplo-de-saida))*

***

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

***

### 📬 Contact & Custom Solutions

Need a custom scraper, historical data delivery, or API integration?

- **Discord**: `@azzouzana`
- **Email**: `labs@azzouzana.com`

# Actor input Schema

## `searchUrl` (type: `string`):

A URL de busca do QuintoAndar a partir da qual iniciar | The QuintoAndar search URL to start from.

## `maxItems` (type: `integer`):

Número máximo de itens a serem coletados | Maximum number of items to scrape.

## Actor input object example

```json
{
  "searchUrl": "https://www.quintoandar.com.br/alugar/imovel/sao-paulo-sp-brasil",
  "maxItems": 12
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
    "searchUrl": "https://www.quintoandar.com.br/alugar/imovel/sao-paulo-sp-brasil"
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/quintoandar-search-pages-scraper-by-search-url---ppe").call(input);

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
run_input = { "searchUrl": "https://www.quintoandar.com.br/alugar/imovel/sao-paulo-sp-brasil" }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/quintoandar-search-pages-scraper-by-search-url---ppe").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "searchUrl": "https://www.quintoandar.com.br/alugar/imovel/sao-paulo-sp-brasil"
}' |
apify call azzouzana/quintoandar-search-pages-scraper-by-search-url---ppe --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/quintoandar-search-pages-scraper-by-search-url---ppe",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
