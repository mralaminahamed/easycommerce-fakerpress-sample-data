# EasyCommerce FakerPress Sample Data

[![GitHub Repository](https://img.shields.io/badge/GitHub-Repository-blue.svg)](https://github.com/mralaminahamed/easycommerce-fakerpress-sample-data)
[![License](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](http://www.gnu.org/licenses/gpl-2.0.txt)
[![Main Plugin](https://img.shields.io/badge/Main_Plugin-EasyCommerce%20FakerPress-orange.svg)](https://github.com/mralaminahamed/easycommerce-fakerpress)

This repository contains locale-specific sample data for the **[EasyCommerce FakerPress](https://github.com/mralaminahamed/easycommerce-fakerpress)** WordPress plugin. The data is automatically downloaded by the plugin during activation and provides realistic test data for various e-commerce entities across 76+ locales.

**🔗 Related Repository**: [EasyCommerce FakerPress Main Plugin](https://github.com/mralaminahamed/easycommerce-fakerpress)

## 📋 Overview

This repository serves as the **data backbone** for EasyCommerce FakerPress, providing:

- **🌍 76+ Locales**: Comprehensive international support
- **📊 2,442 JSON Files**: Extensive data coverage
- **🏪 E-commerce Focus**: Specialized data for online stores
- **🔄 Auto-sync**: Automatically downloaded by the main plugin
- **🎯 Realistic Data**: Culturally appropriate and business-relevant content

## 🏗️ Architecture

### Repository Relationship

```
EasyCommerce FakerPress (Main Plugin)
├── Core Plugin Code
├── Admin Interface (React)
├── REST API Controllers
└── Sample Data Integration → Downloads from this repository
    ├── Automatic Download on Activation
    ├── wp-content/uploads/easycommerce-fakerpress-sample-data/
    └── Locale-based Data Loading
```

### Data Flow

1. **Plugin Activation** → Downloads sample data ZIP from GitHub
2. **Data Extraction** → Extracts to WordPress uploads directory
3. **Locale Detection** → Loads appropriate locale data
4. **Generator Usage** → Provides realistic test data for all generators

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

### Automatic Integration

This repository is automatically used by the **[EasyCommerce FakerPress](https://github.com/mralaminahamed/easycommerce-fakerpress)** plugin:

1. **Plugin Activation**: When you activate EasyCommerce FakerPress, it automatically downloads this sample data repository
2. **Data Storage**: Sample data is stored in `wp-content/uploads/easycommerce-fakerpress-sample-data/`
3. **Locale Detection**: Data is loaded based on your WordPress locale setting for culturally appropriate content
4. **Fallback Support**: If a specific locale isn't available, the plugin falls back to `en_US` data

### Manual Usage

If you need to use this data independently:

```php
// Load sample data for a specific locale
$sample_data = json_decode(file_get_contents('path/to/sample-data/products/en_US/adjectives.json'), true);
```

### Integration with Generators

The sample data powers all 10 generators in EasyCommerce FakerPress:

- **🛍️ Products**: Realistic product names, categories, and attributes
- **👥 Customers**: Localized customer data with regional preferences
- **📦 Orders**: Order statuses and payment methods by region
- **🎫 Coupons**: Discount codes and promotional content
- **📍 Locations**: Geographic data for shipping and billing
- **🚚 Shipping Plans**: Regional shipping options
- **💰 Transactions**: Payment processing data
- **🛒 Cart Sessions**: Shopping cart states
- **🏷️ Tax Classes**: Regional tax configurations
- **🔄 Product Variations**: Size, color, and attribute combinations

See the **[main plugin documentation](https://github.com/mralaminahamed/easycommerce-fakerpress/blob/main/docs/usage.md)** for detailed usage instructions.

## Contributing

We welcome contributions to expand locale support and improve data quality!

### Adding New Locales

1. **Fork** this repository
2. **Create** a new directory for the locale (e.g., `fr_CA/` for Canadian French)
3. **Add** the appropriate JSON files following the existing structure
4. **Ensure** data is realistic and culturally appropriate
5. **Test** with the [EasyCommerce FakerPress plugin](https://github.com/mralaminahamed/easycommerce-fakerpress)
6. **Submit** a pull request

### Data Guidelines

- **Cultural Accuracy**: Ensure data reflects local customs, naming conventions, and business practices
- **Realistic Values**: Use authentic product names, addresses, and terminology
- **Complete Coverage**: Provide data for all applicable categories (products, customers, orders, etc.)
- **JSON Format**: Follow the established JSON structure (see File Format section)

### Testing

Test your locale additions with the main plugin:

```bash
# In the main plugin directory
composer install
npm install && npm run build
# Activate plugin and test your new locale
```

### Related Resources

- **[Main Plugin Contributing Guide](https://github.com/mralaminahamed/easycommerce-fakerpress/blob/main/docs/development.md)**
- **[Plugin Issues](https://github.com/mralaminahamed/easycommerce-fakerpress/issues)**
- **[Data Format Standards](https://github.com/mralaminahamed/easycommerce-fakerpress/blob/main/docs/architecture.md)**

## 📊 Data Sources & Methodology

### Generation Approach

The sample data was generated using a combination of:

- **🤖 FakerPHP Library**: Core data generation with locale support
- **🌍 Cultural Research**: Region-specific business practices and naming conventions
- **📈 Real E-commerce Data**: Analysis of actual online store patterns
- **🎯 Business Logic**: Realistic pricing, categorization, and customer behavior patterns

### Quality Assurance

- **Cultural Accuracy**: Data reviewed for regional appropriateness
- **Business Relevance**: Focus on actual e-commerce use cases
- **Performance Optimized**: Efficient JSON structures for fast loading
- **Extensible Format**: Easy to add new locales and data types

### Data Categories Overview

Each data category serves specific generators in the main plugin:

| Category | Files/Locale | Primary Use | Example Generators |
|----------|-------------|-------------|-------------------|
| **Products** | 8 files | Product creation | Products, Variations |
| **Customers** | 8 files | User profiles | Customers, Orders |
| **Orders** | 6 files | Transaction data | Orders, Transactions |
| **Locations** | 3 files | Geographic info | Customers, Shipping |
| **Cart Sessions** | 1 file | Session states | Cart Sessions |
| **Shipping Plans** | 1 file | Delivery options | Shipping Plans |
| **Tax Classes** | 1 file | Tax configurations | Tax Classes |

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

### JSON Schema Examples

**Simple Array** (most common):
```json
{
  "type": "array",
  "items": {"type": "string"},
  "example": ["Wireless Headphones", "Bluetooth Speaker", "USB Cable"]
}
```

**Object Array** (for complex data):
```json
{
  "type": "array",
  "items": {
    "type": "object",
    "properties": {
      "name": {"type": "string"},
      "code": {"type": "string"},
      "weight": {"type": "number"}
    }
  },
  "example": [
    {"name": "Standard Shipping", "code": "standard", "weight": 1},
    {"name": "Express Delivery", "code": "express", "weight": 2}
  ]
}
```

## 📈 Statistics & Coverage

### Repository Metrics

- **📁 Total Files**: 2,442 JSON files
- **📝 Total Lines**: 57,063+ lines of structured data
- **🌍 Supported Locales**: 76+ international locales
- **📊 Data Categories**: 8 main e-commerce categories
- **💾 Compressed Size**: ~2.3MB (uncompressed: ~8.7MB)

### Locale Distribution

| Region | Locales | Coverage | Notes |
|--------|---------|----------|-------|
| **Europe** | 28 | 🇩🇪🇫🇷🇬🇧🇮🇹🇪🇸🇳🇱🇧🇪🇵🇱🇷🇺🇺🇦🇸🇪🇳🇴🇩🇰🇫🇮🇭🇷🇸🇰🇸🇮🇱🇹🇱🇻🇪🇪🇮🇸🇨🇿🇭🇺🇧🇬🇷🇴🇵🇹 | Comprehensive European coverage |
| **Americas** | 8 | 🇺🇸🇨🇦🇧🇷🇦🇷🇵🇪🇻🇪🇲🇽🇺🇾 | North & South American locales |
| **Asia** | 32 | 🇯🇵🇰🇷🇨🇳🇮🇳🇮🇩🇹🇭🇻🇳🇲🇾🇸🇬🇭🇰🇵🇭🇰🇦🇪🇹🇷🇮🇱🇦🇲🇬🇪🇰🇿🇲🇳🇳🇵🇧🇩 | Extensive Asian language support |
| **Africa** | 4 | 🇳🇬🇿🇦🇺🇬🇦🇴 | Growing African locale support |
| **Oceania** | 4 | 🇦🇺🇳🇿🇵🇬🇫🇯 | Pacific region coverage |

### Data Completeness by Category

| Category | Locales | Avg Files/Locale | Status |
|----------|---------|------------------|--------|
| **Products** | 76 | 8.0 | ✅ Complete |
| **Customers** | 76 | 8.0 | ✅ Complete |
| **Orders** | 76 | 6.0 | ✅ Complete |
| **Locations** | 76 | 3.0 | ✅ Complete |
| **Cart Sessions** | 76 | 1.0 | ✅ Complete |
| **Product Variations** | 76 | 2.0 | ✅ Complete |
| **Shipping Plans** | 7 | 1.0 | 🚧 Partial |
| **Tax Classes** | 2 | 1.0 | 🚧 Minimal |

### File Size Distribution

- **Small files** (< 1KB): 45% - Simple arrays and basic data
- **Medium files** (1-10KB): 40% - Standard product/customer data
- **Large files** (10-50KB): 12% - Comprehensive product catalogs
- **Extra large files** (> 50KB): 3% - Extensive locale-specific datasets

## License

This sample data repository is part of the EasyCommerce FakerPress plugin ecosystem and follows the same **GPL-2.0-or-later** license.

- **📄 License**: [GPL v2 or later](http://www.gnu.org/licenses/gpl-2.0.txt)
- **🔗 Main Plugin**: [EasyCommerce FakerPress](https://github.com/mralaminahamed/easycommerce-fakerpress)
- **📧 Author**: Al Amin Ahamed ([@mralaminahamed](https://github.com/mralaminahamed))

## Support & Resources

- **🐛 Bug Reports**: [Create an issue](https://github.com/mralaminahamed/easycommerce-fakerpress-sample-data/issues)
- **💡 Feature Requests**: [Plugin repository](https://github.com/mralaminahamed/easycommerce-fakerpress/issues)
- **📖 Documentation**: [Main plugin docs](https://github.com/mralaminahamed/easycommerce-fakerpress/tree/main/docs)
- **🤝 Contributing**: See [Contributing](#contributing) section above

---

**Part of the EasyCommerce FakerPress ecosystem** | **v1.0.0** | November 2025