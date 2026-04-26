# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Data-only repository. No build system, no dependencies, no tests. Contains locale-specific JSON sample data consumed by the [EasyCommerce FakerPress](https://github.com/mralaminahamed/easycommerce-fakerpress) plugin at runtime.

The plugin downloads this repo on activation and loads files via `Generator::load_json_file()` using path pattern:
```
{sample_data_dir}/{category}/{locale}/{filename}.json
```
Falls back to `en_US` if the requested locale directory is absent.

## Repository Structure

3 categories × 75 locales = ~225 directories. Each category has a fixed set of JSON files:

| Category | Files |
|---|---|
| `customers/` | `countries.json`, `currencies.json`, `customer_tags.json`, `phone_patterns.json`, `postcode_patterns.json`, `preferred_categories.json`, `preferred_languages.json`, `states_provinces.json` |
| `orders/` | `fulfillment_statuses.json`, `order_statuses.json`, `payment_methods.json`, `shipping_methods.json`, `sources.json`, `weighted_countries.json` |
| `products/` | `adjectives.json`, `brands.json`, `categories.json`, `digital_attributes.json`, `digital_products.json`, `physical_attributes.json`, `physical_products.json`, `tags.json` |

## Data Formats

Two formats in use:

**Weighted dict** — used for random weighted selection (keys = values, numbers = weights):
```json
{ "pending": 25, "processing": 35, "completed": 30 }
```

**Simple array** — used for `randomElement()` picks:
```json
["stripe", "paypal", "bank"]
```

**Object dict** — used when generator needs structured config per entry:
```json
{
  "standard": { "min": 5.99, "max": 12.99, "days": "5-7", "weight": 50 }
}
```

## EasyCommerce Enum Values

Status/type fields must match these exact values from the EasyCommerce plugin (machine keys, always English regardless of locale):

| Field | Valid values |
|---|---|
| Order status | `pending`, `processing`, `completed`, `cancelled`, `on_hold`, `partially_refunded`, `refunded` |
| Fulfillment status | `unfulfilled`, `fulfilled`, `partially_fulfilled`, `shipped`, `delivered`, `returned` |
| Payment methods | `stripe`, `paypal`, `cash-on-delivery`, `bank`, `square`, `braintree`, `mollie`, `paddle` |

All enum keys must stay English even in non-English locales — these values go directly into the database.

## Adding or Updating a Locale

1. Copy an existing locale directory (use `en_US` as template)
2. Replace string values with locale-appropriate content
3. Keep all status/enum keys in English (see table above)
4. Keep JSON structure identical — generators expect exact keys
5. 2-space indent, LF line endings, trailing newline

To add a locale across all categories at once (bash):
```bash
NEW_LOCALE="xx_XX"
BASE="/path/to/easycommerce-fakerpress-sample-data"
for cat in customers orders products; do
  cp -r "$BASE/$cat/en_US" "$BASE/$cat/$NEW_LOCALE"
done
```

## Which Files Are Consumed

All three categories are fully loaded by generators at runtime:

- **`orders/*`** — all 6 files loaded by `Order` generator (`load_sample_data()`)
- **`products/*`** — all 8 files loaded by `Product` generator
- **`customers/*`** — all 8 files loaded by `Customer` generator

## Validation

No automated validator. Manually verify JSON is valid:
```bash
find . -name "*.json" | while read f; do python3 -m json.tool "$f" > /dev/null || echo "INVALID: $f"; done
```

Check a specific locale is complete (has same file count as en_US):
```bash
LOCALE="de_DE"
for cat in customers orders products; do
  expected=$(ls ./$cat/en_US/ | wc -l)
  actual=$(ls ./$cat/$LOCALE/ 2>/dev/null | wc -l)
  [ "$expected" != "$actual" ] && echo "MISSING in $cat/$LOCALE (has $actual, expected $expected)"
done
```
