# Lab-03 Answer:
#  2. Create a postman request to RITM Status Check

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/pwc_nextgen_request/ritm_status_check

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
  "ritm_number": "RITM3212869"
}
```
**Response :**
```json
{
    "result": {
        "number": "RITM3212869",
        "stage": "fulfillment",
        "state": "Work in Progress",
        "state_code": "2"
    }
}
```