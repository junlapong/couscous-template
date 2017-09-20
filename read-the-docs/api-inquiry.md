---
currentMenu: inquiry
---
# INQUIRY

Inquiry registration status

### Endpoint

`{base_url}/kda-api/api/v1/inquiry`

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
	...
}
```

## Example
