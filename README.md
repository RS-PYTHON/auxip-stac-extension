# AUXIP Extension Specification

- **Title:** AUXIP
- **Identifier:** <https://home.rs-python.eu/auxip-stac-extension/v1.1.0/schema.json>
- **Field Name Prefix:** auxip
- **Scope:** Item
- **Extension [Maturity Classification](https://github.com/radiantearth/stac-spec/tree/master/extensions/README.md#extension-maturity):** Pilot
- **Owner**: @vprivat-ads

This document explains the AUXIP Extension to the [SpatioTemporal Asset Catalog](https://github.com/radiantearth/stac-spec) (STAC) specification.
Allows to describe Copernicus auxiliary files from ADGS as STAC items.

- Examples:
  - [Item example](examples/item.json): Shows the basic usage of the extension in a STAC Item
- [JSON Schema](json-schema/schema.json)
- [Changelog](./CHANGELOG.md)

## Fields

The fields in the table below can be used in these parts of STAC documents:

- [ ] Catalogs
- [ ] Collections
- [x] Item Properties (incl. Summaries in Collections)
- [ ] Assets (for both Collections and Items, incl. Item Asset Definitions in Collections)
- [ ] Links

| Field Name           | Type          | Description                                                   |
| -------------------- | ------------- | ------------------------------------------------------------- |
| auxip:id             | string (uuid) | **REQUIRED**. UUID for the product instance within the AUXIP. |

### Additional Field Information

#### auxip:id

Universally unique identifier (UUID).
The Id is a local identifier for the product instance within the AUXIP, assigned by the service managing the AUXIP.

## Contributing

All contributions are subject to the
[STAC Specification Code of Conduct](https://github.com/radiantearth/stac-spec/blob/master/CODE_OF_CONDUCT.md).
For contributions, please follow the
[STAC specification contributing guide](https://github.com/radiantearth/stac-spec/blob/master/CONTRIBUTING.md) Instructions
for running tests are copied here for convenience.

### Running tests

The same checks that run as checks on PR's are part of the repository and can be run locally to verify that changes are valid. 
To run tests locally, you'll need `npm`, which is a standard part of any [node.js installation](https://nodejs.org/en/download/).

First you'll need to install everything with npm once. Just navigate to the root of this repository and on 
your command line run:
```bash
npm install
```

Then to check markdown formatting and test the examples against the JSON schema, you can run:
```bash
npm test
```

This will spit out the same texts that you see online, and you can then go and fix your markdown or examples.

If the tests reveal formatting problems with the examples, you can fix them with:
```bash
npm run format-examples
```

---

![](docs/images/banner_logo.jpg)

This project is funded by the EU and ESA.
