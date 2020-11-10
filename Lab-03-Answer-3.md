# Lab-03 Answer:
#  3. Create a postman request to Get environment details .

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/pwc_nextgen_request/environment_details?environment_id=SB001-DEV075

**Request Type:** GET
 
**Required Header:**
- Proxy-Authorization
- apikey
- apikeysecret
- Authorization
- Content-Type

**Request Parameter:**
| Key | Value |
|-----|-----|
|environment_id|SB001-DEV075|

**Response :**
```json
{
    {
    "result": {
        "environment_id": "SB001-DEV075",
        "environment_name": "Sandbox Service001 - Azure US East (Development D075)",
        "environment_alias": "ngc-cli-training-robin",
        "environment_hosting_region": "eastus",
        "environment_apptio": "globalnis645",
        "environment_release_group": "Sandbox Service001 Support R & D Group ",
        "environment_variant": "",
        "environment_type": "Development",
        "environment_resource_groups": "PZI-GXU2-N-RGP-SB001-D053",
        "resources": [
            "{\"name\":\"US - IFS - SB001-DEV075\",\"resource_type\":\"ServiceNow Group\",\"status\":\"not_discoverable\",\"ci_id\":\"\"}",
            "{\"name\":\"PZI-GXU2-N-RGP-SB001-D053\",\"resource_type\":\"Workload Resource Group\",\"status\":\"discovered\",\"ci_id\":\"6fb9f4fe1bc4a0d0db3554207e4bcbe3\"}"
        ],
        "cyberark_details": {
            "SafeName": "",
            "CyberArkCPMName": "Passwv05_West_01",
            "CyberArkPlatformPolicyWin": "GL_AZ_US2_Win_Local_Accs",
            "CyberArkPlatformPolicyLinux": "GL_AZ_US2_UNIX_Local_Accs",
            "CyberArkBuiltInAdminSafeName": "GLSRVW_BLT_AZUMEM_US2",
            "CyberArkLinuxBuiltInAdminSafeName": "GLSRVU_BLT_AZUMEM_US2",
            "cyberark_safe_group": ""
        },
        "related_cis": [
            {
                "name": "PZI-GXUS-N-VNT-D040",
                "class_name": null
            },
            {
                "name": "Azure US East",
                "class_name": null
            },
            {
                "name": "PZI-GXU2-N-RGP-SB001-D053",
                "class_name": null
            }
        ],
        "environment_details": {
            "user_parameters": {},
            "system_parameters": {
                "APPLICATION_ENVIRONMENT_ADMINISTRATORS": "ehendricks004,cyoung070,ehernandez123,rbudhatoki001",
                "AZURE_READONLY_USERS": "erik.hendrickson@pwc.com,robin.budhathoki@pwc.com,eric.h.hernandez@pwc.com,constant.young@pwc.com",
                "AZURE_SUBSCRIPTION": "PZI-GXUS-N-SUB040",
                "AZURE_SUBSCRIPTION_ID": "4bd68fef-3353-4f87-8d7c-205fc4196e5f",
                "GHS_TARIFF": "zcm",
                "PERSONA": "developer",
                "SRID": "RITM3216952",
                "STORAGE_TYPE": "Managed Disks",
                "TAGS": {
                    "ghs-los": "Internal Firm Services",
                    "ghs-solution": "Sandbox Service001",
                    "ghs-appid": "SB001",
                    "ghs-solutionexposure": "PwC Internal",
                    "ghs-serviceoffering": "",
                    "ghs-environment": "ngc-cli-training-robin",
                    "ghs-owner": "Constant Young",
                    "ghs-apptioid": "globalnis645",
                    "ghs-envid": "SB001-DEV075",
                    "ghs-tariff": "zcm",
                    "ghs-srid": "RITM3216952",
                    "ghs-environmenttype": "Development",
                    "ghs-deployedby": "portal",
                    "ghs-dataclassification": "",
                    "ghs-reserved1": "",
                    "ghs-reserved2": "",
                    "ghs-reserved3": "",
                    "ghs-reserved4": "",
                    "ghs-reserved5": "",
                    "ghs-udt1": "",
                    "ghs-udt2": ""
                },
                "TFE_ADMIN_GROUP": "tfe-sandbox-service-sb001-dev075-project",
                "TFE_TEAM": {
                    "team_name": "tfe-sandbox-service-sb001-dev075-project",
                    "team_id": "team-mSE3z21feWtXk3Nj",
                    "team_org": "Sandbox-Service",
                    "team_instance": "https://global.tfe.pwcinternal.com"
                },
                "TFE_WORKSPACE": {
                    "workspace_name": "sandbox-service-sb001-dev075-app",
                    "workspace_id": "ws-R3q5pestWT1V6brm",
                    "workspace_org": "Sandbox-Service",
                    "workspace_instance": "https://global.tfe.pwcinternal.com"
                },
                "TFE_WORKSPACE_ADMINS": "ehendricks004,cyoung070,ehernandez123,rbudhatoki001",
                "VAULT_NAMESPACE": "sandbox/ifs/sb001/sb001-dev075",
                "VAULT_ROLE_NAME": "TFE-SB001-DEV075",
                "VAULT_URL ": "",
                "VNET": "PZI-GXUS-N-VNT-D040",
                "WORKLOAD_AD": "One AD",
                "WORKLOAD_ADMINS": "ehendricks004,cyoung070,ehernandez123,rbudhatoki001"
            }
        },
        "subnets": []
    }
}
}
```