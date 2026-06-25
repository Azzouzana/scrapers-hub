# 🚀 Meta Ads Library Scraper — Facebook & Instagram (Pages & Search URLs)

> **⚡ Cloud-Hosted Tool:** This repository contains the official documentation and support hub for the Meta Ads Library Scraper — Facebook & Instagram (Pages & Search URLs). This tool runs entirely in the cloud on the Apify platform—no local installation, proxy management, or infrastructure maintenance required.
>
> [👉 RUN THIS SCRAPER ON APIFY](https://apify.com/azzouzana/meta-facebook-instagram-ads-library?fpr=cbgdsf)

---

## Meta Ads Library Scraper — Facebook & Instagram (Pages & Search URLs)

Manually extracting data from the **Meta Ads Library** (Facebook & Instagram ads) is a massive time-sink. We built this scraper to be the most reliable, high-speed way to get that data into your hands.

### Engineering Excellence & Reliability 🚀

- **Zero-Friction Resolution**: Drop in a direct Facebook Page URL or a complex Ads Library search URL. We serve you back, clean data.
- **High-Velocity Automation**: Our lightweight architecture is built for speed and stamina. While you’re grabbing a coffee, we’re paginating through thousands of ads with precision.
- **Granular Audience Intelligence**: Need more than just a surface-level scan? Enable `extractDetails` for a deep dive into demographics (age/gender), precise reach, and regional delivery data.
- **enterprise-Grade Resilience**: Built to bypass detection, handle retries, and deliver 100% clean, sorted JSON data every single time.
- **Lightweight PPE Pricing**: No bloated subscriptions. Our Pay-Per-Event model ensures you only pay for the successful results you actually receive.

### 🛠️ How to Play

#### Input Parameters

| Field | Type | Description |
|-------|------|-------------|
| `startUrl` | String | **(Required)** Direct Page URL or a pre-filtered Ads Library search URL. |
| `maxAds` | Number | How many ads do you actually need? (Default: 100) |
| `extractDetails` | Boolean | `true` = Deep data (Reach, Demographics). `false` = Quick summary. |

#### Example 1: The "I want everything from this page" Search
```json
{
    "startUrl": "https://www.facebook.com/adidas/",
    "extractDetails": true,
    "maxAds": 50
}
````

#### Example 2: The "Ads library UR search, please" Search

```json
{
    "startUrl": "https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=US&q=running%20shoes",
    "extractDetails": false,
    "maxAds": 100
}
```

### 💰 The Math (It’s Friendly!)

Our Pay-Per-Event (PPE) model is simpler than a 1st-grade math quiz:

- **The Basics**: **$0.5 per 1,000 ads** (For the index data).
- **The Details**: **+$0.5 per 1,000 ads** (Only if you fetch deep metrics like reach/demographics).

Total for 1,000 fully-detailed ads: **$1.00**. That's cheaper than a bad latte.

### 🆓 Free tier limitations

We want you to see how this actor works before you commit. To keep things fair for everyone, the **free tier** usually includes these trial limits:

- **Sample data:** up to **5 listings** per run—enough to check data quality.
- **Daily cap:** **5 runs** per calendar day (UTC).
- **Between runs:** at least **30 minutes** before you can start another run.

> Limits can change with platform load depending on system load and your intended scraping to prevent what we might interpret as free users abuse.

#### Upgrade when you're ready!

Use the free tier to decide if this actor fits your project. Paid Apify plans remove these wait times and caps so you can run at full volume—[**upgrade to a paid plan**](https://apify.com/pricing?fpr=cbgdsf).

### 📦 What’s in the Box?

We deliver a clean, sorted JSON for every ad. No clutter, no mystery keys.

```json
{
  "aaa_info": {
    "has_violating_payer_beneficiary": false,
    "is_ad_taken_down": false,
    "payer_beneficiary_data": [],
    "targets_eu": false
  },
  "ad_archive_id": "1247196049838563",
  "advertiser": {
    "ad_library_page_info": {
      "page_info": {
        "entity_type": "PERSON_PROFILE",
        "ig_followers": 29537558,
        "ig_username": "adidas",
        "ig_verification": true,
        "is_profile_page": false,
        "likes": 43273726,
        "page_alias": "adidas",
        "page_category": "Product/service",
        "page_cover_photo": "https://scontent-lga3-3.xx.fbcdn.net/v/t39.30808-6/514287112_1135327741952281_436765062017775631_n.jpg?_nc_cat=110&ccb=1-7&_nc_sid=9b1e99&_nc_ohc=RI80WD75b5cQ7kNvwHCQ99C&_nc_oc=AdnNmbPpfcVFX9K6kTryu0c0Ka9z7sY5w_8Y7aZdlQxz1oAFGrSMHaCNvvw91NzkQM0&_nc_zt=23&_nc_ht=scontent-lga3-3.xx&_nc_gid=0De9znyOtHpOj2kASZbVZQ&_nc_ss=8&oh=00_Afwm71ggjQeIhp8yJ3-uGnj-UDNkSeStQGfr3-gLTC7FTg&oe=69ABDB91",
        "page_id": "182162001806727",
        "page_is_deleted": false,
        "page_is_restricted": false,
        "page_name": "adidas",
        "page_profile_uri": "https://www.facebook.com/adidas/",
        "page_verification": "BLUE_VERIFIED",
        "profile_photo": "https://scontent-lga3-2.xx.fbcdn.net/v/t39.30808-1/438169687_822361736582218_6310067482670633529_n.jpg?stp=dst-jpg_s148x148_tt6&_nc_cat=1&ccb=1-7&_nc_sid=418b77&_nc_ohc=oNfy-Ko0IWIQ7kNvwGWjrhf&_nc_oc=Adk52ufhHNjfubBEm11VBXXaCsxwWchDJg-GJFLn1L5oCptR9-aQHo8F0GDGMEx42xk&_nc_zt=24&_nc_ht=scontent-lga3-2.xx&_nc_gid=0De9znyOtHpOj2kASZbVZQ&_nc_ss=8&oh=00_AfxWdQgjT_zU_nKsKijlHVj03o-B9Abj5tRUutTnqSB6ew&oe=69ABC6BD"
      },
      "page_spend": {
        "is_political_page": false,
        "lifetime_by_disclaimer": [],
        "weekly_by_disclaimer": []
      }
    },
    "page": {
      "about": {
        "text": "Through sport we have the power to change lives. "
      },
      "id": "182162001806727",
      "is_delegate_page_with_linked_primary_profile": false
    }
  },
  "categories": [
    "UNKNOWN"
  ],
  "contains_digital_created_media": false,
  "contains_sensitive_content": false,
  "currency": "",
  "end_date": 1772438400,
  "gated_type": "ELIGIBLE",
  "has_user_reported": false,
  "hide_data_status": "NONE",
  "impressions_with_index": {
    "impressions_index": -1
  },
  "is_aaa_eligible": true,
  "is_active": true,
  "is_violating_eu_siep": false,
  "menu_items": [],
  "page_id": "182162001806727",
  "page_is_deleted": false,
  "page_name": "adidas",
  "publisher_platform": [
    "FACEBOOK",
    "INSTAGRAM",
    "AUDIENCE_NETWORK",
    "MESSENGER"
  ],
  "regional_regulation_data": {
    "finserv": {
      "is_deemed_finserv": false,
      "is_limited_delivery": false
    },
    "tw_anti_scam": {
      "is_limited_delivery": false
    }
  },
  "snapshot": {
    "body": {
      "text": "En yeni ürünleri stoklar tükenmeden keşfet!"
    },
    "caption": "trendyol.com",
    "cards": [
      {
        "body": "En yeni ürünleri stoklar tükenmeden keşfet!",
        "caption": "trendyol.com",
        "cta_text": "Shop Now",
        "cta_type": "SHOP_NOW",
        "image_crops": [],
        "link_description": "adidas mağazasının ürünleri çeşitli indirim ve kampanya fırsatlarıyla Trendyol’da. adidas ürünleriyle alışverişin keyfini çıkarın!",
        "link_url": "https://www.trendyol.com/adidas/aeroready-designed-2-move-woven-erkek-sort-gt8161-p-121933974?boutiqueId=637297&merchantId=61",
        "original_image_url": "https://scontent-lga3-2.xx.fbcdn.net/v/t39.35426-6/458984539_910117537802622_6014979994684120870_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=UwGyR6IJA7UQ7kNvwH6cMPY&_nc_oc=AdmUjYcIwj_GQ-cDy1N_1G4TcTRJgP1zDXvugXLQCiA3b2o4G2ANTP7e2TfCa77-LEo&_nc_zt=14&_nc_ht=scontent-lga3-2.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_Afzdofw9oY3gsVo0VbCBdi-NPP--6f7DmsWfCYOG5Rwg5A&oe=69ABE901",
        "resized_image_url": "https://scontent-lga3-2.xx.fbcdn.net/v/t39.35426-6/458984539_910117537802622_6014979994684120870_n.jpg?stp=dst-jpg_s600x600_tt6&_nc_cat=109&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=UwGyR6IJA7UQ7kNvwH6cMPY&_nc_oc=AdmUjYcIwj_GQ-cDy1N_1G4TcTRJgP1zDXvugXLQCiA3b2o4G2ANTP7e2TfCa77-LEo&_nc_zt=14&_nc_ht=scontent-lga3-2.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_AfxTVVw-4pBdhn797Bp-1hWVLpodHSVnzr_gsidKPSqT-Q&oe=69ABE901",
        "title": "Adidas aeroready designed 2 move woven erkek şort",
        "watermarked_resized_image_url": ""
      },
      {
        "body": "En yeni ürünleri stoklar tükenmeden keşfet!",
        "caption": "trendyol.com",
        "cta_text": "Shop Now",
        "cta_type": "SHOP_NOW",
        "image_crops": [],
        "link_description": "adidas mağazasının ürünleri çeşitli indirim ve kampanya fırsatlarıyla Trendyol’da. adidas ürünleriyle alışverişin keyfini çıkarın!",
        "link_url": "https://www.trendyol.com/adidas/aeroready-designed-to-move-sport-3-stripes-tisort-p-102735749?boutiqueId=637297&merchantId=61",
        "original_image_url": "https://scontent-lga3-3.xx.fbcdn.net/v/t39.35426-6/459179979_1522928291948784_5242565886003771747_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=06UkowcIXHEQ7kNvwEnudSZ&_nc_oc=Adl0jj8keISA79qOruCVvop_PotPwwoT9ISRk2G6jMOy9OZjBhfML2sm7uOrWJZFSMM&_nc_zt=14&_nc_ht=scontent-lga3-3.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_Afza8lzcJW07UyJJ6USDs3N5OKXdzCDjoTFjT1uIFiX_PA&oe=69ABEE6B",
        "resized_image_url": "https://scontent-lga3-3.xx.fbcdn.net/v/t39.35426-6/459179979_1522928291948784_5242565886003771747_n.jpg?stp=dst-jpg_s600x600_tt6&_nc_cat=106&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=06UkowcIXHEQ7kNvwEnudSZ&_nc_oc=Adl0jj8keISA79qOruCVvop_PotPwwoT9ISRk2G6jMOy9OZjBhfML2sm7uOrWJZFSMM&_nc_zt=14&_nc_ht=scontent-lga3-3.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_Afxhl98QEff568r4N4D3KnSYT2wxrFOIO3l5A1Ha6AL6Iw&oe=69ABEE6B",
        "title": "Adidas aeroready designed to move sport 3-stripes tişört",
        "watermarked_resized_image_url": ""
      },
      {
        "body": "En yeni ürünleri stoklar tükenmeden keşfet!",
        "caption": "trendyol.com",
        "cta_text": "Shop Now",
        "cta_type": "SHOP_NOW",
        "image_crops": [],
        "link_description": "adidas mağazasının ürünleri çeşitli indirim ve kampanya fırsatlarıyla Trendyol’da. adidas ürünleriyle alışverişin keyfini çıkarın!",
        "link_url": "https://www.trendyol.com/adidas/aeroready-essentials-chelsea-3-stripes-sort-p-102831156?boutiqueId=637299&merchantId=61",
        "original_image_url": "https://scontent-lga3-1.xx.fbcdn.net/v/t39.35426-6/458955856_365827979921544_6295218169291992724_n.jpg?_nc_cat=111&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=pUEz3xZbx_4Q7kNvwGQrHKP&_nc_oc=AdnzCZfBhyMGKEerIceU9CUdcZrgoE_p1Y2026Cs0xjs3O25vGdogs06ptFG4FioRmM&_nc_zt=14&_nc_ht=scontent-lga3-1.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_AfwMz8Ol3kvxsJpUD-hyCAMg0CKGJBwMGFGWIOGAi7U8Dw&oe=69ABCCCA",
        "resized_image_url": "https://scontent-lga3-1.xx.fbcdn.net/v/t39.35426-6/458955856_365827979921544_6295218169291992724_n.jpg?stp=dst-jpg_s600x600_tt6&_nc_cat=111&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=pUEz3xZbx_4Q7kNvwGQrHKP&_nc_oc=AdnzCZfBhyMGKEerIceU9CUdcZrgoE_p1Y2026Cs0xjs3O25vGdogs06ptFG4FioRmM&_nc_zt=14&_nc_ht=scontent-lga3-1.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_AfynJU8MdbxHbhRAelV5e69RSs5eqqsa4nZGs2emOOvOrw&oe=69ABCCCA",
        "title": "Adidas aeroready essentials chelsea 3-stripes şort",
        "watermarked_resized_image_url": ""
      },
      {
        "body": "En yeni ürünleri stoklar tükenmeden keşfet!",
        "caption": "trendyol.com",
        "cta_text": "Shop Now",
        "cta_type": "SHOP_NOW",
        "image_crops": [],
        "link_description": "adidas mağazasının ürünleri çeşitli indirim ve kampanya fırsatlarıyla Trendyol’da. adidas ürünleriyle alışverişin keyfini çıkarın!",
        "link_url": "https://www.trendyol.com/adidas/loungewear-essentials-slim-3-stripes-kadin-tisort-gl0783-p-103712544?boutiqueId=637299&merchantId=61",
        "original_image_url": "https://scontent-lga3-3.xx.fbcdn.net/v/t39.35426-6/459203591_8388306787893087_6744967283201809953_n.jpg?_nc_cat=104&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=cPeNi2UTysoQ7kNvwHghTey&_nc_oc=AdkcHhtbVsr3w1nbVBgmSsXF_mqjLzuHhwIq_QvxifuOWUCHrtfGAmqfbmDd5MdUEng&_nc_zt=14&_nc_ht=scontent-lga3-3.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_Afx5nqfMsIFaIW74lxfzMBp7pagC2a9WcrNQwn0ozCMdMg&oe=69ABD242",
        "resized_image_url": "https://scontent-lga3-3.xx.fbcdn.net/v/t39.35426-6/459203591_8388306787893087_6744967283201809953_n.jpg?stp=dst-jpg_s600x600_tt6&_nc_cat=104&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=cPeNi2UTysoQ7kNvwHghTey&_nc_oc=AdkcHhtbVsr3w1nbVBgmSsXF_mqjLzuHhwIq_QvxifuOWUCHrtfGAmqfbmDd5MdUEng&_nc_zt=14&_nc_ht=scontent-lga3-3.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_AfyudVj-ffWJFCuV0YemlLIuMOTSeWvtNidfgLWu3rI0oA&oe=69ABD242",
        "title": "Adidas loungewear essentials slim 3-stripes kadın tişört gl0783",
        "watermarked_resized_image_url": ""
      },
      {
        "body": "En yeni ürünleri stoklar tükenmeden keşfet!",
        "caption": "trendyol.com",
        "cta_text": "Shop Now",
        "cta_type": "SHOP_NOW",
        "image_crops": [],
        "link_description": "adidas mağazasının ürünleri çeşitli indirim ve kampanya fırsatlarıyla Trendyol’da. adidas ürünleriyle alışverişin keyfini çıkarın!",
        "link_url": "https://www.trendyol.com/adidas/aeroready-designed-to-move-sport-3-stripes-tisort-p-108524756?boutiqueId=637297&merchantId=61",
        "original_image_url": "https://scontent-lga3-3.xx.fbcdn.net/v/t39.35426-6/458942054_540660991955062_7574167761605093131_n.jpg?_nc_cat=110&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=bg-ggtF6jjMQ7kNvwFfxmN3&_nc_oc=AdnQD12U3Qg6lcPFY4X8sVcq5LAN1qYMXLM2NuWM7C5KWwjWzh7H6PfOkIpYo8mOgsY&_nc_zt=14&_nc_ht=scontent-lga3-3.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_Afxqbtte27DYgaWOrAC8pxN_HyWPKE65B2TkgbFE8syVxA&oe=69ABD6B7",
        "resized_image_url": "https://scontent-lga3-3.xx.fbcdn.net/v/t39.35426-6/458942054_540660991955062_7574167761605093131_n.jpg?stp=dst-jpg_s600x600_tt6&_nc_cat=110&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=bg-ggtF6jjMQ7kNvwFfxmN3&_nc_oc=AdnQD12U3Qg6lcPFY4X8sVcq5LAN1qYMXLM2NuWM7C5KWwjWzh7H6PfOkIpYo8mOgsY&_nc_zt=14&_nc_ht=scontent-lga3-3.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_Afx1bBfDFegxsRQ__N5CA_KM6ZREaQEQqUqxfzwtjy4PAQ&oe=69ABD6B7",
        "title": "Adidas aeroready designed to move sport 3-stripes tişört",
        "watermarked_resized_image_url": ""
      },
      {
        "body": "En yeni ürünleri stoklar tükenmeden keşfet!",
        "caption": "trendyol.com",
        "cta_text": "Shop Now",
        "cta_type": "SHOP_NOW",
        "image_crops": [],
        "link_description": "adidas mağazasının ürünleri çeşitli indirim ve kampanya fırsatlarıyla Trendyol’da. adidas ürünleriyle alışverişin keyfini çıkarın!",
        "link_url": "https://www.trendyol.com/adidas/designed-2-move-3-stripes-tisort-p-111298816?boutiqueId=637299&merchantId=61",
        "original_image_url": "https://scontent-lga3-2.xx.fbcdn.net/v/t39.35426-6/458987405_815114647455849_1083379548238680318_n.jpg?_nc_cat=105&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=RsFkyRb-JN8Q7kNvwFLVyRD&_nc_oc=AdlbH77IXUhxRaCRrIHPtJHJtz99_yiVxadZQyNVJfXYiQAIGu-95x5yTOIaEBDzLaQ&_nc_zt=14&_nc_ht=scontent-lga3-2.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_AfzBH7mhNrUNhKXvd1J4hFjfsYRehK75kmKbZZWwz4fyUQ&oe=69ABF50D",
        "resized_image_url": "https://scontent-lga3-2.xx.fbcdn.net/v/t39.35426-6/458987405_815114647455849_1083379548238680318_n.jpg?stp=dst-jpg_s600x600_tt6&_nc_cat=105&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=RsFkyRb-JN8Q7kNvwFLVyRD&_nc_oc=AdlbH77IXUhxRaCRrIHPtJHJtz99_yiVxadZQyNVJfXYiQAIGu-95x5yTOIaEBDzLaQ&_nc_zt=14&_nc_ht=scontent-lga3-2.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_AfxzebLXIG_Ee-xIdHKsPlThaTNAyDKAEJgjEStmsXWvUw&oe=69ABF50D",
        "title": "Adidas designed 2 move 3-stripes tişört",
        "watermarked_resized_image_url": ""
      }
    ],
    "cta_text": "Shop now",
    "cta_type": "SHOP_NOW",
    "display_format": "DPA",
    "ec_certificates": [],
    "extra_images": [],
    "extra_links": [],
    "extra_texts": [],
    "extra_videos": [],
    "images": [],
    "is_reshared": false,
    "link_url": "https://www.trendyol.com/magaza/adidas-m-61?sst=0",
    "page_categories": [
      "Product/service"
    ],
    "page_id": "182162001806727",
    "page_is_deleted": false,
    "page_like_count": 43273726,
    "page_name": "adidas",
    "page_profile_picture_url": "https://scontent-lga3-2.xx.fbcdn.net/v/t39.35426-6/459071284_1254658215954912_4868907127556146219_n.jpg?stp=dst-jpg_s60x60_tt6&_nc_cat=101&ccb=1-7&_nc_sid=c53f8f&_nc_ohc=fVDpgdljow4Q7kNvwEB-tLz&_nc_oc=Adk0COH7p4c27OrmXiBDElb-FJ-dn4tkkeeT_Lw2ovNPcEcUL67Z5lAHXrUlg976nnw&_nc_zt=14&_nc_ht=scontent-lga3-2.xx&_nc_gid=XmasJEZWfRl9bm_b6ODIlA&_nc_ss=8&oh=00_AfwZe-rdF6dR1JTKPxt63gmij5FOJgki_HEspGAXydOJsQ&oe=69ABCAE3",
    "page_profile_uri": "https://www.facebook.com/adidas/",
    "title": "{{product.name}}",
    "videos": []
  },
  "start_date": 1730880000,
  "targeted_or_reached_countries": [],
  "transparency_by_location": {
    "eu_transparency": {
      "age_country_gender_reach_breakdown": [
        {
          "age_gender_breakdowns": [
            {
              "age_range": "45-54",
              "female": 2,
              "male": 2
            },
            {
              "age_range": "35-44",
              "female": 1,
              "male": 1
            }
          ],
          "country": "IT"
        },
        {
          "age_gender_breakdowns": [
            {
              "age_range": "55-64",
              "male": 2
            },
            {
              "age_range": "45-54",
              "male": 2
            },
            {
              "age_range": "25-34",
              "female": 1,
              "male": 1
            },
            {
              "age_range": "35-44",
              "female": 1
            }
          ],
          "country": "DE"
        }
      ],
      "eu_total_reach": 13,
      "gender_audience": "All",
      "location_audience": [],
      "targets_eu": false
    }
  },
  "violation_types": []
}
```

### Contact 📬

**Need a custom solution? Have a feature request or just want to chat?**\
We'd love to hear from you!

- 💬 **Discord**: `@azzouzana`
- 📧 **Email**: <labs@azzouzana.com>

### Keywords

Facebook Ads Scraper, Meta Ads Library, Competitor Analysis, Marketing Data, Ad Intelligence, Facebook Page ID, Meta Ad Metrics, Real Estate Ads, E-commerce Trends.

# Actor input Schema

## `startUrl` (type: `string`):

Either a Facebook Ads Library search URL (https://www.facebook.com/ads/library/?...) or a Facebook Page URL (https://www.facebook.com/PageName).

## `extractDetails` (type: `boolean`):

Whether to fetch deep ad details (including reach, spend, impressions, etc.)

## `maxAds` (type: `integer`):

Maximum number of ads to scrape.

## Actor input object example

```json
{
  "startUrl": "https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=FR&is_targeted_country=false&media_type=all&q=cars",
  "extractDetails": false,
  "maxAds": 2000
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
    "startUrl": "https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=FR&is_targeted_country=false&media_type=all&q=cars",
    "maxAds": 2000
};

// Run the Actor and wait for it to finish
const run = await client.actor("azzouzana/meta-facebook-instagram-ads-library").call(input);

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
    "startUrl": "https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=FR&is_targeted_country=false&media_type=all&q=cars",
    "maxAds": 2000,
}

# Run the Actor and wait for it to finish
run = client.actor("azzouzana/meta-facebook-instagram-ads-library").call(run_input=run_input)

# Fetch and print Actor results from the run's dataset (if there are any)
print("💾 Check your data here: https://console.apify.com/storage/datasets/" + run["defaultDatasetId"])
for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)

# 📚 Want to learn more 📖? Go to → https://docs.apify.com/api/client/python/docs/quick-start

```

## CLI example

```bash
echo '{
  "startUrl": "https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=FR&is_targeted_country=false&media_type=all&q=cars",
  "maxAds": 2000
}' |
apify call azzouzana/meta-facebook-instagram-ads-library --silent --output-dataset

```

## MCP server setup

```json
{
    "mcpServers": {
        "apify": {
            "command": "npx",
            "args": [
                "mcp-remote",
                "https://mcp.apify.com/?tools=azzouzana/meta-facebook-instagram-ads-library",
                "--header",
                "Authorization: Bearer <YOUR_API_TOKEN>"
            ]
        }
    }
}

```
