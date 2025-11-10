# EasyCommerce FakerPress Sample Data

This repository contains locale-specific sample data for the EasyCommerce FakerPress WordPress plugin. The data is automatically downloaded by the plugin during activation and provides realistic test data for various e-commerce entities.

## Structure

The repository is organized by data type and locale:

```
easycommerce-fakerpress-sample-data/
├── cart_sessions/          # Cart session data by locale
├── customers/              # Customer data by locale
├── locations/              # Geographic location data by locale
├── orders/                 # Order-related data by locale
├── products/               # Product data by locale
├── product_variations/     # Product variation data by locale
├── shipping_plans/         # Shipping plan data by locale
└── tax_classes/            # Tax class data by locale
```

## Supported Locales

The following locales are supported with varying levels of completeness:

- `ar_SA` - Arabic (Saudi Arabia)
- `at_AT` - Austrian German
- `bg_BG` - Bulgarian (Bulgaria)
- `bn_BD` - Bangla (Bangladesh)
- `cs_CZ` - Czech (Czech Republic)
- `da_DK` - Danish (Denmark)
- `de_AT` - German (Austria)
- `de_CH` - German (Switzerland)
- `de_DE` - German (Germany)
- `el_CY` - Greek (Cyprus)
- `el_GR` - Greek (Greece)
- `en_AU` - English (Australia)
- `en_GB` - English (Great Britain)
- `en_HK` - English (Hong Kong)
- `en_IN` - English (India)
- `en_NG` - English (Nigeria)
- `en_NZ` - English (New Zealand)
- `en_PH` - English (Philippines)
- `en_SG` - English (Singapore)
- `en_UG` - English (Uganda)
- `en_US` - English (United States)
- `en_ZA` - English (South Africa)
- `es_AR` - Spanish (Argentina)
- `es_ES` - Spanish (Spain)
- `es_PE` - Spanish (Peru)
- `es_VE` - Spanish (Venezuela)
- `et_EE` - Estonian (Estonia)
- `fa_IR` - Persian (Iran)
- `fi_FI` - Finnish (Finland)
- `fr_BE` - French (Belgium)
- `fr_CA` - French (Canada)
- `fr_CH` - French (Switzerland)
- `fr_FR` - French (France)
- `he_IL` - Hebrew (Israel)
- `hi_IN` - Hindi (India)
- `hr_HR` - Croatian (Croatia)
- `hu_HU` - Hungarian (Hungary)
- `hy_AM` - Armenian (Armenia)
- `id_ID` - Indonesian (Indonesia)
- `is_IS` - Icelandic (Iceland)
- `it_CH` - Italian (Switzerland)
- `it_IT` - Italian (Italy)
- `ja_JP` - Japanese (Japan)
- `ka_GE` - Georgian (Georgia)
- `kk_KZ` - Kazakh (Kazakhstan)
- `ko_KR` - Korean (South Korea)
- `lt_LT` - Lithuanian (Lithuania)
- `lv_LV` - Latvian (Latvia)
- `me_ME` - Montenegrin (Montenegro)
- `mn_MN` - Mongolian (Mongolia)
- `ms_MY` - Malay (Malaysia)
- `nb_NO` - Norwegian Bokmål (Norway)
- `ne_NP` - Nepali (Nepal)
- `nl_BE` - Dutch (Belgium)
- `nl_NL` - Dutch (Netherlands)
- `pl_PL` - Polish (Poland)
- `pt_AO` - Portuguese (Angola)
- `pt_BR` - Portuguese (Brazil)
- `pt_PT` - Portuguese (Portugal)
- `ro_MD` - Romanian (Moldova)
- `ro_RO` - Romanian (Romania)
- `ru_RU` - Russian (Russia)
- `sk_SK` - Slovak (Slovakia)
- `sl_SI` - Slovenian (Slovenia)
- `sr_Cyrl_RS` - Serbian Cyrillic (Serbia)
- `sr_Latn_RS` - Serbian Latin (Serbia)
- `sr_RS` - Serbian (Serbia)
- `sv_SE` - Swedish (Sweden)
- `th_TH` - Thai (Thailand)
- `tr_TR` - Turkish (Turkey)
- `uk_UA` - Ukrainian (Ukraine)
- `vi_VN` - Vietnamese (Vietnam)
- `zh_CN` - Chinese (China)
- `zh_TW` - Chinese (Taiwan)

## Data Types

### Cart Sessions
- `session_states.json` - Cart session states and statuses

### Customers
- `countries.json` - Country names and codes
- `currencies.json` - Currency codes and symbols
- `customer_tags.json` - Customer tag names
- `phone_patterns.json` - Phone number patterns
- `postcode_patterns.json` - Postal code patterns
- `preferred_categories.json` - Preferred product categories
- `preferred_languages.json` - Preferred languages
- `states_provinces.json` - State/province names

### Locations
- `countries.json` - Country information
- `state_names.json` - State/province names
- `timezone_configs.json` - Timezone configurations

### Orders
- `fulfillment_statuses.json` - Order fulfillment statuses
- `order_statuses.json` - Order statuses
- `payment_methods.json` - Payment method names
- `shipping_methods.json` - Shipping method names
- `sources.json` - Order source channels
- `weighted_countries.json` - Countries with weightings for realistic distribution

### Products
- `adjectives.json` - Product name adjectives
- `brands.json` - Brand names
- `categories.json` - Product category names
- `digital_attributes.json` - Digital product attributes
- `digital_products.json` - Digital product names
- `physical_attributes.json` - Physical product attributes
- `physical_products.json` - Physical product names
- `tags.json` - Product tag names

### Product Variations
- `variation_attributes.json` - Product variation attributes
- `variation_values.json` - Product variation values

### Shipping Plans
- `plan_types.json` - Shipping plan types

### Tax Classes
- `tax_types.json` - Tax class types

## Usage

This repository is automatically used by the EasyCommerce FakerPress plugin. The plugin downloads this data during activation and stores it in the WordPress uploads directory at `wp-content/uploads/easycommerce-fakerpress-sample-data/`.

The data is loaded based on the current WordPress locale setting and provides realistic, locale-appropriate test data for e-commerce development and testing.

## Contributing

To add support for new locales or update existing data:

1. Create a new directory for the locale (e.g., `fr_CA/` for Canadian French)
2. Add the appropriate JSON files following the existing structure
3. Ensure data is realistic and culturally appropriate
4. Test with the EasyCommerce FakerPress plugin

## File Format

All data files are JSON arrays containing strings or objects appropriate to their purpose. For example:

```json
["Item 1", "Item 2", "Item 3"]
```

or

```json
[
  {"name": "Item 1", "code": "CODE1"},
  {"name": "Item 2", "code": "CODE2"}
]
```

## Statistics

- **Total files**: 2,442 JSON files
- **Total lines**: 57,063+ lines of data
- **Supported locales**: 76+ locales
- **Data categories**: 8 main categories

## License

This sample data repository is part of the EasyCommerce FakerPress plugin and follows the same GPL-2.0-or-later license.