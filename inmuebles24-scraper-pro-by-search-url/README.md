# 🚀 Inmuebles24 Scraper — Sale, Rent & Commercial (By Search URL)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Inmuebles24 Scraper — Sale, Rent & Commercial (By Search URL). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/inmuebles24-scraper-pro-by-search-url?fpr=cbgdsf)

---

## Inmuebles24 Scraper — Sale, Rent & Commercial (By Search URL)

### Language / Idioma
[English Version](#english-version) | [Versión en Español](#versión-en-español)

---

### English Version

Extract listings from **[Inmuebles24.com](https://www.inmuebles24.com)**, Mexico's largest real estate marketplace. This actor scrapes search results with automatic pagination and enterprise-grade reliability.

#### 🌟 Key Features
- **Fast Performance**: Automatic pagination handling for seamless and thorough data extraction.
- **Rich, Flattened Data**: Structured JSON output ready for direct import into Excel, Google Sheets, or any external database.
- **Stealth Technology**: Native anti-bot bypass helps maintain access and high success rates.

#### 🚀 How It Works
1. **Enter Search URL**: Perform a search on Inmuebles24 and copy the URL (e.g., filtered by city, price, or property type).
2. **Configure**: Set your `maxItems` limit.
3. **Run**: Get fresh, structured data delivered in seconds.

##### Valid URLs examples
Copy any **search results** URL from your browser after you filter on Inmuebles24. For example:
- https://www.inmuebles24.com/inmuebles-en-venta-hasta-2000000-pesos.html
- https://www.inmuebles24.com/locales-comerciales-en-renta-hasta-2-recamaras.html
(Page suffixes such as `-pagina-2` are normalized automatically.)
- 
#### 💰 Cost Estimation (PPE)
This actor costs **$1.00 per 1,000 scraped listings**, no hidden fees.

| Scenario | Items scraped | Calculation | Total Cost |
| :--- | :--- | :--- | :--- |
| Example scrape | 1,000 | 1,000 × $0.001 | **$1.00** |
| Example scrape | 500 | 500 × $0.001 | **$0.50** |

#### SEO Keywords
inmuebles24 scraper, inmuebles24 api, mexico real estate, apify inmuebles24 scraper, housing market data mexico

#### Input Parameters
| Parameter | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `startUrl` | String | - | **Required**. The Inmuebles24 search results URL. |
| `maxItems` | Integer | `10` | Maximum number of items to scrape (up to 20,000). |

#### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

##### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

---

### Versión en Español

Extraiga anuncios inmobiliarios de **[Inmuebles24.com](https://www.inmuebles24.com)**, el portal inmobiliario más grande de México. Este actor extrae resultados de búsqueda con paginación automática y confiabilidad empresarial.

#### 🌟 Funciones Principales
- **Alto Rendimiento**: Manejo automático de paginación para una extracción de datos fluida y completa.
- **Datos Planos y Ricos**: Salida JSON estructurada lista para importar en Excel, Google Sheets o cualquier base de datos externa.

#### 🚀 Cómo Funciona
1. **URL de Búsqueda**: Realice una búsqueda en Inmuebles24 y copie la URL.
2. **Configuración**: Ajuste el límite de resultados (`maxItems`).
3. **Ejecución**: Reciba datos frescos y estructurados en segundos.

##### Ejemplos de URL válidas
Copie la URL de **resultados de búsqueda** del navegador después de aplicar filtros en Inmuebles24. Por ejemplo:
- https://www.inmuebles24.com/inmuebles-en-venta-hasta-2000000-pesos.html
- https://www.inmuebles24.com/locales-comerciales-en-renta-hasta-2-recamaras.html
(Los sufijos como `-pagina-2` se normalizan automáticamente.)
- 
#### 💰 Estimación de Costos (PPE)
Este actor cuesta **$1.00 USD por cada 1,000 listados extraídos**, sin cargos ocultos.

| Escenario | Elementos guardados | Cálculo | Costo Total |
| :--- | :--- | :--- | :--- |
| Ejemplo | 1,000 | 1,000 × $0.001 | **$1.00** |
| Ejemplo | 500 | 500 × $0.001 | **$0.50** |

#### Palabras Clave SEO
scraper inmuebles24, api inmuebles24, datos inmobiliarios méxico, extracción de datos inmobiliarios, bienes raíces méxico

#### Parámetros de Entrada
| Parámetro | Tipo | Default | Descripción |
| :--- | :--- | :--- | :--- |
| `startUrl` | String | - | **Requerido**. La URL de resultados de búsqueda de Inmuebles24. |
| `maxItems` | Integer | `10` | Número máximo de elementos a extraer (hasta 20,000). |

#### 🆓 Limitaciones de la versión gratuita

Queremos que vea cómo funciona este actor antes de comprometerse. Para que las cosas sean justas para todos, la **versión gratuita** suele incluir estos límites de prueba:

- **Datos de muestra:** hasta **5 listados** por ejecución, lo suficiente para comprobar la calidad de los datos.
- **Límite diario:** **5 ejecuciones** por día calendario (UTC).
- **Entre ejecuciones:** al menos **30 minutos** antes de poder iniciar otra ejecución.

> Los límites pueden cambiar con la carga de la plataforma según la carga del sistema y el raspado previsto.

##### Actualice cuando esté listo para escalar

Utilice el nivel gratuito para decidir si este actor se adapta a su proyecto. Los planes pagos de Apify eliminan estos tiempos de espera y límites para que pueda ejecutar a pleno volumen: [**actualice a un plan pago**](https://apify.com/pricing?fpr=cbgdsf).

---

#### Data Output / Ejemplo de Salida (Full Sorted Sample)
```json
{
	"alphanumeric_key": "63h74n",
	"alt": false,
	"avisoDuplicado": "aviso_sinduplicado_148695443",
	"descriptionNormalized": "Situada en la exclusiva zona de Puerto Cancún, esta impresionante residencia de aproximadamente 720 m² combina lujo...",
	"expenses_amount": 0,
	"expenses_currency": "MN",
	"flagsFeatures": [],
	"generatedTitle": "Casa · 720m² · 3 Recámaras · 4 Estacionamientos",
	"hasPlans": false,
	"hasTour": false,
	"hasVideos": false,
	"highlightedFeatures": [],
	"house_address_name": "Casas Venta En Venta Casa en Puerto Cancun, Cancún, Benito Juárez, Quintana Roo",
	"house_address_type": "PostalAddress",
	"house_image": "https://img10.naventcdn.com/avisos/18/01/48/69/54/43/720x532/1582687338.jpg",
	"house_name": "Casa · 720m² · 3 Recámaras · 4 Estacionamientos",
	"house_type": "House",
	"images": [
		"https://img10.naventcdn.com/avisos/18/01/48/69/54/43/720x532/1582687338.jpg?isFirstImage=true",
		"https://img10.naventcdn.com/avisos/18/01/48/69/54/43/720x532/1582687345.jpg",
    "..."
	],
	"leadWhatsappDevelopmentRequestData": true,
	"leadWhatsappPostingRequestData": true,
	"modified_date": "2026-02-26T14:29:06-0500",
	"operation_type": "Venta",
	"pixelPlus": false,
	"postingCode": "1HO7689226",
	"postingId": "148695443",
	"postingLocation_address_name": "En Venta Casa en Puerto Cancun",
	"postingLocation_address_visibility": "EXACT",
	"postingLocation_location_depth": 4,
	"postingLocation_location_label": "SUBZONA",
	"postingLocation_location_locationId": "V1-E-1111354",
	"postingLocation_location_name": "Puerto Cancún",
	"postingLocation_location_parent_depth": 3,
	"postingLocation_location_parent_label": "ZONA",
	"postingLocation_location_parent_locationId": "V1-D-50004155",
	"postingLocation_location_parent_name": "Cancún",
	"postingLocation_location_parent_parent_depth": 2,
	"postingLocation_location_parent_parent_label": "CIUDAD",
	"postingLocation_location_parent_parent_locationId": "V1-C-50000980",
	"postingLocation_location_parent_parent_name": "Benito Juárez",
	"postingLocation_location_parent_parent_parent_depth": 1,
	"postingLocation_location_parent_parent_parent_label": "PROVINCIA",
	"postingLocation_location_parent_parent_parent_locationId": "V1-B-83",
	"postingLocation_location_parent_parent_parent_name": "Quintana Roo",
	"postingLocation_location_parent_parent_parent_parent_depth": 0,
	"postingLocation_location_parent_parent_parent_parent_label": "PAIS",
	"postingLocation_location_parent_parent_parent_parent_locationId": "V1-A-18",
	"postingLocation_location_parent_parent_parent_parent_name": "Mexico",
	"postingLocation_postingGeolocation_geolocation_latitude": 21.2080761,
	"postingLocation_postingGeolocation_geolocation_longitude": -86.8445552,
	"postingLocation_postingGeolocation_urlStaticMap": "https://maps.google.com/maps/api/staticmap?center=21.2080761,-86.8445552&zoom=16&size=780x456&sensor=true&scale=2&...",
	"postingType": "PROPERTY",
	"premier": true,
	"price_amount": 2500000,
	"price_currency": "USD",
	"publicationAreaId": "3",
	"publisher_approved": false,
	"publisher_created_date": 1753761600000,
	"publisher_id_portal": "101",
	"publisher_name": "101 Most Exclusive by Bustamante",
	"publisher_premier": true,
	"publisher_publisherId": "102891459",
	"publisher_publisherTags": [],
	"publisher_publisherTypeId": "2",
	"publisher_slot": "aviso_sinslot_148695443",
	"publisher_slug": "",
	"publisher_url": "https://www.inmuebles24.com/inmobiliarias/101-most-exclusive-by-bustamante_102891459-inmuebles.html",
	"publisher_urlLogo": "https://img10.naventcdn.com/empresas/18/01/02/89/14/59/130x70/logo_bustamante-group_1754026822917.jpg",
	"realEstateType_name": "Casas",
	"realEstateType_realEstateTypeId": "1",
	"requestVisit5A_activeModal5A": false,
	"requestVisit5A_activeModalPostlead5A": false,
	"requestVisit5A_cronutRent": false,
	"requestVisit5A_cronutSell": false,
	"requestVisit5A_showWhatsapp": false,
	"reserved": false,
	"status": "ONLINE",
	"title": "En Venta Casa en Puerto Cancun",
	"triggerPill": "Zona exclusiva",
	"trigger_pills": [
		"Zona exclusiva_0.9_*",
		"Lujo y confort_0.8_*",
		"Ubicación privilegiada_0.9_*",
		"Entorno privado_0.7_*",
		"Alta plusvalía_0.8_*"
	],
	"units": [],
	"url": "https://www.inmuebles24.com/propiedades/clasificado/veclcain-en-venta-casa-en-puerto-cancun-148695443.html",
	"viewPhoneAnonymousLead": false,
	"whatsApp": "52 9981647683"
}
````

#### Contact 📬

**Need a custom solution? Have a feature request or just want to chat?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

# Actor input Schema

## `startUrl` (type: `string`):

Inmuebles24 search results URL / URL de resultados de búsqueda de Inmuebles24

## `maxItems` (type: `integer`):

Maximum number of listings to scrape / Número máximo de elementos a extraer

## Actor input object example

```json
{
  "startUrl": "https://www.inmuebles24.com/inmuebles-en-venta-desde-6000000-pesos.html",
  "maxItems": 10
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
    "startUrl": "https://www.inmuebles24.com/inmuebles-en-venta-desde-6000000-pesos.html"
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/inmuebles24-scraper-pro-by-search-url").call(input);

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
run_input = { "startUrl": "https://www.inmuebles24.com/inmuebles-en-venta-desde-6000000-pesos.html" }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/inmuebles24-scraper-pro-by-search-url").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.inmuebles24.com/inmuebles-en-venta-desde-6000000-pesos.html"
}' |
apify call azzouzana/inmuebles24-scraper-pro-by-search-url --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/inmuebles24-scraper-pro-by-search-url",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
