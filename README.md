# vlt-client

[![Build Status](https://travis-ci.com/aliaspayments/vlt-client.svg?token=kLayivNQVqi3WiCnBo9X&branch=master)](https://travis-ci.com/aliaspayments/vlt-client)

## Usage

```typescript
const client = new VltClient({
  apiKey: 'abc123',
	apiSecret: 'abc1234',
	apiUrl: 'http://localhost:3000'
});

// List gateways
await client.gateways.list();

// Create gateway
await client.gateways.create({
	name: "My Gateway",
	type: "global_transport",
	credentials: {
		username: 'abc123',
		password: 'abc123'
	}
});

// Update gateway
await client.gateways.update('59ef868c138285143d48c7f1', { name: 'my gateway' });

// Redact gateway
await client.gateways.redact('59ef868c138285143d48c7f1');
```
