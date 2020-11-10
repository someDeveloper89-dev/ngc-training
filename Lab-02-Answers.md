# Lab-02 Answers

1. The required body parameters to create an App Environment are: 

```json
{
    "app_short_code": <APP_SHORT_CODE>,
    "u_alias": <ALIAS_NAME>,
    "u_hosting_location": <HOSTING_LOCATION>,
    "u_environments": "Development",
    "u_data_classification": "internal",
    "cost_center": <COST_CENTER>,
    "workload_admins": <WORKLOAD_ADMIN_EMAIL_ID>,
    "u_app_env_admins": <APP_ENV_ADMIN_EMAIL_ID>,
    "azure_services_required": true,
    "cyberark_safe_required": false,
    "onead_ou_required": false,
    "onead_sa_required": false,
    "tfe_required": true,
    "u_persona": "co-managed",
    "app_account_required": false,
    "sql_account_required": false,
    "gpo_admin_required": "No",
    "organization": <TFE_ORGANIZATION>,
    "tfe_team_members": <TFE_TEAM_MEMBERS>,
    "requested_for": <REQUESTED_FOR_MEMBER_MAIL_ID>,
    "vnet_name":<VNET_NAME>,
    "portal_users": <PORTAL_USER_MAIL_ID>,
    "subscription": <AZURE_SUBSCRIPTION_ID>,
    "tfe_workspaces": [
        {
            "workspace_purpose": "app",
            "workspace_suffix": "app"
        }
    ]
}
```

2. Creating a postman request to create App Environment

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/pwc_nextgen_request/provision_environment 
 
**Required Header:**
- Proxy-Authorization
- apikey
- apikeysecret
- Authorization
- Content-Type

**Request Body:**
```json
{
    "app_short_code": "SB001",
    "u_alias": "ngc-cli-training-robin",
    "u_hosting_location": "eastus",
    "u_environments": "Development",
    "u_data_classification": "internal",
    "cost_center": "{{costCenter}}",
    "workload_admins": "{{requested_for_email}}",
    "u_app_env_admins": "{{requested_for_email}}",
    "azure_services_required": true,
    "cyberark_safe_required": false,
    "onead_ou_required": false,
    "onead_sa_required": false,
    "tfe_required": true,
    "u_persona": "co-managed",
    "app_account_required": false,
    "sql_account_required": false,
    "gpo_admin_required": "No",
    "organization": "Sandbox-Service",
    "tfe_team_members": "{{requested_for_email}}",
    "requested_for": "eric.h.hernandez@pwc.com",
    "vnet_name": "PZI-GXUS-N-VNT-D040",
    "portal_users": "{{requested_for_email}}",
    "subscription": "PZI-GXUS-N-SUB040",
    "tfe_workspaces": [
        {
            "workspace_purpose": "app",
            "workspace_suffix": "app"
        }
    ]
}
```
**Sample Response :**
```json
{
    "result": {
        "status": "success",
        "message": "Requested Item created: RITM3216952",
        "record": "RITM3216952",
        "sysid": "8b4738f21bc4e410060e4002cd4bcbd1",
        "ciID": "0c57f8321b0060d0597d21b4bd4bcb2e",
        "ciCode": "SB001-DEV075",
        "ciName": "Sandbox Service001 - Azure US East (Development D075)"
    }
}
```
