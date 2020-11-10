# Lab-03 Answer:
#  5. Create a postman request to Create Naming services for the following resources.

| Resource | Quantity |
|-------|-------:|
|Resource Group|2|
|Load Balancer|1|
|||

> ## **Generating Name for Resource Group, QTY-2**

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/naming_service

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
    "u_environment_id":"SB001-DEV075",
    "u_hosting_location": "eastus",
    "u_resource_type": "cmdb_ci_resource_group",
    "u_quantity": "2"
}
```
**Response :**
```json
{
    "result": {
        "naming_request": "NSR0005000",
        "ciNames": "PZI-GXU2-N-RGP-SB001-D054,PZI-GXU2-N-RGP-SB001-D055",
        "requests_submitted": "[]",
        "environment_id": "SB001-DEV075",
        "resource_type": "cmdb_ci_resource_group",
        "status": "success"
    }
}
```

> ## **Generating Name for Load Balancer, QTY-1**

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/naming_service

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
    "u_environment_id": "{{environmentId}}",
    "u_function": "Internal",
    "u_hosting_location": "eastus",
    "u_resource_type": "Cloud Load Balancer",
    "u_tier":"T2",
    "u_quantity": "1"
}

```
**Response :**
```json
{
    "result": {
        "naming_request": "NSR0005001",
        "ciNames": "U2ZSB001ILBT2D006",
        "requests_submitted": "[]",
        "environment_id": "SB001-DEV075",
        "resource_type": "Cloud Load Balancer",
        "status": "success"
    }
}
```
**Note:** The value of ***ciNames*** returns the name requested for the resource

