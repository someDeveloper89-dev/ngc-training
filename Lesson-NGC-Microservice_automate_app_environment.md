# Introduction 

In the lesson we will walk through different NGC Microservices available and how do we manage and automate the process of creating or maintaining of Application Environment, the configuration of Parameters, configure the resources name, etc using the Rest-API calls of NGC Microservices.

# About NGC-Microservice

The NGC-Microservice API allows developers and developer tools to make use of the various NextGen Cloud capabilities in ServiceNow via scripting. The API is REST-based and features validation to ensure all necessary attributes are provided and accurate.

---

> ## Automate the creation of an Application Environment using NGC Microservices

Automation of creating an Application Environment can be done in two ways, first one using Postman request and second one using ADO extensions, for this lesson we will checkout how to automate the process using Postman Request:
> **Using Postman Request**

This API is used to submit a Create Application Environment request which triggers a series of automation based on the options specified.

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
**Sample Response :**
```json
{
    "result": {
        "status": "success",
        "message": "Requested Item created: <SNOW_RITM_NO>",
        "record": <SNOW_RITM_NO>,
        "sysid": <SYS_ID>,
        "ciID": <CI_ID>,
        "ciCode": <APP_ENV_ID>, //APPLICATION  ENVIRONMENT ID
        "ciName": <APPLICATION ENVIRONMENT REFERENCE NAME >
    }
}
```