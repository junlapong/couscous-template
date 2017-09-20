---
currentMenu: topup
---
# TOPUP

Topup API

### Endpoint

`{base_url}/kda-api/api/v1/topup`

### Headers

Content-Type: `application/json`

### Body

```json
{
	"payeeCode" : "PYC",
	"param" : "{encrypted_msg}"
}
```

#### Param

`{encrypted_msg}` is message encrypted with `AES 256 CBC mode` by `secret_key`

```json
{
	"registerId" : "150408684476899",
	"referenceId" : "9876543210",
	"amount" : "999",
	"tramnsactionId" : "12345678",
	"transactionDate" : "2016-12-31T23:59:59Z"
}
```

## Example
### Request
```
curl -POST --url "https://int.krungsriepayment.com/kda-api/api/v1/topup" \
     -H "Content-Type: application/json" \
     -d '{ "payeeCode" : "PYC", "param" : "374a52ec57e7d8a237ccda7f86ee6b3097462930f2bff5c4464c2fd2f87a233bd9b80e4f7cf7c77ecdbd5734808d6cc40469074bd6b4b0625f1b3877d8f1a63c5eb9aa7c99ccca41dd634bca4319f75243448272f650daa5bf4f4e0a0be23fdd7b2032b15ae25444ce0b8eb68e93783e7db2444f9db4c2813fc18f461121ee00a542b1e082165159608f46d15b8cec995e08b2a4d8e50c0f3bf4800ec820ed45512b3e6d88a37d0e115b85c4ac13e04e2df05ff5336936693e930c4284248a021b0d1bacae18802f6d7d1d08f314aa6f42327ffa3e2a58acb9e5d1929bf4a22c" }'
```

### Response

```json
{
  "param" : "f65f939a558513314acff1ff220f9c827493e76da04573e23a756d8c86142c2657ebde62bde9a56252e398e9fe149edd8c8cee645844d1cf5c326492de2d5965"
}
```