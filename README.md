# Swup Documentation

The `Swup` class allows interaction with the Swup API for managing currencies, balances, exchanges, and creating invoices. This class supports asynchronous requests to the API using `GET` and `POST` HTTP methods.

Documentation: [Postman](https://www.postman.com/swup-ai/workspace/swup/documentation/24821794-5c3fe268-1859-4608-a837-45df894ea620)

## Constructor

```javascript
const swup = new Swup(publicKey, privateKey, [locale]);
```
Parameters:

- `publicKey` (string): Your account's public key.
- `privateKey` (string): Your account's private key.
- `locale` (string, optional): Localization for the Accept-Language header. Default is 'en'.

## Usage Example:
```javascript
const swup = new Swup('publicKey', 'privateKey');
const currencies = await swup.currencies();
console.log(currencies);

const data = { /* invoice data */ };
const result = await swup.createInvoice(data);
console.log(result);
```
## Requirements

- Node.js version 14 or later.
- crypto module (included in Node.js standard library).
- node-fetch module for HTTP requests (can be added via npm: npm install node-fetch).