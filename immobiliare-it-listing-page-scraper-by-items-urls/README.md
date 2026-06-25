# 🚀 Immobiliare.it Listing Scraper (By Listings URLs)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Immobiliare.it Listing Scraper (By Listings URLs). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/immobiliare-it-listing-page-scraper-by-items-urls?fpr=cbgdsf)

---

## Immobiliare.it Listing Scraper (By Listings URLs)

### Versione italiana

#### 🤩 Panoramica

🚀 Il nostro velocissimo scraper per le pagine di dettaglio di Immobiliare.it (tramite URL diretti degli immobili)  ti
consente di estrarre le informazioni sugli immobili ed esportarle in diversi formati (JSON, CSV, HTML ecc.) 🔥 Inserisci
gli URL diretti degli immobili e sei a posto!

👉 Ti permette di estrarre dettagli completi come titolo, descrizioni, foto, informazioni energetiche, data di
costruzione, prezzo, informazioni sull'annunciante (inclusa e-mail/numero di telefono), mezzi di trasporto vicini e
molto altro ancora.

#### 📚 Come utilizzare questo actor

1. 👉 [Registrati per un account gratuito su Apify](https://apify.com/sign-up?fpr=cbgdsf) – non è necessaria la carta di credito!
2. 🎉 Clicca sul pulsante **"Get Started"** e completa una rapida registrazione.
3. 💰 L'account gratuito include abbastanza crediti per provare questo actor.
4. ⏳ Inizia a fare scraping durante il periodo di prova gratuito – nessun impegno o pagamento anticipato richiesto.

Lo scraper ha un parametro obbligatorio `startUrls` che è un array contenente una lista di link diretti agli immobili.

#### 🆓 Limitazioni del piano gratuito

Vogliamo che tu possa vedere come funziona questo actor prima di impegnarti. Per mantenere le cose eque per tutti, il **piano gratuito** include di solito questi limiti di prova:

- **Dati di prova:** fino a **5 annunci** per run—sufficienti per verificare la qualità dei dati.
- **Limite giornaliero:** **5 run** al giorno di calendario (UTC).
- **Tra un run e l’altro:** almeno **30 minuti** prima di poterne avviare un altro.

> I limiti possono cambiare in base al carico della piattaforma, al carico del sistema e al tipo di scraping previsto.

##### Quando sei pronto a scalare

Usa il piano gratuito per capire se questo actor fa al caso tuo. I piani Apify a pagamento rimuovono tempi di attesa e limiti così puoi lavorare a pieno regime—[**passa a un piano a pagamento**](https://apify.com/pricing?fpr=cbgdsf).

#### ⚠️ È legale fare scraping su Immobiliare.it?

È legale scrapare i dati pubblicamente disponibili, come descrizioni degli immobili, prezzi, foto, trasporti nelle
vicinanze, ecc. Leggi il nostro articolo sul blog
sulla [legalità del web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) per saperne di più.

#### 🤔 Perché fare scraping su Immobiliare.it?

Immobiliare.it è uno dei siti immobiliari più popolari in Italia ed Europa. Con decine di migliaia di annunci, c'è
sicuramente qualcosa per te!

Quindi, cosa potresti fare con tutti questi dati sugli annunci immobiliari?

- Trovare immobili in vendita nelle vicinanze
- Fare un'analisi dei dati del mercato
- Creare un elenco di email di agenti immobiliari
- Raccogliere dati sugli alloggi per ricerche o esigenze personali
- Confrontare i dati raccolti con un indice di valore delle case
- Utilizzare i dati per un'analisi complessiva del mercato immobiliare

Queste sono solo alcune idee per aiutarti a riflettere su come il web scraping possa fornirti i dati di cui hai bisogno.
Le possibilità sono infinite 🚀

#### 🛠️ Parametri di ingresso:

| Campo               | Tipo     | Descrizione                                                                  | Valore predefinito / Esempio                                                                 |
|---------------------|----------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| `startUrls`          | `array` (obbligatorio)   | Gli URL diretti degli immobili che lo scraper elaborerà. | `https://www.immobiliare.it/annunci/110399387/` |

#### 🧐 Risultato

I risultati sono salvati in un dataset (o "dataset" nel gergo di Apify). Ogni elemento contiene informazioni di un
annuncio:

##### Esempio di risultato:

Un esempio di risultato potrebbe somigliare alla schermata qui sotto:

```json
{
	"advertiser": {
		"agency": {
			"id": 130313,
			"type": "constructor",
			"showOnlyAgentPhone": false,
			"phones": [
				{
					"type": "vTel1",
					"value": "0331 167 1626"
				}
			],
			"bookableVisit": {
				"isVisitBookable": false,
				"virtualVisitEnabled": false
			},
			"isPaid": true,
			"label": "Impresa Edile",
			"displayName": "Edil Tatani",
			"guaranteed": false,
			"showAgentPhone": false,
			"showLogo": true,
			"imageUrls": {
				"small": "https://pic.im-cdn.it/imagenoresize/1671968281.jpg",
				"large": "https://pic.im-cdn.it/imagenoresize/1671968289.jpg"
			},
			"agencyUrl": "https://www.immobiliare.it/imprese-edili/130313/edil-tatani-busto/",
			"showExternalLink": true,
			"timetable": [],
			"hasPriceProposal": true
		},
		"hasCallNumbers": true
	},
	"contract": "sale",
	"contractValue": "Vendita",
	"createdAt": 1743694748,
	"dataType": "real-estate",
	"hasMainProperty": true,
	"hasParent": false,
	"id": 119663118,
	"iput_url": "https://www.immobiliare.it/annunci/119663118/",
	"isAIVoiceEnabled": false,
	"isNew": false,
	"isProjectLike": true,
	"luxury": false,
	"mortgage": {
		"showWidget": true,
		"mortgageWidget": {
			"callToAction": {
				"text": "Vuoi sapere che mutuo puoi richiedere?",
				"url": "https://www.immobiliare.it/mutui/simulazione/?src=immobiliare.it",
				"label": "Scoprilo subito"
			},
			"tax": 1154,
			"rates": [
				{
					"percent": 50,
					"rates": [
						{
							"year": 10,
							"rate": 0.0295
						},
						{
							"year": 15,
							"rate": 0.03
						},
						{
							"year": 20,
							"rate": 0.03
						},
						{
							"year": 25,
							"rate": 0.031
						},
						{
							"year": 30,
							"rate": 0.031
						}
					]
				},
				{
					"percent": 70,
					"rates": [
						{
							"year": 10,
							"rate": 0.0295
						},
						{
							"year": 15,
							"rate": 0.03
						},
						{
							"year": 20,
							"rate": 0.03
						},
						{
							"year": 25,
							"rate": 0.031
						},
						{
							"year": 30,
							"rate": 0.031
						}
					]
				},
				{
					"percent": 80,
					"rates": [
						{
							"year": 10,
							"rate": 0.0295
						},
						{
							"year": 15,
							"rate": 0.0305
						},
						{
							"year": 20,
							"rate": 0.031
						},
						{
							"year": 25,
							"rate": 0.031
						},
						{
							"year": 30,
							"rate": 0.031
						}
					]
				},
				{
					"percent": 95,
					"rates": [
						{
							"year": 10,
							"rate": 0.0366
						},
						{
							"year": 15,
							"rate": 0.0388
						},
						{
							"year": 20,
							"rate": 0.0397
						},
						{
							"year": 25,
							"rate": 0.0416
						},
						{
							"year": 30,
							"rate": 0.0416
						}
					]
				},
				{
					"percent": 100,
					"rates": [
						{
							"year": 10,
							"rate": 0.0463
						},
						{
							"year": 15,
							"rate": 0.0465
						},
						{
							"year": 20,
							"rate": 0.0469
						},
						{
							"year": 25,
							"rate": 0.0476
						},
						{
							"year": 30,
							"rate": 0.0476
						}
					]
				}
			],
			"value": 270200,
			"price": 386000
		},
		"mortgageBanner": [
			{
				"type": "link",
				"url": "https://www.immobiliare.it/mutui/simulazione/?src=immobiliare.it"
			},
			{
				"type": "preApproveLink",
				"url": "/mutui/pre-approvazione-online/?src=immobiliare.it"
			}
		]
	},
	"price": {
		"visible": true,
		"value": 386000,
		"formattedValue": "€ 386.000 - € 450.000",
		"minValue": "€ 386.000",
		"maxValue": "€ 450.000"
	},
	"properties": [
		{
			"showSurfaceConstitution": false,
			"adLinks": [],
			"primaryFeatures": [
				{
					"id": 8,
					"name": "Esposizione interna",
					"value": 0,
					"isVisible": false,
					"codeName": ""
				},
				{
					"id": 9,
					"name": "Esposizione esterna",
					"value": 0,
					"isVisible": false,
					"codeName": ""
				},
				{
					"id": 17,
					"name": "Accesso per disabili",
					"value": 1,
					"isVisible": true,
					"codeName": ""
				},
				{
					"id": 29,
					"name": "Parcheggio bici",
					"value": 0,
					"isVisible": false,
					"codeName": ""
				},
				{
					"id": null,
					"name": "Nessun giardino",
					"value": null,
					"isVisible": false,
					"codeName": "no-garden"
				},
				{
					"id": null,
					"name": "Infissi esterni in triplo vetro / PVC",
					"value": null,
					"isVisible": true,
					"codeName": "window-frames-in-triple-glass-pvc"
				}
			],
			"isMain": true,
			"ga4features": [
				"accesso per disabili",
				"infissi esterni in triplo vetro / pvc"
			],
			"id": "119663118",
			"cadastrals": [],
			"caption": "Residenza Le Due Magnolie – Eleganza Contemporanea ",
			"category": {
				"id": 27,
				"name": "Nuove costruzioni"
			},
			"costs": {
				"appliedVat": null,
				"agencyCommission": null,
				"commissionSubject": null,
				"notaryCommission": null
			},
			"description": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nNel pieno centro di Busto Arsizio, in via Gaudenzio Ferrari a soli 100 metri dal Municipio, sorge Residenza Le Due Magnolie: un raffinato edificio di nuova costruzione composto da sole 12 unità abitative, progettate per offrire il massimo comfort in un contesto moderno, efficiente e riservato. L’architettura della palazzina si distingue per linee pulite ed eleganti, perfettamente integrate nel tessuto urbano, mentre gli spazi interni sono studiati per garantire funzionalità, luminosità e benessere abitativo.\n\nOgni appartamento è unico e caratterizzato da ambienti ampi e ben distribuiti, con finiture di pregio personalizzabili e spazi esterni privati, come terrazzi o giardini, ideali per godersi momenti di relax all’aperto. \n\nL’intero edificio è in classe energetica A3 e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, pompe di calore, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata. La qualità costruttiva si traduce in efficienza, risparmio e comfort quotidiano.\n\nCompletano la proposta box auto doppi e cantine private, collegati direttamente ai piani tramite ascensore. La posizione è strategica: centrale, servita, comoda per la stazione e perfetta per chi desidera vivere in pieno centro città senza rinunciare alla tranquillità.\n\nResidenza Le Due Magnolie è la scelta ideale per chi cerca una casa elegante, tecnologica e a misura di vita.",
			"defaultDescription": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nNel pieno centro di Busto Arsizio, in via Gaudenzio Ferrari a soli 100 metri dal Municipio, sorge Residenza Le Due Magnolie: un raffinato edificio di nuova costruzione composto da sole 12 unità abitative, progettate per offrire il massimo comfort in un contesto moderno, efficiente e riservato. L’architettura della palazzina si distingue per linee pulite ed eleganti, perfettamente integrate nel tessuto urbano, mentre gli spazi interni sono studiati per garantire funzionalità, luminosità e benessere abitativo.\n\nOgni appartamento è unico e caratterizzato da ambienti ampi e ben distribuiti, con finiture di pregio personalizzabili e spazi esterni privati, come terrazzi o giardini, ideali per godersi momenti di relax all’aperto. \n\nL’intero edificio è in classe energetica A3 e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, pompe di calore, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata. La qualità costruttiva si traduce in efficienza, risparmio e comfort quotidiano.\n\nCompletano la proposta box auto doppi e cantine private, collegati direttamente ai piani tramite ascensore. La posizione è strategica: centrale, servita, comoda per la stazione e perfetta per chi desidera vivere in pieno centro città senza rinunciare alla tranquillità.\n\nResidenza Le Due Magnolie è la scelta ideale per chi cerca una casa elegante, tecnologica e a misura di vita.",
			"energy": {
				"zeroEnergyBuilding": true,
				"thermalInsulation": null,
				"emission": null,
				"heatingType": "centralizzato, a pavimento, alimentato a pompa di calore",
				"airConditioning": "autonomo, freddo/caldo",
				"class": {
					"name": "A3",
					"color": "#5c8501"
				},
				"epi": "≥ 3,51",
				"epiUm": "m²",
				"renewableEpi": "≥ 3,51",
				"renewableEpiUm": "m²",
				"buildingPerformance": {
					"winter": "high",
					"summer": "high"
				}
			},
			"ga4Heating": "Centralizzato",
			"features": [
				"Infissi esterni in triplo vetro / PVC"
			],
			"floors": "3 piani",
			"garage": "12 in box privato/box in garage",
			"income": false,
			"location": {
				"latitude": 45.6151,
				"longitude": 8.8545,
				"zoom": 15,
				"nation": {
					"id": "IT",
					"name": "Italia",
					"keyurl": "Italia"
				},
				"region": "Lombardia",
				"province": "Varese",
				"provinceId": "VA",
				"city": "Busto Arsizio",
				"cityId": 8487,
				"macrozone": "Centro",
				"macrozoneId": 10738,
				"microzone": "Piazza Santa Maria",
				"locality": null,
				"address": "Via Gaudenzio Ferrari, 5",
				"streetNumber": null,
				"marker": "marker"
			},
			"multimedia": {
				"photos": [
					{
						"id": 1679617014,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679617014/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679617014/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679617014/cover-m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679617014/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1679617036,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679617036/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679617036/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679617036/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679617036/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1679615630,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679615630/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679615630/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679615630/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679615630/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1679614886,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679614886/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679614886/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679614886/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679614886/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1679614664,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679614664/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679614664/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679614664/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679614664/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1679615738,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679615738/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679615738/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679615738/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679615738/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1680224688,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680224688/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680224688/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680224688/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680224688/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1680223906,
						"caption": "Giardino",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680223906/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680223906/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680223906/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680223906/xxl.jpg"
						},
						"tag": {
							"label": "Giardino",
							"key": "ext_garden",
							"category": "other"
						}
					},
					{
						"id": 1679618050,
						"caption": "Ascensori",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679618050/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679618050/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679618050/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679618050/xxl.jpg"
						},
						"tag": {
							"label": "Ascensori",
							"key": "ext_elevators",
							"category": "other"
						}
					},
					{
						"id": 1679618066,
						"caption": "Scala",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679618066/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679618066/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679618066/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679618066/xxl.jpg"
						},
						"tag": {
							"label": "Scala",
							"key": "other_staircase",
							"category": "other"
						}
					}
				],
				"videos": [],
				"floorplans": [],
				"photoPlan": [],
				"virtualTours": [],
				"documents": [
					{
						"id": 19090856,
						"type": "capitolato",
						"format": "pdf",
						"length": 5834037,
						"title": "Scarica capitolato",
						"url": "https://pic.im-cdn.it/file/19090856"
					}
				],
				"hasMultimedia": true,
				"hasOnlyPhotos": true
			},
			"photo": {
				"id": 1679617014,
				"caption": "Facciata",
				"urls": {
					"thumb": "https://pwm.im-cdn.it/image/1679617014/thumb.jpg",
					"small": "https://pwm.im-cdn.it/image/1679617014/xxs-c.jpg",
					"medium": "https://pwm.im-cdn.it/image/1679617014/cover-m-c.jpg",
					"large": "https://pwm.im-cdn.it/image/1679617014/xxl.jpg"
				}
			},
			"price": {
				"visible": true,
				"value": 386000,
				"formattedValue": "€ 386.000 - € 450.000",
				"minValue": "€ 386.000",
				"maxValue": "€ 450.000"
			},
			"lastUpdate": "Annuncio aggiornato il 29/07/2025",
			"rent": {
				"deposit": null,
				"priceReferenceIndex": null,
				"redemptionRent": null,
				"availableToStudents": false
			},
			"surface": "128 m²",
			"typology": {
				"id": 112,
				"name": "Progetto"
			},
			"typologyV2": {
				"id": 276,
				"name": "Progetto"
			},
			"typologyValue": "Progetto",
			"ga4Garage": "12 in box privato/box in garage",
			"typologyGA4Translation": "Progetto",
			"unitsValue": "12 abitative",
			"residentialUnits": 12,
			"commercialUnits": null,
			"workDates": "01/01/2021 - 01/07/2024",
			"workProgress": "Lavori completati nel luglio del 2024.",
			"land": null,
			"typologyAmount": 6,
			"mainFeatures": [
				{
					"type": "rooms",
					"label": "3 - 4 locali",
					"compactLabel": "3 - 4"
				},
				{
					"type": "surface",
					"label": "da 128 m²"
				},
				{
					"type": "typologyAmount",
					"label": "6 tipologie",
					"compactLabel": "6"
				}
			],
			"rooms": "3 - 4"
		},
		{
			"showSurfaceConstitution": false,
			"adLinks": [],
			"primaryFeatures": [
				{
					"id": 17,
					"name": "Accesso per disabili",
					"value": 1,
					"isVisible": true,
					"codeName": ""
				},
				{
					"id": null,
					"name": "balcone",
					"value": 1,
					"isVisible": true,
					"codeName": "balcony"
				},
				{
					"id": null,
					"name": "terrazza",
					"value": 1,
					"isVisible": true,
					"codeName": "terrace"
				},
				{
					"id": null,
					"name": "Nessun giardino",
					"value": null,
					"isVisible": false,
					"codeName": "no-garden"
				},
				{
					"id": null,
					"name": "Infissi esterni in triplo vetro / PVC",
					"value": null,
					"isVisible": true,
					"codeName": "window-frames-in-triple-glass-pvc"
				}
			],
			"isMain": false,
			"ga4features": [
				"accesso per disabili",
				"balcone",
				"terrazzo",
				"infissi esterni in triplo vetro / pvc"
			],
			"id": "18601630",
			"elevator": true,
			"bathrooms": "2",
			"cadastrals": [],
			"caption": "Trilocale - Primo Piano",
			"category": {
				"id": 1,
				"name": "Residenziale"
			},
			"description": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nElegante trilocale con superficie commerciale di 128 m² situato al primo piano, progettato per offrire comfort, razionalità degli spazi e luminosità naturale. L’ampia zona giorno open space, con cucina a vista e angolo relax, si apre su un ampio e luminoso terrazzo ideale per pranzi all’aperto o momenti di relax.\n\nLa zona notte è ben separata e offre due camere da letto, di cui una padronale con bagno privato dedicato ed un ampio balcone. Un altro bagno finestrato serve la zona giorno e la seconda camera. Gli ambienti sono ben distribuiti e valorizzati da finiture di pregio personalizzabili, pensati per accogliere sia la vita quotidiana che i momenti speciali.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata. \n\nUn appartamento ideale per chi cerca un’abitazione raffinata e funzionale in un contesto residenziale esclusivo nel cuore della città.\nContattaci e vieni a scoprirlo dal vivo.",
			"defaultDescription": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nElegante trilocale con superficie commerciale di 128 m² situato al primo piano, progettato per offrire comfort, razionalità degli spazi e luminosità naturale. L’ampia zona giorno open space, con cucina a vista e angolo relax, si apre su un ampio e luminoso terrazzo ideale per pranzi all’aperto o momenti di relax.\n\nLa zona notte è ben separata e offre due camere da letto, di cui una padronale con bagno privato dedicato ed un ampio balcone. Un altro bagno finestrato serve la zona giorno e la seconda camera. Gli ambienti sono ben distribuiti e valorizzati da finiture di pregio personalizzabili, pensati per accogliere sia la vita quotidiana che i momenti speciali.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata. \n\nUn appartamento ideale per chi cerca un’abitazione raffinata e funzionale in un contesto residenziale esclusivo nel cuore della città.\nContattaci e vieni a scoprirlo dal vivo.",
			"energy": {
				"zeroEnergyBuilding": true,
				"thermalInsulation": null,
				"emission": null,
				"class": {
					"name": "A3",
					"color": "#5c8501"
				},
				"epi": "≥ 3,51",
				"epiUm": "m²",
				"renewableEpi": "≥ 3,51",
				"renewableEpiUm": "m²",
				"buildingPerformance": {
					"winter": "high",
					"summer": "high"
				}
			},
			"ga4Heating": "Assente",
			"features": [
				"Infissi esterni in triplo vetro / PVC"
			],
			"floor": {
				"abbreviation": "1",
				"value": "1° piano, con ascensore",
				"floorOnlyValue": "1 piano",
				"ga4FloorValue": "1 piano"
			},
			"floors": "3 piani",
			"income": false,
			"location": {
				"latitude": 45.61510086,
				"longitude": 8.85449982,
				"zoom": 15,
				"nation": {
					"id": "IT",
					"name": "Italia",
					"keyurl": "Italia"
				},
				"region": "Lombardia",
				"province": "Varese",
				"provinceId": "VA",
				"city": "Busto Arsizio",
				"cityId": 8487,
				"macrozone": "Centro",
				"macrozoneId": 10738,
				"microzone": "Piazza Santa Maria",
				"locality": null,
				"address": "Via Gaudenzio Ferrari, 5",
				"streetNumber": null,
				"marker": "marker"
			},
			"multimedia": {
				"photos": [
					{
						"id": 1702711790,
						"caption": "Planimetria",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1702711790/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1702711790/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1702711790/cover-m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1702711790/xxl.jpg"
						},
						"tag": {
							"label": "Planimetria",
							"key": "other_planimetry",
							"category": "other"
						}
					},
					{
						"id": 1680392676,
						"caption": "Terrazzo",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680392676/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680392676/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680392676/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680392676/xxl.jpg"
						},
						"tag": {
							"label": "Terrazzo",
							"key": "ext_terrace",
							"category": "other"
						}
					},
					{
						"id": 1680392812,
						"caption": "Soggiorno",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680392812/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680392812/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680392812/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680392812/xxl.jpg"
						},
						"tag": {
							"label": "Soggiorno",
							"key": "int_sitting_room",
							"category": "other"
						}
					},
					{
						"id": 1680392916,
						"caption": "Soggiorno",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680392916/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680392916/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680392916/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680392916/xxl.jpg"
						},
						"tag": {
							"label": "Soggiorno",
							"key": "int_sitting_room",
							"category": "other"
						}
					}
				],
				"videos": [],
				"floorplans": [
					{
						"id": 113085878,
						"caption": "",
						"urls": {
							"thumb": "https://pic.im-cdn.it/plan/113085878/thumb.jpg",
							"small": "https://pic.im-cdn.it/plan/113085878/xxs-c.jpg",
							"medium": "https://pic.im-cdn.it/plan/113085878/m.jpg",
							"large": "https://pic.im-cdn.it/plan/113085878/xxl.jpg"
						},
						"url": null,
						"interactive": false
					}
				],
				"photoPlan": [],
				"virtualTours": [],
				"documents": [],
				"hasMultimedia": true,
				"hasOnlyPhotos": false
			},
			"photo": {
				"id": 1702711790,
				"caption": "Planimetria",
				"urls": {
					"thumb": "https://pwm.im-cdn.it/image/1702711790/thumb.jpg",
					"small": "https://pwm.im-cdn.it/image/1702711790/xxs-c.jpg",
					"medium": "https://pwm.im-cdn.it/image/1702711790/cover-m-c.jpg",
					"large": "https://pwm.im-cdn.it/image/1702711790/xxl.jpg"
				}
			},
			"price": {
				"visible": true,
				"value": 386000,
				"formattedValue": "€ 386.000",
				"minValue": "€ 386.000",
				"priceRange": "300.001 - 500.000 &euro;",
				"pricePerSquareMeter": "3.016 €/m²"
			},
			"lastUpdate": "Annuncio aggiornato il 29/07/2025",
			"rooms": "3",
			"roomsValue": "3 locali, 2 bagni",
			"surface": "128 m²",
			"typology": {
				"id": 4,
				"name": "Appartamento"
			},
			"typologyV2": {
				"id": 14,
				"name": "Appartamento"
			},
			"typologyValue": "Appartamento",
			"typologyGA4Translation": "Appartamento",
			"residentialUnits": null,
			"commercialUnits": null,
			"land": null,
			"mainFeatures": [
				{
					"type": "rooms",
					"label": "3 locali",
					"compactLabel": "3"
				},
				{
					"type": "surface",
					"label": "128 m²"
				},
				{
					"type": "bathrooms",
					"label": "2 bagni",
					"compactLabel": "2"
				},
				{
					"type": "floor",
					"label": "Piano 1",
					"compactLabel": "1"
				},
				{
					"type": "elevator",
					"label": "Ascensore",
					"compactLabel": "Sì"
				}
			]
		},
		{
			"showSurfaceConstitution": false,
			"adLinks": [],
			"primaryFeatures": [
				{
					"id": 17,
					"name": "Accesso per disabili",
					"value": 1,
					"isVisible": true,
					"codeName": ""
				},
				{
					"id": null,
					"name": "balcone",
					"value": 1,
					"isVisible": true,
					"codeName": "balcony"
				},
				{
					"id": null,
					"name": "terrazza",
					"value": 1,
					"isVisible": true,
					"codeName": "terrace"
				},
				{
					"id": null,
					"name": "Giardino privato",
					"value": null,
					"isVisible": true,
					"codeName": "private-garden"
				},
				{
					"id": null,
					"name": "Infissi esterni in triplo vetro / PVC",
					"value": null,
					"isVisible": true,
					"codeName": "window-frames-in-triple-glass-pvc"
				}
			],
			"isMain": false,
			"ga4features": [
				"accesso per disabili",
				"balcone",
				"terrazzo",
				"giardino privato",
				"infissi esterni in triplo vetro / pvc"
			],
			"id": "19559316",
			"elevator": true,
			"bathrooms": "2",
			"cadastrals": [],
			"caption": "TRILOCALE CON GIARDINO PRIVATO - PIANO TERRA",
			"category": {
				"id": 1,
				"name": "Residenziale"
			},
			"description": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nAmpio trilocale al piano terra con superficie commerciale di 147 m² con spazi ben distribuiti e grande luminosità. L’ampia zona giorno open space si affaccia sul terrazzo e sull'elegante giardino privato, perfetto per vivere l’esterno in ogni stagione. La zona notte è composta da tre camere da letto e doppi servizi.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata.\n\nIdeale per famiglie o per chi cerca il comfort di una casa indipendente con tutte le comodità di un contesto residenziale esclusivo.\nContattaci e vieni a scoprirlo dal vivo.",
			"defaultDescription": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nAmpio trilocale al piano terra con superficie commerciale di 147 m² con spazi ben distribuiti e grande luminosità. L’ampia zona giorno open space si affaccia sul terrazzo e sull'elegante giardino privato, perfetto per vivere l’esterno in ogni stagione. La zona notte è composta da tre camere da letto e doppi servizi.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata.\n\nIdeale per famiglie o per chi cerca il comfort di una casa indipendente con tutte le comodità di un contesto residenziale esclusivo.\nContattaci e vieni a scoprirlo dal vivo.",
			"energy": {
				"zeroEnergyBuilding": true,
				"thermalInsulation": null,
				"emission": null,
				"class": {
					"name": "A3",
					"color": "#5c8501"
				},
				"epi": "≥ 3,51",
				"epiUm": "m²",
				"renewableEpi": "≥ 3,51",
				"renewableEpiUm": "m²",
				"buildingPerformance": {
					"winter": "high",
					"summer": "high"
				}
			},
			"ga4Heating": "Assente",
			"features": [
				"Infissi esterni in triplo vetro / PVC"
			],
			"floor": {
				"abbreviation": "T",
				"value": "Piano terra, con ascensore",
				"floorOnlyValue": "piano terra",
				"ga4FloorValue": "piano terra"
			},
			"floors": "3 piani",
			"income": false,
			"location": {
				"latitude": 45.61510086,
				"longitude": 8.85449982,
				"zoom": 15,
				"nation": {
					"id": "IT",
					"name": "Italia",
					"keyurl": "Italia"
				},
				"region": "Lombardia",
				"province": "Varese",
				"provinceId": "VA",
				"city": "Busto Arsizio",
				"cityId": 8487,
				"macrozone": "Centro",
				"macrozoneId": 10738,
				"microzone": "Piazza Santa Maria",
				"locality": null,
				"address": "Via Gaudenzio Ferrari, 5",
				"streetNumber": null,
				"marker": "marker"
			},
			"multimedia": {
				"photos": [
					{
						"id": 1760581306,
						"caption": "Planimetria",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1760581306/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1760581306/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1760581306/cover-m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1760581306/xxl.jpg"
						},
						"tag": {
							"label": "Planimetria",
							"key": "other_planimetry",
							"category": "other"
						}
					}
				],
				"videos": [],
				"floorplans": [
					{
						"id": 116052444,
						"caption": "",
						"urls": {
							"thumb": "https://pic.im-cdn.it/plan/116052444/thumb.jpg",
							"small": "https://pic.im-cdn.it/plan/116052444/xxs-c.jpg",
							"medium": "https://pic.im-cdn.it/plan/116052444/m.jpg",
							"large": "https://pic.im-cdn.it/plan/116052444/xxl.jpg"
						},
						"url": null,
						"interactive": false
					}
				],
				"photoPlan": [],
				"virtualTours": [],
				"documents": [],
				"hasMultimedia": true,
				"hasOnlyPhotos": false
			},
			"photo": {
				"id": 1760581306,
				"caption": "Planimetria",
				"urls": {
					"thumb": "https://pwm.im-cdn.it/image/1760581306/thumb.jpg",
					"small": "https://pwm.im-cdn.it/image/1760581306/xxs-c.jpg",
					"medium": "https://pwm.im-cdn.it/image/1760581306/cover-m-c.jpg",
					"large": "https://pwm.im-cdn.it/image/1760581306/xxl.jpg"
				}
			},
			"price": {
				"visible": true,
				"value": 399000,
				"formattedValue": "€ 399.000",
				"minValue": "€ 399.000",
				"priceRange": "300.001 - 500.000 &euro;",
				"pricePerSquareMeter": "2.714 €/m²"
			},
			"lastUpdate": "Annuncio aggiornato il 29/07/2025",
			"rooms": "3",
			"roomsValue": "3 locali, 2 bagni",
			"surface": "147 m²",
			"typology": {
				"id": 4,
				"name": "Appartamento"
			},
			"typologyV2": {
				"id": 14,
				"name": "Appartamento"
			},
			"typologyValue": "Appartamento",
			"typologyGA4Translation": "Appartamento",
			"residentialUnits": null,
			"commercialUnits": null,
			"land": null,
			"mainFeatures": [
				{
					"type": "rooms",
					"label": "3 locali",
					"compactLabel": "3"
				},
				{
					"type": "surface",
					"label": "147 m²"
				},
				{
					"type": "bathrooms",
					"label": "2 bagni",
					"compactLabel": "2"
				},
				{
					"type": "floor",
					"label": "Piano T",
					"compactLabel": "T"
				},
				{
					"type": "elevator",
					"label": "Ascensore",
					"compactLabel": "Sì"
				}
			]
		},
		{
			"showSurfaceConstitution": false,
			"adLinks": [],
			"primaryFeatures": [
				{
					"id": 17,
					"name": "Accesso per disabili",
					"value": 1,
					"isVisible": true,
					"codeName": ""
				},
				{
					"id": null,
					"name": "balcone",
					"value": 1,
					"isVisible": true,
					"codeName": "balcony"
				},
				{
					"id": null,
					"name": "terrazza",
					"value": 1,
					"isVisible": true,
					"codeName": "terrace"
				},
				{
					"id": null,
					"name": "Nessun giardino",
					"value": null,
					"isVisible": false,
					"codeName": "no-garden"
				},
				{
					"id": null,
					"name": "Infissi esterni in triplo vetro / PVC",
					"value": null,
					"isVisible": true,
					"codeName": "window-frames-in-triple-glass-pvc"
				}
			],
			"isMain": false,
			"ga4features": [
				"accesso per disabili",
				"balcone",
				"terrazzo",
				"infissi esterni in triplo vetro / pvc"
			],
			"id": "18601874",
			"elevator": true,
			"bathrooms": "2",
			"cadastrals": [],
			"caption": "TRILOCALE - PRIMO PIANO",
			"category": {
				"id": 1,
				"name": "Residenziale"
			},
			"description": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nElegante trilocale dalla superfice commerciale di 130 m² situato al primo piano, progettato per offrire comfort, razionalità degli spazi e luminosità naturale. L’ampia zona giorno open space, con cucina a vista e angolo relax, si apre su un ampio e luminoso terrazzo, ideale per pranzi all’aperto o momenti di relax.\n\nLa zona notte è ben separata e offre due camere da letto, di cui una padronale con bagno privato dedicato e accesso unico ad ampio terrazzo. Un altro bagno, anch'esso finestrato, serve la zona giorno e la seconda camera. Gli ambienti sono ben distribuiti e valorizzati da finiture di pregio personalizzabili, pensati per accogliere sia la vita quotidiana che i momenti speciali.\n\nClasse energetica A2, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione con deumidificazione meccanica controllata.\n\nUn appartamento ideale per chi cerca un’abitazione raffinata e funzionale in un contesto residenziale esclusivo nel cuore della città.\nContattaci e vieni a scoprirlo dal vivo.",
			"defaultDescription": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nElegante trilocale dalla superfice commerciale di 130 m² situato al primo piano, progettato per offrire comfort, razionalità degli spazi e luminosità naturale. L’ampia zona giorno open space, con cucina a vista e angolo relax, si apre su un ampio e luminoso terrazzo, ideale per pranzi all’aperto o momenti di relax.\n\nLa zona notte è ben separata e offre due camere da letto, di cui una padronale con bagno privato dedicato e accesso unico ad ampio terrazzo. Un altro bagno, anch'esso finestrato, serve la zona giorno e la seconda camera. Gli ambienti sono ben distribuiti e valorizzati da finiture di pregio personalizzabili, pensati per accogliere sia la vita quotidiana che i momenti speciali.\n\nClasse energetica A2, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione con deumidificazione meccanica controllata.\n\nUn appartamento ideale per chi cerca un’abitazione raffinata e funzionale in un contesto residenziale esclusivo nel cuore della città.\nContattaci e vieni a scoprirlo dal vivo.",
			"energy": {
				"zeroEnergyBuilding": true,
				"thermalInsulation": null,
				"emission": null,
				"class": {
					"name": "A3",
					"color": "#5c8501"
				},
				"epi": "≥ 3,51",
				"epiUm": "m²",
				"renewableEpi": "≥ 3,51",
				"renewableEpiUm": "m²",
				"buildingPerformance": {
					"winter": "high",
					"summer": "high"
				}
			},
			"ga4Heating": "Assente",
			"features": [
				"Infissi esterni in triplo vetro / PVC"
			],
			"floor": {
				"abbreviation": "1",
				"value": "1° piano, con ascensore",
				"floorOnlyValue": "1 piano",
				"ga4FloorValue": "1 piano"
			},
			"floors": "3 piani",
			"income": false,
			"location": {
				"latitude": 45.61510086,
				"longitude": 8.85449982,
				"zoom": 15,
				"nation": {
					"id": "IT",
					"name": "Italia",
					"keyurl": "Italia"
				},
				"region": "Lombardia",
				"province": "Varese",
				"provinceId": "VA",
				"city": "Busto Arsizio",
				"cityId": 8487,
				"macrozone": "Centro",
				"macrozoneId": 10738,
				"microzone": "Piazza Santa Maria",
				"locality": null,
				"address": "Via Gaudenzio Ferrari, 5",
				"streetNumber": null,
				"marker": "marker"
			},
			"multimedia": {
				"photos": [
					{
						"id": 1702710340,
						"caption": "Planimetria",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1702710340/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1702710340/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1702710340/cover-m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1702710340/xxl.jpg"
						},
						"tag": {
							"label": "Planimetria",
							"key": "other_planimetry",
							"category": "other"
						}
					},
					{
						"id": 1760528904,
						"caption": "Salone",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1760528904/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1760528904/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1760528904/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1760528904/xxl.jpg"
						},
						"tag": {
							"label": "Salone",
							"key": "int_livingroom",
							"category": "livingRoom"
						}
					},
					{
						"id": 1760528880,
						"caption": "Camera da letto",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1760528880/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1760528880/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1760528880/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1760528880/xxl.jpg"
						},
						"tag": {
							"label": "Camera da letto",
							"key": "int_bedroom",
							"category": "bedroom"
						}
					},
					{
						"id": 1680412782,
						"caption": "Soggiorno",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680412782/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680412782/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680412782/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680412782/xxl.jpg"
						},
						"tag": {
							"label": "Soggiorno",
							"key": "int_sitting_room",
							"category": "other"
						}
					},
					{
						"id": 1680412874,
						"caption": "Terrazzo",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680412874/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680412874/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680412874/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680412874/xxl.jpg"
						},
						"tag": {
							"label": "Terrazzo",
							"key": "ext_terrace",
							"category": "other"
						}
					}
				],
				"videos": [],
				"floorplans": [
					{
						"id": 113086814,
						"caption": "",
						"urls": {
							"thumb": "https://pic.im-cdn.it/plan/113086814/thumb.jpg",
							"small": "https://pic.im-cdn.it/plan/113086814/xxs-c.jpg",
							"medium": "https://pic.im-cdn.it/plan/113086814/m.jpg",
							"large": "https://pic.im-cdn.it/plan/113086814/xxl.jpg"
						},
						"url": null,
						"interactive": false
					}
				],
				"photoPlan": [],
				"virtualTours": [],
				"documents": [],
				"hasMultimedia": true,
				"hasOnlyPhotos": false
			},
			"photo": {
				"id": 1702710340,
				"caption": "Planimetria",
				"urls": {
					"thumb": "https://pwm.im-cdn.it/image/1702710340/thumb.jpg",
					"small": "https://pwm.im-cdn.it/image/1702710340/xxs-c.jpg",
					"medium": "https://pwm.im-cdn.it/image/1702710340/cover-m-c.jpg",
					"large": "https://pwm.im-cdn.it/image/1702710340/xxl.jpg"
				}
			},
			"price": {
				"visible": true,
				"value": 399000,
				"formattedValue": "€ 399.000",
				"minValue": "€ 399.000",
				"priceRange": "300.001 - 500.000 &euro;",
				"pricePerSquareMeter": "3.069 €/m²"
			},
			"lastUpdate": "Annuncio aggiornato il 29/07/2025",
			"rooms": "3",
			"roomsValue": "3 locali, 2 bagni",
			"surface": "130 m²",
			"typology": {
				"id": 4,
				"name": "Appartamento"
			},
			"typologyV2": {
				"id": 14,
				"name": "Appartamento"
			},
			"typologyValue": "Appartamento",
			"typologyGA4Translation": "Appartamento",
			"residentialUnits": null,
			"commercialUnits": null,
			"land": null,
			"mainFeatures": [
				{
					"type": "rooms",
					"label": "3 locali",
					"compactLabel": "3"
				},
				{
					"type": "surface",
					"label": "130 m²"
				},
				{
					"type": "bathrooms",
					"label": "2 bagni",
					"compactLabel": "2"
				},
				{
					"type": "floor",
					"label": "Piano 1",
					"compactLabel": "1"
				},
				{
					"type": "elevator",
					"label": "Ascensore",
					"compactLabel": "Sì"
				}
			]
		},
		{
			"showSurfaceConstitution": false,
			"adLinks": [],
			"primaryFeatures": [
				{
					"id": 17,
					"name": "Accesso per disabili",
					"value": 1,
					"isVisible": true,
					"codeName": ""
				},
				{
					"id": null,
					"name": "balcone",
					"value": 1,
					"isVisible": true,
					"codeName": "balcony"
				},
				{
					"id": null,
					"name": "terrazza",
					"value": 1,
					"isVisible": true,
					"codeName": "terrace"
				},
				{
					"id": null,
					"name": "Giardino privato",
					"value": null,
					"isVisible": true,
					"codeName": "private-garden"
				},
				{
					"id": null,
					"name": "Infissi esterni in triplo vetro / PVC",
					"value": null,
					"isVisible": true,
					"codeName": "window-frames-in-triple-glass-pvc"
				}
			],
			"isMain": false,
			"ga4features": [
				"accesso per disabili",
				"balcone",
				"terrazzo",
				"giardino privato",
				"infissi esterni in triplo vetro / pvc"
			],
			"id": "18591790",
			"elevator": true,
			"bathrooms": "2",
			"cadastrals": [],
			"caption": "Quadrilocale con giardino privato - Piano Terra",
			"category": {
				"id": 1,
				"name": "Residenziale"
			},
			"description": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nAmpio quadrilocale al piano terra con superficie commerciale di 147 m² con spazi ben distribuiti e grande luminosità. L’ampia zona giorno open space si affaccia sul terrazzo e sull'elegante giardino privato, perfetto per vivere l’esterno in ogni stagione. La zona giorno viene completata da un luminoso studio ideale per lo smart working. La zona notte è composta da due camere da letto e doppi servizi.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata.\n\nIdeale per famiglie o per chi cerca il comfort di una casa indipendente con tutte le comodità di un contesto residenziale esclusivo.\nContattaci e vieni a scoprirlo dal vivo.",
			"defaultDescription": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nAmpio quadrilocale al piano terra con superficie commerciale di 147 m² con spazi ben distribuiti e grande luminosità. L’ampia zona giorno open space si affaccia sul terrazzo e sull'elegante giardino privato, perfetto per vivere l’esterno in ogni stagione. La zona giorno viene completata da un luminoso studio ideale per lo smart working. La zona notte è composta da due camere da letto e doppi servizi.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata.\n\nIdeale per famiglie o per chi cerca il comfort di una casa indipendente con tutte le comodità di un contesto residenziale esclusivo.\nContattaci e vieni a scoprirlo dal vivo.",
			"energy": {
				"zeroEnergyBuilding": true,
				"thermalInsulation": null,
				"emission": null,
				"class": {
					"name": "A3",
					"color": "#5c8501"
				},
				"epi": "≥ 3,51",
				"epiUm": "m²",
				"renewableEpi": "≥ 3,51",
				"renewableEpiUm": "m²",
				"buildingPerformance": {
					"winter": "high",
					"summer": "high"
				}
			},
			"ga4Heating": "Assente",
			"features": [
				"Infissi esterni in triplo vetro / PVC"
			],
			"floor": {
				"abbreviation": "T",
				"value": "Piano terra, con ascensore",
				"floorOnlyValue": "piano terra",
				"ga4FloorValue": "piano terra"
			},
			"floors": "3 piani",
			"income": false,
			"location": {
				"latitude": 45.61510086,
				"longitude": 8.85449982,
				"zoom": 15,
				"nation": {
					"id": "IT",
					"name": "Italia",
					"keyurl": "Italia"
				},
				"region": "Lombardia",
				"province": "Varese",
				"provinceId": "VA",
				"city": "Busto Arsizio",
				"cityId": 8487,
				"macrozone": "Centro",
				"macrozoneId": 10738,
				"microzone": "Piazza Santa Maria",
				"locality": null,
				"address": "Via Gaudenzio Ferrari, 5",
				"streetNumber": null,
				"marker": "marker"
			},
			"multimedia": {
				"photos": [
					{
						"id": 1760570528,
						"caption": "Planimetria",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1760570528/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1760570528/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1760570528/cover-m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1760570528/xxl.jpg"
						},
						"tag": {
							"label": "Planimetria",
							"key": "other_planimetry",
							"category": "other"
						}
					}
				],
				"videos": [],
				"floorplans": [],
				"photoPlan": [],
				"virtualTours": [],
				"documents": [],
				"hasMultimedia": true,
				"hasOnlyPhotos": true
			},
			"photo": {
				"id": 1760570528,
				"caption": "Planimetria",
				"urls": {
					"thumb": "https://pwm.im-cdn.it/image/1760570528/thumb.jpg",
					"small": "https://pwm.im-cdn.it/image/1760570528/xxs-c.jpg",
					"medium": "https://pwm.im-cdn.it/image/1760570528/cover-m-c.jpg",
					"large": "https://pwm.im-cdn.it/image/1760570528/xxl.jpg"
				}
			},
			"price": {
				"visible": true,
				"value": 399000,
				"formattedValue": "€ 399.000",
				"minValue": "€ 399.000",
				"priceRange": "300.001 - 500.000 &euro;",
				"pricePerSquareMeter": "2.714 €/m²"
			},
			"reference": {
				"label": "riferimento",
				"code": "P.T. 4"
			},
			"lastUpdate": "Annuncio aggiornato il 29/07/2025",
			"rooms": "4",
			"roomsValue": "4 locali, 2 bagni",
			"surface": "147 m²",
			"typology": {
				"id": 4,
				"name": "Appartamento"
			},
			"typologyV2": {
				"id": 14,
				"name": "Appartamento"
			},
			"typologyValue": "Appartamento",
			"typologyGA4Translation": "Appartamento",
			"residentialUnits": null,
			"commercialUnits": null,
			"land": null,
			"mainFeatures": [
				{
					"type": "rooms",
					"label": "4 locali",
					"compactLabel": "4"
				},
				{
					"type": "surface",
					"label": "147 m²"
				},
				{
					"type": "bathrooms",
					"label": "2 bagni",
					"compactLabel": "2"
				},
				{
					"type": "floor",
					"label": "Piano T",
					"compactLabel": "T"
				},
				{
					"type": "elevator",
					"label": "Ascensore",
					"compactLabel": "Sì"
				}
			]
		},
		{
			"showSurfaceConstitution": false,
			"adLinks": [],
			"primaryFeatures": [
				{
					"id": 17,
					"name": "Accesso per disabili",
					"value": 1,
					"isVisible": true,
					"codeName": ""
				},
				{
					"id": null,
					"name": "balcone",
					"value": 1,
					"isVisible": true,
					"codeName": "balcony"
				},
				{
					"id": null,
					"name": "terrazza",
					"value": 1,
					"isVisible": true,
					"codeName": "terrace"
				},
				{
					"id": null,
					"name": "Giardino privato",
					"value": null,
					"isVisible": true,
					"codeName": "private-garden"
				},
				{
					"id": null,
					"name": "Infissi esterni in triplo vetro / PVC",
					"value": null,
					"isVisible": true,
					"codeName": "window-frames-in-triple-glass-pvc"
				}
			],
			"isMain": false,
			"ga4features": [
				"accesso per disabili",
				"balcone",
				"terrazzo",
				"giardino privato",
				"infissi esterni in triplo vetro / pvc"
			],
			"id": "18601000",
			"elevator": true,
			"bathrooms": "2",
			"cadastrals": [],
			"caption": "Quadrilocale con giardino privato - Piano Terra",
			"category": {
				"id": 1,
				"name": "Residenziale"
			},
			"description": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nAmpio quadrilocale al piano terra con superficie commerciale di 147 m² con spazi ben distribuiti e grande luminosità. \nL’ampia zona giorno open space si affaccia su un terrazzo e un elegante giardino privato, perfetto per vivere l’esterno in ogni stagione. \nLa zona notte è ben separata e offre tre camere da letto, di cui una padronale con bagno privato dedicato. Un altro bagno finestrato serve le altre due camere. Gli ambienti sono ben distribuiti e valorizzati da finiture di pregio personalizzabili, pensati per accogliere sia la vita quotidiana che i momenti speciali.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico, ventilazione e deumidificazione meccanica controllata. \n\nIdeale per famiglie o per chi cerca il comfort di una casa indipendente con tutte le comodità di un contesto residenziale esclusivo.\nContattaci e vieni a scoprirlo dal vivo.",
			"defaultDescription": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nAmpio quadrilocale al piano terra con superficie commerciale di 147 m² con spazi ben distribuiti e grande luminosità. \nL’ampia zona giorno open space si affaccia su un terrazzo e un elegante giardino privato, perfetto per vivere l’esterno in ogni stagione. \nLa zona notte è ben separata e offre tre camere da letto, di cui una padronale con bagno privato dedicato. Un altro bagno finestrato serve le altre due camere. Gli ambienti sono ben distribuiti e valorizzati da finiture di pregio personalizzabili, pensati per accogliere sia la vita quotidiana che i momenti speciali.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico, ventilazione e deumidificazione meccanica controllata. \n\nIdeale per famiglie o per chi cerca il comfort di una casa indipendente con tutte le comodità di un contesto residenziale esclusivo.\nContattaci e vieni a scoprirlo dal vivo.",
			"energy": {
				"zeroEnergyBuilding": true,
				"thermalInsulation": null,
				"emission": null,
				"class": {
					"name": "A3",
					"color": "#5c8501"
				},
				"epi": "≥ 3,51",
				"epiUm": "m²",
				"renewableEpi": "≥ 3,51",
				"renewableEpiUm": "m²",
				"buildingPerformance": {
					"winter": "high",
					"summer": "high"
				}
			},
			"ga4Heating": "Assente",
			"features": [
				"Infissi esterni in triplo vetro / PVC"
			],
			"floor": {
				"abbreviation": "T",
				"value": "Piano terra, con ascensore",
				"floorOnlyValue": "piano terra",
				"ga4FloorValue": "piano terra"
			},
			"floors": "3 piani",
			"income": false,
			"location": {
				"latitude": 45.61510086,
				"longitude": 8.85449982,
				"zoom": 15,
				"nation": {
					"id": "IT",
					"name": "Italia",
					"keyurl": "Italia"
				},
				"region": "Lombardia",
				"province": "Varese",
				"provinceId": "VA",
				"city": "Busto Arsizio",
				"cityId": 8487,
				"macrozone": "Centro",
				"macrozoneId": 10738,
				"microzone": "Piazza Santa Maria",
				"locality": null,
				"address": "Via Gaudenzio Ferrari, 5",
				"streetNumber": null,
				"marker": "marker"
			},
			"multimedia": {
				"photos": [
					{
						"id": 1704232246,
						"caption": "Planimetria",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1704232246/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1704232246/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1704232246/cover-m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1704232246/xxl.jpg"
						},
						"tag": {
							"label": "Planimetria",
							"key": "other_planimetry",
							"category": "other"
						}
					},
					{
						"id": 1680399174,
						"caption": "Cortile interno",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680399174/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680399174/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680399174/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680399174/xxl.jpg"
						},
						"tag": {
							"label": "Cortile interno",
							"key": "ext_internal_courtyard",
							"category": "other"
						}
					},
					{
						"id": 1680399250,
						"caption": "Terrazzo",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680399250/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680399250/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680399250/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680399250/xxl.jpg"
						},
						"tag": {
							"label": "Terrazzo",
							"key": "ext_terrace",
							"category": "other"
						}
					},
					{
						"id": 1680399058,
						"caption": "Soggiorno",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680399058/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680399058/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680399058/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680399058/xxl.jpg"
						},
						"tag": {
							"label": "Soggiorno",
							"key": "int_sitting_room",
							"category": "other"
						}
					},
					{
						"id": 1680399294,
						"caption": "Camera da letto",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680399294/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680399294/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680399294/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680399294/xxl.jpg"
						},
						"tag": {
							"label": "Camera da letto",
							"key": "int_bedroom",
							"category": "bedroom"
						}
					}
				],
				"videos": [],
				"floorplans": [
					{
						"id": 113083374,
						"caption": "",
						"urls": {
							"thumb": "https://pic.im-cdn.it/plan/113083374/thumb.jpg",
							"small": "https://pic.im-cdn.it/plan/113083374/xxs-c.jpg",
							"medium": "https://pic.im-cdn.it/plan/113083374/m.jpg",
							"large": "https://pic.im-cdn.it/plan/113083374/xxl.jpg"
						},
						"url": null,
						"interactive": false
					}
				],
				"photoPlan": [],
				"virtualTours": [],
				"documents": [],
				"hasMultimedia": true,
				"hasOnlyPhotos": false
			},
			"photo": {
				"id": 1704232246,
				"caption": "Planimetria",
				"urls": {
					"thumb": "https://pwm.im-cdn.it/image/1704232246/thumb.jpg",
					"small": "https://pwm.im-cdn.it/image/1704232246/xxs-c.jpg",
					"medium": "https://pwm.im-cdn.it/image/1704232246/cover-m-c.jpg",
					"large": "https://pwm.im-cdn.it/image/1704232246/xxl.jpg"
				}
			},
			"price": {
				"visible": true,
				"value": 410000,
				"formattedValue": "€ 410.000",
				"minValue": "€ 410.000",
				"priceRange": "300.001 - 500.000 &euro;",
				"pricePerSquareMeter": "2.789 €/m²"
			},
			"reference": {
				"label": "riferimento",
				"code": "P.T. 3"
			},
			"lastUpdate": "Annuncio aggiornato il 29/07/2025",
			"rooms": "4",
			"roomsValue": "4 locali, 2 bagni",
			"surface": "147 m²",
			"typology": {
				"id": 4,
				"name": "Appartamento"
			},
			"typologyV2": {
				"id": 14,
				"name": "Appartamento"
			},
			"typologyValue": "Appartamento",
			"typologyGA4Translation": "Appartamento",
			"residentialUnits": null,
			"commercialUnits": null,
			"land": null,
			"mainFeatures": [
				{
					"type": "rooms",
					"label": "4 locali",
					"compactLabel": "4"
				},
				{
					"type": "surface",
					"label": "147 m²"
				},
				{
					"type": "bathrooms",
					"label": "2 bagni",
					"compactLabel": "2"
				},
				{
					"type": "floor",
					"label": "Piano T",
					"compactLabel": "T"
				},
				{
					"type": "elevator",
					"label": "Ascensore",
					"compactLabel": "Sì"
				}
			]
		},
		{
			"showSurfaceConstitution": false,
			"adLinks": [],
			"primaryFeatures": [
				{
					"id": 17,
					"name": "Accesso per disabili",
					"value": 1,
					"isVisible": true,
					"codeName": ""
				},
				{
					"id": null,
					"name": "balcone",
					"value": 1,
					"isVisible": true,
					"codeName": "balcony"
				},
				{
					"id": null,
					"name": "terrazza",
					"value": 1,
					"isVisible": true,
					"codeName": "terrace"
				},
				{
					"id": null,
					"name": "Giardino privato",
					"value": null,
					"isVisible": true,
					"codeName": "private-garden"
				},
				{
					"id": null,
					"name": "Infissi esterni in triplo vetro / PVC",
					"value": null,
					"isVisible": true,
					"codeName": "window-frames-in-triple-glass-pvc"
				}
			],
			"isMain": false,
			"ga4features": [
				"accesso per disabili",
				"balcone",
				"terrazzo",
				"giardino privato",
				"infissi esterni in triplo vetro / pvc"
			],
			"id": "18601202",
			"elevator": true,
			"bathrooms": "2",
			"cadastrals": [],
			"caption": "TRILOCALE CON GIARDINO E POSTO AUTO ESCLUSIVO - PIANO TERRA",
			"category": {
				"id": 1,
				"name": "Residenziale"
			},
			"description": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nAmpio trilocale al piano terra con superficie commerciale di 159 m² con spazi ben distribuiti e grande luminosità. L’ampia zona giorno open space si affaccia su un terrazzo e un elegante giardino privato, perfetto per vivere l’esterno in ogni stagione. La zona notte è composta da due camere da letto, doppi servizi finestrati, e un vano da poter utilizzare come lavanderia o ripostiglio. \nIncluso nel prezzo, un comodo posto auto coperto con ingresso indipendente da Via Miani: una soluzione esclusiva che unisce privacy e praticità quotidiana.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata.\n\nIdeale per famiglie o per chi cerca il comfort di una casa indipendente con tutte le comodità di un contesto residenziale esclusivo.\nContattaci e vieni a scoprirlo dal vivo.",
			"defaultDescription": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nAmpio trilocale al piano terra con superficie commerciale di 159 m² con spazi ben distribuiti e grande luminosità. L’ampia zona giorno open space si affaccia su un terrazzo e un elegante giardino privato, perfetto per vivere l’esterno in ogni stagione. La zona notte è composta da due camere da letto, doppi servizi finestrati, e un vano da poter utilizzare come lavanderia o ripostiglio. \nIncluso nel prezzo, un comodo posto auto coperto con ingresso indipendente da Via Miani: una soluzione esclusiva che unisce privacy e praticità quotidiana.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata.\n\nIdeale per famiglie o per chi cerca il comfort di una casa indipendente con tutte le comodità di un contesto residenziale esclusivo.\nContattaci e vieni a scoprirlo dal vivo.",
			"energy": {
				"zeroEnergyBuilding": true,
				"thermalInsulation": null,
				"emission": null,
				"class": {
					"name": "A3",
					"color": "#5c8501"
				},
				"epi": "≥ 3,51",
				"epiUm": "m²",
				"renewableEpi": "≥ 3,51",
				"renewableEpiUm": "m²",
				"buildingPerformance": {
					"winter": "high",
					"summer": "high"
				}
			},
			"ga4Heating": "Assente",
			"features": [
				"Infissi esterni in triplo vetro / PVC"
			],
			"floor": {
				"abbreviation": "T",
				"value": "Piano terra, con ascensore",
				"floorOnlyValue": "piano terra",
				"ga4FloorValue": "piano terra"
			},
			"floors": "3 piani",
			"income": false,
			"location": {
				"latitude": 45.61510086,
				"longitude": 8.85449982,
				"zoom": 15,
				"nation": {
					"id": "IT",
					"name": "Italia",
					"keyurl": "Italia"
				},
				"region": "Lombardia",
				"province": "Varese",
				"provinceId": "VA",
				"city": "Busto Arsizio",
				"cityId": 8487,
				"macrozone": "Centro",
				"macrozoneId": 10738,
				"microzone": "Piazza Santa Maria",
				"locality": null,
				"address": "Via Gaudenzio Ferrari, 5",
				"streetNumber": null,
				"marker": "marker"
			},
			"multimedia": {
				"photos": [
					{
						"id": 1702713262,
						"caption": "Planimetria",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1702713262/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1702713262/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1702713262/cover-m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1702713262/xxl.jpg"
						},
						"tag": {
							"label": "Planimetria",
							"key": "other_planimetry",
							"category": "other"
						}
					},
					{
						"id": 1680375438,
						"caption": "Giardino",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680375438/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680375438/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680375438/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680375438/xxl.jpg"
						},
						"tag": {
							"label": "Giardino",
							"key": "ext_garden",
							"category": "other"
						}
					},
					{
						"id": 1680376904,
						"caption": "Soggiorno",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680376904/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680376904/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680376904/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680376904/xxl.jpg"
						},
						"tag": {
							"label": "Soggiorno",
							"key": "int_sitting_room",
							"category": "other"
						}
					},
					{
						"id": 1680376922,
						"caption": "Soggiorno",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680376922/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680376922/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680376922/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680376922/xxl.jpg"
						},
						"tag": {
							"label": "Soggiorno",
							"key": "int_sitting_room",
							"category": "other"
						}
					},
					{
						"id": 1680376948,
						"caption": "Giardino",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680376948/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680376948/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680376948/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680376948/xxl.jpg"
						},
						"tag": {
							"label": "Giardino",
							"key": "ext_garden",
							"category": "other"
						}
					}
				],
				"videos": [],
				"floorplans": [
					{
						"id": 113085010,
						"caption": "",
						"urls": {
							"thumb": "https://pic.im-cdn.it/plan/113085010/thumb.jpg",
							"small": "https://pic.im-cdn.it/plan/113085010/xxs-c.jpg",
							"medium": "https://pic.im-cdn.it/plan/113085010/m.jpg",
							"large": "https://pic.im-cdn.it/plan/113085010/xxl.jpg"
						},
						"url": null,
						"interactive": false
					}
				],
				"photoPlan": [],
				"virtualTours": [],
				"documents": [],
				"hasMultimedia": true,
				"hasOnlyPhotos": false
			},
			"photo": {
				"id": 1702713262,
				"caption": "Planimetria",
				"urls": {
					"thumb": "https://pwm.im-cdn.it/image/1702713262/thumb.jpg",
					"small": "https://pwm.im-cdn.it/image/1702713262/xxs-c.jpg",
					"medium": "https://pwm.im-cdn.it/image/1702713262/cover-m-c.jpg",
					"large": "https://pwm.im-cdn.it/image/1702713262/xxl.jpg"
				}
			},
			"price": {
				"visible": true,
				"value": 450000,
				"formattedValue": "€ 450.000",
				"minValue": "€ 450.000",
				"priceRange": "300.001 - 500.000 &euro;",
				"pricePerSquareMeter": "2.830 €/m²"
			},
			"reference": {
				"label": "riferimento",
				"code": "P.T. 2"
			},
			"lastUpdate": "Annuncio aggiornato il 29/07/2025",
			"rooms": "3",
			"roomsValue": "3 locali, 2 bagni",
			"surface": "159 m²",
			"typology": {
				"id": 4,
				"name": "Appartamento"
			},
			"typologyV2": {
				"id": 14,
				"name": "Appartamento"
			},
			"typologyValue": "Appartamento",
			"typologyGA4Translation": "Appartamento",
			"residentialUnits": null,
			"commercialUnits": null,
			"land": null,
			"mainFeatures": [
				{
					"type": "rooms",
					"label": "3 locali",
					"compactLabel": "3"
				},
				{
					"type": "surface",
					"label": "159 m²"
				},
				{
					"type": "bathrooms",
					"label": "2 bagni",
					"compactLabel": "2"
				},
				{
					"type": "floor",
					"label": "Piano T",
					"compactLabel": "T"
				},
				{
					"type": "elevator",
					"label": "Ascensore",
					"compactLabel": "Sì"
				}
			]
		}
	],
	"propertiesCount": 6,
	"reference": {
		"label": "riferimento",
		"code": "EK-119663118"
	},
	"state": {
		"id": 1,
		"name": "attivo"
	},
	"title": "Appartamenti di nuova costruzione a Busto Arsizio",
	"type": "ad",
	"typology": {
		"id": 112,
		"name": "Progetto"
	},
	"updatedAt": 1753805649,
	"uuid": "f5ba4c90-73ba-562b-80ac-5971b6d22443",
	"visibility": "supervetrina"
}
````

Vieni a esplorare!

#### 🔍 **Cerchi qualcos'altro?**

Sentiti libero di esplorare i [+4.000 scraper preconfigurati su Apify Store](https://apify.com/store?fpr=cbgdsf) per altre opzioni!

#### 📬 Contatti & Soluzioni Personalizzate

**Hai bisogno di qualcosa di specifico?** Vuoi fare due chiacchiere? Non esitare a contattarci! 💬

- **Discord**: `@azzouzana` 🎮
- **Email**: `labs@azzouzana.com` 📧

#### ⚠️ Disclaimer

Questo Actor è uno strumento indipendente e non è affiliato, approvato o sponsorizzato da Immobiliare.it Group o da una
qualsiasi delle sue consociate. Tutti i marchi commerciali menzionati sono di proprietà dei rispettivi titolari.

### English version

#### 🤩 Features

🚀 Our blazing fast Immobiliare.it details page scraper (by direct items URLs) 🏠 lets you extract real estate items'
information and export them to various formats (JSON, CSV, HTML etc..) 🔥 Bring your direct items URLs, and you're good
to go!
👉 It enables you to scrape rich details as title, descriptions, photos, energy information, construction date, price,
publisher information (email/phone number included), nearby transportation and a lot more.

#### 📚 How to use this actor

1. 👉 [Register for a free Apify account](https://apify.com/sign-up?fpr=cbgdsf) – no credit card required!
2. 🎉 Just click the **"Get Started"** button and complete a quick signup.
3. 💰 A free account includes enough credits to test this actor.
4. ⏳ Enjoy scraping for the free trial period, no commitment or upfront payment required.

The scraper has a required `startUrls` parameter which is an array holding a list of direct ads links

#### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

##### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

#### ⚠️ Is it legal to scrape immobiliare.it?

It is legal to scrape publicly available data such as real estate descriptions, prices, photos, nearby transportation
etc. Read our blog post on [the legality of web scraping](https://blog.apify.com/is-web-scraping-legal?fpr=cbgdsf) to learn more.

#### 🤔 Why scrape immobiliare.it?

Immobiliare.it is one of the most popular real estate websites in Italy and Europe, with hundreds of thousands of ads,
there's definitely something for you out there!

So what could you do with all these ads?

- Find real estate for sale nearby
- Do market data analysis
- Build a real estate agent email list
- Collect housing data for research or personal purposes
- Compare collected data with home value index
- Use the data for overall real estate data analytics

These are just some ideas to get you thinking about how web scraping can give you the data you need. Sky is the limit 🚀

#### 🛠️ Input

| Field | Type | Description | Default value / Example
| ----- | ---- | ----------- | ------------- |
| `startUrls`  | `array` (required) | The direct URLs real estates items that the scraper will process. | `https://www.immobiliare.it/annunci/110399387/` |

#### 🧐 Output

Output is stored in a dataset. Each item is information about a real estate item:

##### Sample output

An output might look like the below data structure:

````json
{
	"advertiser": {
		"agency": {
			"id": 130313,
			"type": "constructor",
			"showOnlyAgentPhone": false,
			"phones": [
				{
					"type": "vTel1",
					"value": "0331 167 1626"
				}
			],
			"bookableVisit": {
				"isVisitBookable": false,
				"virtualVisitEnabled": false
			},
			"isPaid": true,
			"label": "Impresa Edile",
			"displayName": "Edil Tatani",
			"guaranteed": false,
			"showAgentPhone": false,
			"showLogo": true,
			"imageUrls": {
				"small": "https://pic.im-cdn.it/imagenoresize/1671968281.jpg",
				"large": "https://pic.im-cdn.it/imagenoresize/1671968289.jpg"
			},
			"agencyUrl": "https://www.immobiliare.it/imprese-edili/130313/edil-tatani-busto/",
			"showExternalLink": true,
			"timetable": [],
			"hasPriceProposal": true
		},
		"hasCallNumbers": true
	},
	"contract": "sale",
	"contractValue": "Vendita",
	"createdAt": 1743694748,
	"dataType": "real-estate",
	"hasMainProperty": true,
	"hasParent": false,
	"id": 119663118,
	"iput_url": "https://www.immobiliare.it/annunci/119663118/",
	"isAIVoiceEnabled": false,
	"isNew": false,
	"isProjectLike": true,
	"luxury": false,
	"mortgage": {
		"showWidget": true,
		"mortgageWidget": {
			"callToAction": {
				"text": "Vuoi sapere che mutuo puoi richiedere?",
				"url": "https://www.immobiliare.it/mutui/simulazione/?src=immobiliare.it",
				"label": "Scoprilo subito"
			},
			"tax": 1154,
			"rates": [
				{
					"percent": 50,
					"rates": [
						{
							"year": 10,
							"rate": 0.0295
						},
						{
							"year": 15,
							"rate": 0.03
						},
						{
							"year": 20,
							"rate": 0.03
						},
						{
							"year": 25,
							"rate": 0.031
						},
						{
							"year": 30,
							"rate": 0.031
						}
					]
				},
				{
					"percent": 70,
					"rates": [
						{
							"year": 10,
							"rate": 0.0295
						},
						{
							"year": 15,
							"rate": 0.03
						},
						{
							"year": 20,
							"rate": 0.03
						},
						{
							"year": 25,
							"rate": 0.031
						},
						{
							"year": 30,
							"rate": 0.031
						}
					]
				},
				{
					"percent": 80,
					"rates": [
						{
							"year": 10,
							"rate": 0.0295
						},
						{
							"year": 15,
							"rate": 0.0305
						},
						{
							"year": 20,
							"rate": 0.031
						},
						{
							"year": 25,
							"rate": 0.031
						},
						{
							"year": 30,
							"rate": 0.031
						}
					]
				},
				{
					"percent": 95,
					"rates": [
						{
							"year": 10,
							"rate": 0.0366
						},
						{
							"year": 15,
							"rate": 0.0388
						},
						{
							"year": 20,
							"rate": 0.0397
						},
						{
							"year": 25,
							"rate": 0.0416
						},
						{
							"year": 30,
							"rate": 0.0416
						}
					]
				},
				{
					"percent": 100,
					"rates": [
						{
							"year": 10,
							"rate": 0.0463
						},
						{
							"year": 15,
							"rate": 0.0465
						},
						{
							"year": 20,
							"rate": 0.0469
						},
						{
							"year": 25,
							"rate": 0.0476
						},
						{
							"year": 30,
							"rate": 0.0476
						}
					]
				}
			],
			"value": 270200,
			"price": 386000
		},
		"mortgageBanner": [
			{
				"type": "link",
				"url": "https://www.immobiliare.it/mutui/simulazione/?src=immobiliare.it"
			},
			{
				"type": "preApproveLink",
				"url": "/mutui/pre-approvazione-online/?src=immobiliare.it"
			}
		]
	},
	"price": {
		"visible": true,
		"value": 386000,
		"formattedValue": "€ 386.000 - € 450.000",
		"minValue": "€ 386.000",
		"maxValue": "€ 450.000"
	},
	"properties": [
		{
			"showSurfaceConstitution": false,
			"adLinks": [],
			"primaryFeatures": [
				{
					"id": 8,
					"name": "Esposizione interna",
					"value": 0,
					"isVisible": false,
					"codeName": ""
				},
				{
					"id": 9,
					"name": "Esposizione esterna",
					"value": 0,
					"isVisible": false,
					"codeName": ""
				},
				{
					"id": 17,
					"name": "Accesso per disabili",
					"value": 1,
					"isVisible": true,
					"codeName": ""
				},
				{
					"id": 29,
					"name": "Parcheggio bici",
					"value": 0,
					"isVisible": false,
					"codeName": ""
				},
				{
					"id": null,
					"name": "Nessun giardino",
					"value": null,
					"isVisible": false,
					"codeName": "no-garden"
				},
				{
					"id": null,
					"name": "Infissi esterni in triplo vetro / PVC",
					"value": null,
					"isVisible": true,
					"codeName": "window-frames-in-triple-glass-pvc"
				}
			],
			"isMain": true,
			"ga4features": [
				"accesso per disabili",
				"infissi esterni in triplo vetro / pvc"
			],
			"id": "119663118",
			"cadastrals": [],
			"caption": "Residenza Le Due Magnolie – Eleganza Contemporanea ",
			"category": {
				"id": 27,
				"name": "Nuove costruzioni"
			},
			"costs": {
				"appliedVat": null,
				"agencyCommission": null,
				"commissionSubject": null,
				"notaryCommission": null
			},
			"description": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nNel pieno centro di Busto Arsizio, in via Gaudenzio Ferrari a soli 100 metri dal Municipio, sorge Residenza Le Due Magnolie: un raffinato edificio di nuova costruzione composto da sole 12 unità abitative, progettate per offrire il massimo comfort in un contesto moderno, efficiente e riservato. L’architettura della palazzina si distingue per linee pulite ed eleganti, perfettamente integrate nel tessuto urbano, mentre gli spazi interni sono studiati per garantire funzionalità, luminosità e benessere abitativo.\n\nOgni appartamento è unico e caratterizzato da ambienti ampi e ben distribuiti, con finiture di pregio personalizzabili e spazi esterni privati, come terrazzi o giardini, ideali per godersi momenti di relax all’aperto. \n\nL’intero edificio è in classe energetica A3 e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, pompe di calore, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata. La qualità costruttiva si traduce in efficienza, risparmio e comfort quotidiano.\n\nCompletano la proposta box auto doppi e cantine private, collegati direttamente ai piani tramite ascensore. La posizione è strategica: centrale, servita, comoda per la stazione e perfetta per chi desidera vivere in pieno centro città senza rinunciare alla tranquillità.\n\nResidenza Le Due Magnolie è la scelta ideale per chi cerca una casa elegante, tecnologica e a misura di vita.",
			"defaultDescription": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nNel pieno centro di Busto Arsizio, in via Gaudenzio Ferrari a soli 100 metri dal Municipio, sorge Residenza Le Due Magnolie: un raffinato edificio di nuova costruzione composto da sole 12 unità abitative, progettate per offrire il massimo comfort in un contesto moderno, efficiente e riservato. L’architettura della palazzina si distingue per linee pulite ed eleganti, perfettamente integrate nel tessuto urbano, mentre gli spazi interni sono studiati per garantire funzionalità, luminosità e benessere abitativo.\n\nOgni appartamento è unico e caratterizzato da ambienti ampi e ben distribuiti, con finiture di pregio personalizzabili e spazi esterni privati, come terrazzi o giardini, ideali per godersi momenti di relax all’aperto. \n\nL’intero edificio è in classe energetica A3 e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, pompe di calore, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata. La qualità costruttiva si traduce in efficienza, risparmio e comfort quotidiano.\n\nCompletano la proposta box auto doppi e cantine private, collegati direttamente ai piani tramite ascensore. La posizione è strategica: centrale, servita, comoda per la stazione e perfetta per chi desidera vivere in pieno centro città senza rinunciare alla tranquillità.\n\nResidenza Le Due Magnolie è la scelta ideale per chi cerca una casa elegante, tecnologica e a misura di vita.",
			"energy": {
				"zeroEnergyBuilding": true,
				"thermalInsulation": null,
				"emission": null,
				"heatingType": "centralizzato, a pavimento, alimentato a pompa di calore",
				"airConditioning": "autonomo, freddo/caldo",
				"class": {
					"name": "A3",
					"color": "#5c8501"
				},
				"epi": "≥ 3,51",
				"epiUm": "m²",
				"renewableEpi": "≥ 3,51",
				"renewableEpiUm": "m²",
				"buildingPerformance": {
					"winter": "high",
					"summer": "high"
				}
			},
			"ga4Heating": "Centralizzato",
			"features": [
				"Infissi esterni in triplo vetro / PVC"
			],
			"floors": "3 piani",
			"garage": "12 in box privato/box in garage",
			"income": false,
			"location": {
				"latitude": 45.6151,
				"longitude": 8.8545,
				"zoom": 15,
				"nation": {
					"id": "IT",
					"name": "Italia",
					"keyurl": "Italia"
				},
				"region": "Lombardia",
				"province": "Varese",
				"provinceId": "VA",
				"city": "Busto Arsizio",
				"cityId": 8487,
				"macrozone": "Centro",
				"macrozoneId": 10738,
				"microzone": "Piazza Santa Maria",
				"locality": null,
				"address": "Via Gaudenzio Ferrari, 5",
				"streetNumber": null,
				"marker": "marker"
			},
			"multimedia": {
				"photos": [
					{
						"id": 1679617014,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679617014/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679617014/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679617014/cover-m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679617014/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1679617036,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679617036/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679617036/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679617036/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679617036/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1679615630,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679615630/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679615630/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679615630/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679615630/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1679614886,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679614886/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679614886/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679614886/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679614886/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1679614664,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679614664/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679614664/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679614664/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679614664/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1679615738,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679615738/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679615738/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679615738/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679615738/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1680224688,
						"caption": "Facciata",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680224688/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680224688/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680224688/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680224688/xxl.jpg"
						},
						"tag": {
							"label": "Facciata",
							"key": "ext_palace",
							"category": "other"
						}
					},
					{
						"id": 1680223906,
						"caption": "Giardino",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680223906/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680223906/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680223906/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680223906/xxl.jpg"
						},
						"tag": {
							"label": "Giardino",
							"key": "ext_garden",
							"category": "other"
						}
					},
					{
						"id": 1679618050,
						"caption": "Ascensori",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679618050/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679618050/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679618050/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679618050/xxl.jpg"
						},
						"tag": {
							"label": "Ascensori",
							"key": "ext_elevators",
							"category": "other"
						}
					},
					{
						"id": 1679618066,
						"caption": "Scala",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1679618066/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1679618066/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1679618066/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1679618066/xxl.jpg"
						},
						"tag": {
							"label": "Scala",
							"key": "other_staircase",
							"category": "other"
						}
					}
				],
				"videos": [],
				"floorplans": [],
				"photoPlan": [],
				"virtualTours": [],
				"documents": [
					{
						"id": 19090856,
						"type": "capitolato",
						"format": "pdf",
						"length": 5834037,
						"title": "Scarica capitolato",
						"url": "https://pic.im-cdn.it/file/19090856"
					}
				],
				"hasMultimedia": true,
				"hasOnlyPhotos": true
			},
			"photo": {
				"id": 1679617014,
				"caption": "Facciata",
				"urls": {
					"thumb": "https://pwm.im-cdn.it/image/1679617014/thumb.jpg",
					"small": "https://pwm.im-cdn.it/image/1679617014/xxs-c.jpg",
					"medium": "https://pwm.im-cdn.it/image/1679617014/cover-m-c.jpg",
					"large": "https://pwm.im-cdn.it/image/1679617014/xxl.jpg"
				}
			},
			"price": {
				"visible": true,
				"value": 386000,
				"formattedValue": "€ 386.000 - € 450.000",
				"minValue": "€ 386.000",
				"maxValue": "€ 450.000"
			},
			"lastUpdate": "Annuncio aggiornato il 29/07/2025",
			"rent": {
				"deposit": null,
				"priceReferenceIndex": null,
				"redemptionRent": null,
				"availableToStudents": false
			},
			"surface": "128 m²",
			"typology": {
				"id": 112,
				"name": "Progetto"
			},
			"typologyV2": {
				"id": 276,
				"name": "Progetto"
			},
			"typologyValue": "Progetto",
			"ga4Garage": "12 in box privato/box in garage",
			"typologyGA4Translation": "Progetto",
			"unitsValue": "12 abitative",
			"residentialUnits": 12,
			"commercialUnits": null,
			"workDates": "01/01/2021 - 01/07/2024",
			"workProgress": "Lavori completati nel luglio del 2024.",
			"land": null,
			"typologyAmount": 6,
			"mainFeatures": [
				{
					"type": "rooms",
					"label": "3 - 4 locali",
					"compactLabel": "3 - 4"
				},
				{
					"type": "surface",
					"label": "da 128 m²"
				},
				{
					"type": "typologyAmount",
					"label": "6 tipologie",
					"compactLabel": "6"
				}
			],
			"rooms": "3 - 4"
		},
		{
			"showSurfaceConstitution": false,
			"adLinks": [],
			"primaryFeatures": [
				{
					"id": 17,
					"name": "Accesso per disabili",
					"value": 1,
					"isVisible": true,
					"codeName": ""
				},
				{
					"id": null,
					"name": "balcone",
					"value": 1,
					"isVisible": true,
					"codeName": "balcony"
				},
				{
					"id": null,
					"name": "terrazza",
					"value": 1,
					"isVisible": true,
					"codeName": "terrace"
				},
				{
					"id": null,
					"name": "Nessun giardino",
					"value": null,
					"isVisible": false,
					"codeName": "no-garden"
				},
				{
					"id": null,
					"name": "Infissi esterni in triplo vetro / PVC",
					"value": null,
					"isVisible": true,
					"codeName": "window-frames-in-triple-glass-pvc"
				}
			],
			"isMain": false,
			"ga4features": [
				"accesso per disabili",
				"balcone",
				"terrazzo",
				"infissi esterni in triplo vetro / pvc"
			],
			"id": "18601630",
			"elevator": true,
			"bathrooms": "2",
			"cadastrals": [],
			"caption": "Trilocale - Primo Piano",
			"category": {
				"id": 1,
				"name": "Residenziale"
			},
			"description": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nElegante trilocale con superficie commerciale di 128 m² situato al primo piano, progettato per offrire comfort, razionalità degli spazi e luminosità naturale. L’ampia zona giorno open space, con cucina a vista e angolo relax, si apre su un ampio e luminoso terrazzo ideale per pranzi all’aperto o momenti di relax.\n\nLa zona notte è ben separata e offre due camere da letto, di cui una padronale con bagno privato dedicato ed un ampio balcone. Un altro bagno finestrato serve la zona giorno e la seconda camera. Gli ambienti sono ben distribuiti e valorizzati da finiture di pregio personalizzabili, pensati per accogliere sia la vita quotidiana che i momenti speciali.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata. \n\nUn appartamento ideale per chi cerca un’abitazione raffinata e funzionale in un contesto residenziale esclusivo nel cuore della città.\nContattaci e vieni a scoprirlo dal vivo.",
			"defaultDescription": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nElegante trilocale con superficie commerciale di 128 m² situato al primo piano, progettato per offrire comfort, razionalità degli spazi e luminosità naturale. L’ampia zona giorno open space, con cucina a vista e angolo relax, si apre su un ampio e luminoso terrazzo ideale per pranzi all’aperto o momenti di relax.\n\nLa zona notte è ben separata e offre due camere da letto, di cui una padronale con bagno privato dedicato ed un ampio balcone. Un altro bagno finestrato serve la zona giorno e la seconda camera. Gli ambienti sono ben distribuiti e valorizzati da finiture di pregio personalizzabili, pensati per accogliere sia la vita quotidiana che i momenti speciali.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata. \n\nUn appartamento ideale per chi cerca un’abitazione raffinata e funzionale in un contesto residenziale esclusivo nel cuore della città.\nContattaci e vieni a scoprirlo dal vivo.",
			"energy": {
				"zeroEnergyBuilding": true,
				"thermalInsulation": null,
				"emission": null,
				"class": {
					"name": "A3",
					"color": "#5c8501"
				},
				"epi": "≥ 3,51",
				"epiUm": "m²",
				"renewableEpi": "≥ 3,51",
				"renewableEpiUm": "m²",
				"buildingPerformance": {
					"winter": "high",
					"summer": "high"
				}
			},
			"ga4Heating": "Assente",
			"features": [
				"Infissi esterni in triplo vetro / PVC"
			],
			"floor": {
				"abbreviation": "1",
				"value": "1° piano, con ascensore",
				"floorOnlyValue": "1 piano",
				"ga4FloorValue": "1 piano"
			},
			"floors": "3 piani",
			"income": false,
			"location": {
				"latitude": 45.61510086,
				"longitude": 8.85449982,
				"zoom": 15,
				"nation": {
					"id": "IT",
					"name": "Italia",
					"keyurl": "Italia"
				},
				"region": "Lombardia",
				"province": "Varese",
				"provinceId": "VA",
				"city": "Busto Arsizio",
				"cityId": 8487,
				"macrozone": "Centro",
				"macrozoneId": 10738,
				"microzone": "Piazza Santa Maria",
				"locality": null,
				"address": "Via Gaudenzio Ferrari, 5",
				"streetNumber": null,
				"marker": "marker"
			},
			"multimedia": {
				"photos": [
					{
						"id": 1702711790,
						"caption": "Planimetria",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1702711790/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1702711790/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1702711790/cover-m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1702711790/xxl.jpg"
						},
						"tag": {
							"label": "Planimetria",
							"key": "other_planimetry",
							"category": "other"
						}
					},
					{
						"id": 1680392676,
						"caption": "Terrazzo",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680392676/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680392676/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680392676/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680392676/xxl.jpg"
						},
						"tag": {
							"label": "Terrazzo",
							"key": "ext_terrace",
							"category": "other"
						}
					},
					{
						"id": 1680392812,
						"caption": "Soggiorno",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680392812/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680392812/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680392812/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680392812/xxl.jpg"
						},
						"tag": {
							"label": "Soggiorno",
							"key": "int_sitting_room",
							"category": "other"
						}
					},
					{
						"id": 1680392916,
						"caption": "Soggiorno",
						"urls": {
							"thumb": "https://pwm.im-cdn.it/image/1680392916/thumb.jpg",
							"small": "https://pwm.im-cdn.it/image/1680392916/xxs-c.jpg",
							"medium": "https://pwm.im-cdn.it/image/1680392916/m-c.jpg",
							"large": "https://pwm.im-cdn.it/image/1680392916/xxl.jpg"
						},
						"tag": {
							"label": "Soggiorno",
							"key": "int_sitting_room",
							"category": "other"
						}
					}
				],
				"videos": [],
				"floorplans": [
					{
						"id": 113085878,
						"caption": "",
						"urls": {
							"thumb": "https://pic.im-cdn.it/plan/113085878/thumb.jpg",
							"small": "https://pic.im-cdn.it/plan/113085878/xxs-c.jpg",
							"medium": "https://pic.im-cdn.it/plan/113085878/m.jpg",
							"large": "https://pic.im-cdn.it/plan/113085878/xxl.jpg"
						},
						"url": null,
						"interactive": false
					}
				],
				"photoPlan": [],
				"virtualTours": [],
				"documents": [],
				"hasMultimedia": true,
				"hasOnlyPhotos": false
			},
			"photo": {
				"id": 1702711790,
				"caption": "Planimetria",
				"urls": {
					"thumb": "https://pwm.im-cdn.it/image/1702711790/thumb.jpg",
					"small": "https://pwm.im-cdn.it/image/1702711790/xxs-c.jpg",
					"medium": "https://pwm.im-cdn.it/image/1702711790/cover-m-c.jpg",
					"large": "https://pwm.im-cdn.it/image/1702711790/xxl.jpg"
				}
			},
			"price": {
				"visible": true,
				"value": 386000,
				"formattedValue": "€ 386.000",
				"minValue": "€ 386.000",
				"priceRange": "300.001 - 500.000 &euro;",
				"pricePerSquareMeter": "3.016 €/m²"
			},
			"lastUpdate": "Annuncio aggiornato il 29/07/2025",
			"rooms": "3",
			"roomsValue": "3 locali, 2 bagni",
			"surface": "128 m²",
			"typology": {
				"id": 4,
				"name": "Appartamento"
			},
			"typologyV2": {
				"id": 14,
				"name": "Appartamento"
			},
			"typologyValue": "Appartamento",
			"typologyGA4Translation": "Appartamento",
			"residentialUnits": null,
			"commercialUnits": null,
			"land": null,
			"mainFeatures": [
				{
					"type": "rooms",
					"label": "3 locali",
					"compactLabel": "3"
				},
				{
					"type": "surface",
					"label": "128 m²"
				},
				{
					"type": "bathrooms",
					"label": "2 bagni",
					"compactLabel": "2"
				},
				{
					"type": "floor",
					"label": "Piano 1",
					"compactLabel": "1"
				},
				{
					"type": "elevator",
					"label": "Ascensore",
					"compactLabel": "Sì"
				}
			]
		},
		{
			"showSurfaceConstitution": false,
			"adLinks": [],
			"primaryFeatures": [
				{
					"id": 17,
					"name": "Accesso per disabili",
					"value": 1,
					"isVisible": true,
					"codeName": ""
				},
				{
					"id": null,
					"name": "balcone",
					"value": 1,
					"isVisible": true,
					"codeName": "balcony"
				},
				{
					"id": null,
					"name": "terrazza",
					"value": 1,
					"isVisible": true,
					"codeName": "terrace"
				},
				{
					"id": null,
					"name": "Giardino privato",
					"value": null,
					"isVisible": true,
					"codeName": "private-garden"
				},
				{
					"id": null,
					"name": "Infissi esterni in triplo vetro / PVC",
					"value": null,
					"isVisible": true,
					"codeName": "window-frames-in-triple-glass-pvc"
				}
			],
			"isMain": false,
			"ga4features": [
				"accesso per disabili",
				"balcone",
				"terrazzo",
				"giardino privato",
				"infissi esterni in triplo vetro / pvc"
			],
			"id": "19559316",
			"elevator": true,
			"bathrooms": "2",
			"cadastrals": [],
			"caption": "TRILOCALE CON GIARDINO PRIVATO - PIANO TERRA",
			"category": {
				"id": 1,
				"name": "Residenziale"
			},
			"description": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nAmpio trilocale al piano terra con superficie commerciale di 147 m² con spazi ben distribuiti e grande luminosità. L’ampia zona giorno open space si affaccia sul terrazzo e sull'elegante giardino privato, perfetto per vivere l’esterno in ogni stagione. La zona notte è composta da tre camere da letto e doppi servizi.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata.\n\nIdeale per famiglie o per chi cerca il comfort di una casa indipendente con tutte le comodità di un contesto residenziale esclusivo.\nContattaci e vieni a scoprirlo dal vivo.",
			"defaultDescription": "VENDITA DIRETTA DAL COSTRUTTORE - ZERO COMMISSIONI DI AGENZIA\n\nAmpio trilocale al piano terra con superficie commerciale di 147 m² con spazi ben distribuiti e grande luminosità. L’ampia zona giorno open space si affaccia sul terrazzo e sull'elegante giardino privato, perfetto per vivere l’esterno in ogni stagione. La zona notte è composta da tre camere da letto e doppi servizi.\n\nClasse energetica A3, finiture personalizzabili e dotato delle più avanzate tecnologie: riscaldamento e raffrescamento a pavimento, impianto domotico, isolamento termo-acustico e la ventilazione e deumidificazione meccanica controllata.\n\nIdeale per famiglie o per chi cerca il comfort di una casa indipendente con tutte le comodità di un contesto residenziale esclusivo.\nContattaci e vieni a scoprirlo dal vivo.",
			"energy": {
				"zeroEnergyBuilding": true,
				"thermalInsulation": null,
				"emission": null,
				"class": {
					"name": "A3",
					"color": "#5c8501"
				},
				"epi": "≥ 3,51",
				"epiUm": "m²",
				"renewableEpi": "≥ 3,51",
				"renewableEpiUm": "m²",
				"buildingPerformance": {
					"winter": "high",
					"summer": "high"
				}
			},
			"ga4Heating": "Assente",
			"features": [
				"Infissi esterni in triplo vetro / PVC"
			],
			"floor": {
				"abbreviation": "T",
				"value": "Piano terra, con ascensore",
				"floorOnlyValue": "piano terra",
				"ga4FloorV

# Actor input Schema

## `startUrls` (type: `array`):

URLs to start with.

## Actor input object example

```json
{
  "startUrls": [
    "https://www.immobiliare.it/annunci/1234939919"
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
        "https://www.immobiliare.it/annunci/1234939919"
    ]
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/immobiliare-it-listing-page-scraper-by-items-urls").call(input);

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
run_input = { "startUrls": ["https://www.immobiliare.it/annunci/1234939919"] }

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/immobiliare-it-listing-page-scraper-by-items-urls").call(run_input=run_input)

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
    "https://www.immobiliare.it/annunci/1234939919"
  ]
}' |
apify call azzouzana/immobiliare-it-listing-page-scraper-by-items-urls --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/immobiliare-it-listing-page-scraper-by-items-urls",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
