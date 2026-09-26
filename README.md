#### [TusinskiDev] Countries Names
# td-countries-names

A lightweight TypeScript package that exports country and territory names as strongly typed constants. It is designed for apps that need a reliable list of country labels for forms, filters, selectors, validation, or sample data without pulling in a large dependency.

## Features

- Typed constants for country names such as `POLAND`, `UNITED_STATES`, and `GERMANY`
- `ALL_COUNTRIES` array for quick rendering of dropdowns and filters
- `CountryName` TypeScript type for safer input validation
- Zero runtime dependencies
- Works in TypeScript and JavaScript projects

## Installation

```bash
npm install td-countries-names
```

## Quick start

```ts
import {
  POLAND,
  UNITED_STATES,
  ALL_COUNTRIES,
  type CountryName,
} from 'td-countries-names';

const country: CountryName = POLAND;

const options = ALL_COUNTRIES.map((name) => ({
  label: name,
  value: name,
}));

console.log(country);
console.log(options.length);
```

## Use cases

This package is useful in many application scenarios:

- Country dropdowns and address forms
- Shipping and billing form validation
- Search filters and dynamic reporting dashboards
- Seed data and fixtures for tests and demos
- Data import and normalization workflows
- Selection lists in admin panels and CRM tools
- Country-based logic in onboarding and compliance flows

## API

The package exports named constants for each country, a complete `ALL_COUNTRIES` list, and a `CountryName` type.

### Main exports

- `ALL_COUNTRIES`: array of all supported country names
- `CountryName`: union type derived from the list
- Individual constants like `FRANCE`, `CANADA`, `JAPAN`, `BRAZIL`, `AUSTRALIA`

## Example: building a select list

```ts
import { ALL_COUNTRIES } from 'td-countries-names';

const countrySelectOptions = ALL_COUNTRIES.map((country) => ({
  value: country,
  label: country,
}));
```

## Why use this package?

If your application needs a compact, predictable list of country names, this library avoids repeated hand-written constants and keeps your codebase type-safe. It is especially useful when you want to generate UI options or validate user-provided country values consistently.

## License

MIT
