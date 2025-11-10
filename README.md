# EasyCommerce FakerPress Sample Data

[![License](https://img.shields.io/badge/license-GPLv2-blue.svg)](LICENSE.txt)  [![WordPress Compatibility](https://img.shields.io/badge/WordPress-%3E=5.8-blue.svg)]()

EasyCommerce FakerPress Sample Data provides locale-specific sample data for the EasyCommerce FakerPress WordPress plugin. This repository contains realistic test data for various e-commerce entities across 75+ locales, automatically downloaded during plugin activation.

## Features

- **75 Locales**: Comprehensive international support with culturally appropriate data
- **2,471 JSON Files**: Extensive data coverage for all e-commerce entities
- **Auto-sync**: Automatically downloaded by the EasyCommerce FakerPress plugin
- **Realistic Data**: Business-relevant content for testing and development
- **Modular Structure**: Organized by data type and locale for easy maintenance

## Why EasyCommerce FakerPress Sample Data?

- **Comprehensive Coverage**: Supports 76+ locales with complete e-commerce data sets
- **Automatic Integration**: Seamlessly integrates with the main FakerPress plugin
- **Performance Optimized**: Efficient JSON structures for fast loading and processing
- **Culturally Accurate**: Region-specific data reflecting local business practices
- **Extensible Format**: Easy to add new locales and data categories

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

## Getting Started

### Requirements
- **EasyCommerce FakerPress Plugin**: Main plugin must be installed and activated
- **WordPress**: Version 5.8 or higher

### Installation
1. The sample data is automatically downloaded when you activate EasyCommerce FakerPress
2. Data is stored in `wp-content/uploads/easycommerce-fakerpress-sample-data/`
3. The plugin automatically detects your WordPress locale and loads appropriate data

## Development Setup

### Data Structure
The repository is organized by data type and locale:

```
easycommerce-fakerpress-sample-data/
├── cart_sessions/     # Cart session data by locale
├── customers/         # Customer data by locale
├── locations/         # Geographic location data by locale
├── orders/            # Order-related data by locale
├── products/          # Product data by locale
├── product_variations/# Product variation data by locale
├── shipping_plans/    # Shipping plan data by locale
└── tax_classes/       # Tax class data by locale
```

### File Format
All data files are JSON arrays containing strings or objects:

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

## Contributing

We welcome contributions to expand locale support and improve data quality!

### Adding New Locales
1. Fork this repository
2. Create a new directory for the locale (e.g., `fr_CA/` for Canadian French)
3. Add the appropriate JSON files following the existing structure
4. Ensure data is realistic and culturally appropriate
5. Submit a pull request

### Data Guidelines
- Cultural Accuracy: Ensure data reflects local customs and business practices
- Realistic Values: Use authentic product names, addresses, and terminology
- JSON Format: Follow the established JSON structure with 2-space indentation

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

## License

EasyCommerce FakerPress Sample Data is licensed under the GNU General Public License v2.0. See the [LICENSE](LICENSE.txt) file for more details.

## Support & Resources

### Documentation
- **[Main Plugin Documentation](https://github.com/mralaminahamed/easycommerce-fakerpress/tree/main/docs)** - Complete usage guide
- **[Data Format Standards](https://github.com/mralaminahamed/easycommerce-fakerpress/blob/main/docs/architecture.md)** - Technical specifications
- **[Contributing Guide](https://github.com/mralaminahamed/easycommerce-fakerpress/blob/main/docs/development.md)** - Development guidelines

### Support Channels
- **🐛 Bug Reports**: [Create an issue](https://github.com/mralaminahamed/easycommerce-fakerpress-sample-data/issues)
- **💡 Feature Requests**: [Plugin repository](https://github.com/mralaminahamed/easycommerce-fakerpress/issues)
- **💬 Discussions**: [GitHub Discussions](https://github.com/mralaminahamed/easycommerce-fakerpress/discussions)

### Related Links
- **🔗 Main Plugin**: [EasyCommerce FakerPress](https://github.com/mralaminahamed/easycommerce-fakerpress)
- **📧 Author**: Al Amin Ahamed ([@mralaminahamed](https://github.com/mralaminahamed))
- **🏢 Organization**: [EasyCommerce Dev](https://github.com/easycommercedev)

---

Thank you for using EasyCommerce FakerPress Sample Data! 🚀