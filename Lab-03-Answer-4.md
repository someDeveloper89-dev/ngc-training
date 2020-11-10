# Lab-03 Answer:
#  4. Create a postman request to Create config Params.

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/pwc_nextgen_request/create_params

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
    "environment_id": "{{environmentId}}",
    "params": {
        "administrator_login_password": "PsSqlus@123",
        "administrator_login_username" : "test-admin"
    }
}
```
**Response :**
```json
{
    "result": true
}
```