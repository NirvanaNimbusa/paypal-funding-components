PayPal Funding Components
-------------------------

[![npm version](https://img.shields.io/npm/v/@paypal/funding-components.svg?style=flat-square)](https://www.npmjs.com/package/@paypal/funding-components) [![build status](https://img.shields.io/travis/paypal/paypal-funding-components/master.svg?style=flat-square)](https://travis-ci.org/paypal/paypal-funding-components)

[![dependencies Status](https://david-dm.org/paypal/paypal-funding-components/status.svg)](https://david-dm.org/paypal/paypal-funding-components) [![devDependencies Status](https://david-dm.org/paypal/paypal-funding-components/dev-status.svg)](https://david-dm.org/paypal/paypal-funding-components?type=dev)

PayPal JavaScript SDK module to deal with funding sources and eligibility.

## Remember a funding source from the client-side

Note: your client-id and domain must be approved to call this function

```javascript
paypal.rememberFunding([ paypal.FUNDING.VENMO ]);
```

## Remember a funding source from the server-side

```javascript
import { rememberFunding } from '@paypal/funding-components';
import { FUNDING } from '@paypal/sdk-constants';

rememberFunding(req, res, [ FUNDING.VENMO ]);
```

## Check a remembered funding source from the server-side

```javascript
import { isFundingRemembered } from '@paypal/funding-components';
import { FUNDING } from '@paypal/sdk-constants';

if (isFundingRemembered(req, FUNDING.VENMO)) {
    // ...
}
```

Pass in a custom set of cookies:

```javascript
isFundingRemembered(req, FUNDING.VENMO, { cookies })
```


Quick Start
-----------

#### Installing

```bash
npm install --save @paypal/funding-components
```

#### Getting Started

- Fork the module
- Run setup: `npm run setup`
- Start editing code in `./src` and writing tests in `./tests`
- `npm run build`

#### Building

```bash
npm run build
```

#### Tests

- Edit tests in `./test/tests`
- Run the tests:

  ```bash
  npm test
  ```
