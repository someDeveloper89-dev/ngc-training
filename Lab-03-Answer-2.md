# Lab-03 Answer:
#  2. Create a postman request to Manage TFE Credentials.

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/pwc_nextgen_request/manage_tfe_credentials

**Request Type:** POST
 
**Required Header:**
- Proxy-Authorization
- apikey
- apikeysecret
- Authorization
- Content-Type

**Request Body:**
```json
{
  "requested_for": "{{requested_for_email}}",
  "environment_id": "{{environmentId}}"
}
```
**Response :**
```json
{
    "result": {
        "status": "success",
        "message": "Requested Item created: RITM3216967",
        "record": "RITM3216967",
        "sysid": "f23a29831b0ce410060e4002cd4bcb97"
    }
}
```