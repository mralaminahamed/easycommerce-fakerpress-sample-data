# AGENTS.md - EasyCommerce FakerPress Sample Data

## Build/Lint/Test Commands

This is a data-only repository containing JSON sample data files. No build, lint, or test commands are applicable.

## Code Style Guidelines

### JSON Formatting
- Use 2-space indentation for all JSON files
- Arrays should be formatted with each item on a new line
- Simple string arrays: `["Item 1", "Item 2", "Item 3"]`
- Object arrays: Follow consistent property ordering
- Validate JSON syntax before committing

### Data Structure Conventions
- All data files are JSON arrays
- Simple arrays contain strings for basic lists (adjectives, categories, etc.)
- Complex data uses objects with consistent property names
- Locale-specific data follows the same structure across all locales
- File naming: lowercase_with_underscores.json

### WooCommerce Integration
- Always use `wc_get_template*` functions to load templates
- Never create custom classes or functions for template loading
- Always use `wc_get_template` first, never use classes like `@includes/Core/TemplateRenderer.php`

### File Organization
- Data organized by category (products, customers, orders, etc.)
- Each category has subdirectories for each supported locale
- Locale codes follow WordPress standards (en_US, de_DE, etc.)
- Consistent file naming across all locales within a category

### Error Handling
- JSON files must be valid and parseable
- Missing locale data falls back to en_US
- Data integrity is critical for plugin functionality

### Naming Conventions
- Use descriptive, lowercase filenames with underscores
- Locale directories use standard WordPress locale codes
- Property names in objects use camelCase or snake_case consistently within files