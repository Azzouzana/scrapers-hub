# 🚀 Inmuebles24 Listing Details Scraper (By Listings URLs)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Inmuebles24 Listing Details Scraper (By Listings URLs). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/inmuebles24-details-scraper-by-listings-urls?fpr=cbgdsf)

---

## Inmuebles24 Listing Details Scraper (By Listings URLs)

### Language / Idioma
[English Version](#english-version) | [Versión en Español](#versión-en-español)

---

### English Version

**Get full property details — contact info, phone numbers, description, features, and more — from any Inmuebles24 listing. Just paste your URLs!**

#### 🌟 Key Features
- **Full Contact Info**: Extracts comprehensive listing data — emails, phones, publisher ratings & much more.
- **Fast & Reliable**: Enterprise-grade reliability with stealth techniques — zero browser overhead.
- **Batch Processing**: Send hundreds or thousands of listing URLs in a single run.
- **Rich, Flattened Data**: Structured JSON output ready for Excel, Google Sheets, APIs, or any database.

#### 🚀 How It Works
1. **Paste URLs**: Provide one or more Inmuebles24 listing URLs.
2. **Run**: The actor fetches full details for each listing and outputs structured data.
3. **Export**: Download your results as JSON, CSV, or push them directly to your database.

#### 💰 Cost Estimation (PPE)
Simple and transparent Pay-Per-Result pricing:
- **Detail Cost**: $2.50 per 1,000 results.

#### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse. 

##### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

##### Pricing Examples:
| Scenario | Listings | Calculation | Total Cost |
| **10 listings** | 10 | 10 × $0.0025 | **$0.025** |
| **100 listings** | 100 | 100 × $0.0025 | **$0.25** |
| **1,000 listings** | 1,000 | 1,000 × $0.0025 | **$2.50** |
| **Free user** | 5 (max) | 5 × $0.0025 | **$0.0125** |

#### Input Parameters
| Parameter | Type | Description | Format/Example |
| :--- | :--- | :--- | :--- |
| `startUrls` | Array | **Required**. List of Inmuebles24 listing URLs. | `["https://www.inmuebles24.com/propiedades/clasificado/ejemplo-departamento-12345678.html"]` |

#### What Data You Get
Each result includes:
- **Title & Description** — Full listing text
- **Price** — Amount, currency, formatted price
- **Contact Info** — Phone numbers (with international format & type), emails, contact name, WhatsApp availability
- **Location** — Address, zone, city, state, postal code, lat/lng coordinates
- **Features** — Bedrooms, bathrooms, parking, area (m²), age, and all other features
- **Publisher** — Agency name, ID, premier status, ratings
- **Images** — All listing photo URLs
- **Publication** — Begin/end dates, plan type
- …and much more!

#### SEO Keywords
inmuebles24 scraper, inmuebles24 details, inmuebles24 phone number, inmuebles24 contact info, mexico real estate api, property details extractor, listing data scraper

---

### Versión en Español

**Obtén los detalles completos de la propiedad — información de contacto, teléfonos, descripción, características y más — de cualquier anuncio de Inmuebles24. ¡Solo pega tus URLs!**

#### 🌟 Funciones Principales
- **Información de Contacto Completa**: Extrae datos completos del anuncio — correos, teléfonos, calificaciones del anunciante y mucho más.
- **Rápido y Confiable**: Tecnología empresarial con técnicas stealth — sin necesidad de navegador.
- **Procesamiento por Lotes**: Envía cientos o miles de URLs de anuncios en una sola ejecución.
- **Datos Planos y Ricos**: Salida JSON estructurada lista para Excel, Google Sheets, APIs o cualquier base de datos.

#### 🚀 Cómo Funciona
1. **Pega URLs**: Proporciona una o más URLs de anuncios de Inmuebles24.
2. **Ejecuta**: El actor obtiene detalles completos de cada anuncio y genera datos estructurados.
3. **Exporta**: Descarga tus resultados como JSON, CSV, o envíalos directamente a tu base de datos.

#### 💰 Estimación de Costos (PPE)
Precios simples y transparentes por resultado:
- **Costo por Detalle**: $3.00 por cada 1,000 resultados.

#### 🆓 Limitaciones de la versión gratuita

Queremos que vea cómo funciona este actor antes de comprometerse. Para que las cosas sean justas para todos, la **versión gratuita** suele incluir estos límites de prueba:

- **Datos de muestra:** hasta **5 listados** por ejecución, lo suficiente para comprobar la calidad de los datos.
- **Límite diario:** **5 ejecuciones** por día calendario (UTC).
- **Entre ejecuciones:** al menos **30 minutos** antes de poder iniciar otra ejecución.

> Los límites pueden cambiar con la carga de la plataforma según la carga del sistema y el raspado previsto.

##### Actualice cuando esté listo para escalar

Utilice el nivel gratuito para decidir si este actor se adapta a su proyecto. Los planes pagos de Apify eliminan estos tiempos de espera y límites para que pueda ejecutar a pleno volumen: [**actualice a un plan pago**](https://apify.com/pricing?fpr=cbgdsf).

##### Ejemplos de Precios:
| Escenario | Anuncios | Cálculo | Costo Total |
| :--- | :--- | :--- | :--- |
| 10 anuncios | 10 | 10 × $0.003 | **$0.03** |
| 100 anuncios | 100 | 100 × $0.003 | **$0.30** |
| 1,000 anuncios | 1,000 | 1,000 × $0.003 | **$3.00** |
| Usuario gratuito | 5 (máx) | 5 × $0.003 | **$0.015** |

#### Parámetros de Entrada
| Parámetro | Tipo | Descripción | Formato/Ejemplo |
| :--- | :--- | :--- | :--- |
| `startUrls` | Array | **Requerido**. Lista de URLs de anuncios de Inmuebles24. | `["https://www.inmuebles24.com/propiedades/clasificado/...-81381820.html"]` |

#### Qué Datos Obtienes
Cada resultado incluye:
- **Título y Descripción** — Texto completo del anuncio
- **Precio** — Monto, moneda, precio formateado
- **Info de Contacto** — Teléfonos (formato internacional y tipo), correos, nombre de contacto, disponibilidad de WhatsApp
- **Ubicación** — Dirección, zona, ciudad, estado, código postal, coordenadas lat/lng
- **Características** — Recámaras, baños, estacionamientos, superficie (m²), antigüedad y más
- **Anunciante** — Nombre de inmobiliaria, ID, estatus premier, calificaciones
- **Imágenes** — Todas las URLs de fotos
- **Publicación** — Fechas de inicio/fin, tipo de plan
- …¡y mucho más!

#### Palabras Clave SEO
scraper inmuebles24, detalles inmuebles24, teléfono inmuebles24, contacto inmuebles24, api bienes raíces méxico, extractor de datos de propiedades

---

#### Data Output / Ejemplo de Salida

```json
{
  "contact_info_contact_name": "Example Real Estate Group",
  "contact_info_emails": ["contact@example-realestate.com"],
  "contact_info_phone": [
    {
      "phone": "55 1234 5678",
      "valid": true,
      "international_format": "+521512345678",
      "phone_type": "PHONE"
    },
    {
      "phone": "55 1234 5678",
      "valid": true,
      "international_format": "+521512345678",
      "phone_type": "WHATSAPP"
    }
  ],
  "description": "Hermoso departamento con vista panorámica, acabados de lujo y amenidades premium...",
  "favorite": false,
  "features_acabados_de_lujo": true,
  "features_almacenaje": true,
  "features_ascensores": "4",
  "features_baños_comunes": true,
  "features_biblioteca": true,
  "features_business_center": true,
  "features_cancha_de_baloncesto": true,
  "features_cancha_de_paddle": true,
  "features_cantidad_total_de_unidades": "120",
  "features_cine": true,
  "features_club_deportivo": true,
  "features_descripción_de_oferta": "Promoción especial: 0% enganche y hasta 18 meses sin intereses.",
  "features_entrega": "inmediata",
  "features_escuelas_cercanas": true,
  "features_estacionamiento_de_visitas": true,
  "features_etapa": "Venta",
  "features_gimnasio": true,
  "features_internetwifi": true,
  "features_jacuzzi": true,
  "features_jardín": true,
  "features_lobby": true,
  "features_piscina": true,
  "features_roof_garden": true,
  "features_sauna": true,
  "features_seguridad": true,
  "features_spa": true,
  "features_video_vigilancia": true,
  "floor_plans": [
    { "url": "https://img10.naventcdn.com/avisos/.../floor_plan_1.jpg", "title": "Type A — 161 m2" },
    { "url": "https://img10.naventcdn.com/avisos/.../floor_plan_2.jpg", "title": "Type B — 195 m2" }
  ],
  "has_whatsapp": true,
  "internal_code": "ABC-12345",
  "location_address_name": "Av. Ejemplo 123",
  "location_address_visibility": "EXACT",
  "location_location_depth": 3,
  "location_location_is_assignable": true,
  "location_location_label": "ZONA",
  "location_location_latitude": 19.4000000,
  "location_location_location_id": "V1-D-00000",
  "location_location_longitude": -99.2500000,
  "location_location_name": "Zona Ejemplo",
  "location_location_parent_depth": 2,
  "location_location_parent_is_assignable": false,
  "location_location_parent_label": "CIUDAD",
  "location_location_parent_latitude": 19.3500000,
  "location_location_parent_location_id": "V1-C-000",
  "location_location_parent_longitude": -99.3400000,
  "location_location_parent_name": "Ciudad Ejemplo",
  "location_location_parent_parent_depth": 1,
  "location_location_parent_parent_is_assignable": false,
  "location_location_parent_parent_label": "PROVINCIA",
  "location_location_parent_parent_latitude": 19.5000000,
  "location_location_parent_parent_location_id": "V1-B-00",
  "location_location_parent_parent_longitude": -99.7200000,
  "location_location_parent_parent_name": "Edo. de México",
  "location_location_parent_parent_parent_depth": 0,
  "location_location_parent_parent_parent_is_assignable": false,
  "location_location_parent_parent_parent_iso_code": "MX",
  "location_location_parent_parent_parent_label": "PAIS",
  "location_location_parent_parent_parent_latitude": 23.6345000,
  "location_location_parent_parent_parent_location_id": "V1-A-18",
  "location_location_parent_parent_parent_longitude": -102.5527000,
  "location_location_parent_parent_parent_name": "Mexico",
  "location_postal_code": "00000",
  "location_posting_geolocation_geolocation_latitude": 19.3950000,
  "location_posting_geolocation_geolocation_longitude": -99.2900000,
  "location_posting_geolocation_visibility": "EXACT",
  "operation_type": "Venta",
  "pictures": [
    { "url": "https://img10.naventcdn.com/avisos/.../photo_1.jpg", "title": "Fachada" },
    { "url": "https://img10.naventcdn.com/avisos/.../photo_2.jpg", "title": "Alberca" }
  ],
  "posting_codes_text": "Cód. del anunciante: ABC-123 | Cód. Inmuebles24: 12345678",
  "posting_id": "12345678",
  "posting_type": "DEVELOPMENT",
  "premier": false,
  "price_amount": 5500000,
  "price_currency": "MN",
  "price_formatted": "Desde MN 5,500,000",
  "publication_begin_date": "2025-01-15T00:00:00-0500",
  "publication_end_date": "2028-01-15T00:00:00-0500",
  "publication_first_date_online": "2025-01-15T00:00:00-0500",
  "publication_plan": "Super Destacado",
  "publisher_id": "100000",
  "publisher_logo": "https://img10.naventcdn.com/empresas/.../logo.jpg",
  "publisher_premier": true,
  "publisher_rating": 4.5,
  "publisher_rating_count": 12,
  "publisher_ratings": [
    { "title": "Atención", "average": 4.7 },
    { "title": "Tiempo de respuesta", "average": 4.3 },
    { "title": "Recomendación", "average": 4.5 }
  ],
  "publisher_recommend_percentage": 90,
  "publisher_type": "Inmobiliaria",
  "real_estate_type_category": "Residencial",
  "real_estate_type_name": "Departamento",
  "site": "24MX",
  "statuses": ["ONLINE"],
  "tags": ["Video"],
  "title": "Departamento de lujo en Zona Ejemplo",
  "units_bathroom_quantity_range": "3 baños",
  "units_garages_quantity_range": "2 estac.",
  "units_quantity": "5 deptos.",
  "units_rooms_quantity_range": "3 rec.",
  "units_total_area_range": "180 m2",
  "url": "https://www.inmuebles24.com/propiedades/clasificado/ejemplo-departamento-de-lujo-12345678.html",
  "videos": [
    "https://www.youtube.com/watch?v=example1",
    "https://www.youtube.com/watch?v=example2"
  ]
}
````

#### Contact 📬

**Need a custom solution? Have a feature request or just want to chat?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

# Actor input Schema

## `startUrls` (type: `array`):

List of Inmuebles24 listing URLs to scrape details for. / Lista de URLs de anuncios de Inmuebles24 para extraer detalles.

## Actor input object example

```json
{
  "startUrls": [
    "https://www.inmuebles24.com/propiedades/clasificado/veclcain-casa-en-venta-agricola-zaragoza-para-remodelar-148217039.html"
  ]
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
    "startUrls": [
        "https://www.inmuebles24.com/propiedades/clasificado/veclcain-casa-en-venta-agricola-zaragoza-para-remodelar-148217039.html"
    ]
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/inmuebles24-details-scraper-by-listings-urls").call(input);

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
run_input = { "startUrls": ["https://www.inmuebles24.com/propiedades/clasificado/veclcain-casa-en-venta-agricola-zaragoza-para-remodelar-148217039.html"] }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/inmuebles24-details-scraper-by-listings-urls").call(run_input=run_input)

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
    "https://www.inmuebles24.com/propiedades/clasificado/veclcain-casa-en-venta-agricola-zaragoza-para-remodelar-148217039.html"
  ]
}' |
apify call azzouzana/inmuebles24-details-scraper-by-listings-urls --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/inmuebles24-details-scraper-by-listings-urls",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
