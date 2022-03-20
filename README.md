Example of NEAR Wallet integration
==================================

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/near-examples/wallet-example)

<!-- MAGIC COMMENT: DO NOT DELETE! Everything above this line is hidden on NEAR Examples page -->

This example demonstrates how to integrate your application with NEAR Wallet.
The contract is quite simple. It can store the account_id of last sender and return it. It also shows how you can debug contracts using logs.

## Getting started

There are two ways to run this project. The first is the quick and a good way to instantly become familiar with this example.
Once familiar, the next step is for a developer to create their own NEAR account and deploy the contract to testnet. This is covered in the following section.

There's a button at the top of this file that says "Open in Gitpod." This will open the project in a new tab with an integrated development environment. The other option is to clone this repository and follow the same instructions.

### Quickest option

1. Install dependencies:

```
yarn --frozen-lockfile
```

2. Build and deploy this smart contract to a development account. This development account will be created automatically and is not intended for reuse:

```
yarn dev
```

Your command line which will display a link to localhost similar to:
```bash
Server running at http://localhost:1234
```

Please open that link your browser to continue and see how to log in with NEAR Wallet in a simple webapp.

### Standard deploy option
In this second option, the smart contract will get deployed to a specific account created with the NEAR Wallet.

1. Ensure `near-cli` is installed by running:

```
near --version
```

If needed, install `near-cli`:

```
npm install near-cli -g
```

2. If you do not have a NEAR account, please create one with [NEAR Wallet](wallet.testnet.near.org).

In the project root, login with `near-cli` by following the instructions after this command:

```
near login
```

3. Modify the top of `src/config.js`, changing the `CONTRACT_NAME` to be the NEAR account that was just used to log in.

```javascript
…
const CONTRACT_NAME = process.env.CONTRACT_NAME || 'YOUR_ACCOUNT_NAME_HERE'; /* TODO: fill this in! */
…
```

4. Start the example!

```
yarn start
```

## To Test

```
yarn asp // as-pect tests
yarn jest // integration tests
yarn test // both
```

## To Explore

- `assembly/main.ts` for the contract code
- `src/index.html` for the front-end HTML
- `src/main.js` for the JavaScript front-end code and how to integrate contracts
- `src/test.js` for the JS tests for the contract


## Data collection
By using Gitpod in this project, you agree to opt-in to basic, anonymous analytics. No personal information is transmitted. Instead, these usage statistics aid in discovering potential bugs and user flow information.
