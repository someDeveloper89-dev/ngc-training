# Introduction

The purpose of this lesson plan is to walk you through the five major NGC services that we use.

## The Five Big One we use are:

- Create App Environment
- Manage TFE Credentials
- Get environment details
- Create config Params
- Naming services

> # **Create App Environment**

## Purpose
This API is used to submit a Create Application Environment request which triggers a series of automations based on the options specified.

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/pwc_nextgen_request/provision_environment

**Request Type:** POST


**Parameters:** 
| Label(name) | Options | Description |
|-------|-------|-------|
|app_short_code|App Short Code of an Application CI|Specify the application short code of the application CI. |
|u_alias|Alias to be used for the Environment|Specify the alias name to be used for the application environment. Example : Testing API|
|u_hosting_location|Data centers paired with the hosting location of the protected environment. |The Data center’ alias for the new Recovery Environment.|
|u_environments|Development, Testing, Staging, Failover, Production |Specify the type of target environment where the application environment is being deployed.|
|u_data_classification|List(Internal/Public/Confidential)|Select the appropriate data classification for the environment|
|cost_center|A valid Apptio ID to associate the Environment to.|GHS-APPTIOID: Provide a valid Apptio ID (from the FCI application).|
|workload_admins|Must be registered User[sys_user]|Specify the users that need access to the workloads deployed in this Application Service Environment. These users will not have permissions to deploy or manage any resources in this Application Service Environment.|
|u_app_env_admins|Valid registered user accounts [sys_user]  recognized by IdAM.|Application Environment Administrators will get permissions that allow them to unlock or release the CyberArk sessions via the CyberArk portal|
|azure_services_required|true/false||
|cyberark_safe_required|true/false|Specify the field with value, true, if CyberArk Safe is required, otherwise, false.|
|onead_ou_required|true/false|Specify the field with value, true, if OneAD OU is required to be created, otherwise, false.|
|onead_sa_required|true/false|Specify the field with value, true, if OneAD Service Account is required to be created, otherwise, false.|
|tfe_required|true/false|Specify the field with value, true, if the terraform environment is required to be created, otherwise, false|
|app_account_required|true/false|Specify the field with true, if an application account is required, otherwise, false.|
|sql_account_required|true/false|Specify the field with true, if a SQL account is required, otherwise, false.|
|gpo_admin_required|Yes/No|Specify the field with value,  true, if OneAD Aura GPO admin account is required, otherwise, false.|
|organization|ASR, IFS, PwCTech|Specify TFE Organization. This determines the TFE instance to use for the new workspace.|
|tfe_team_members|List of the email ids(previous and new).This list will be updated as theTFE Team members.|Specify the valid PwC email accounts of all the users, who should be assigned the TFE Workspace admin role.|
|requested_for|Email address to be notified when the microservice has completed|Specify the PWC email address of the person for whom the request is being submitted.|
|vnet_name|Virtual networks related to the hosting location selected.|The Hosting Cloud network of the new Recovery Environment|
|portal_users|Text|Specify the list of Azure Read only users or portal users. Specify valid PwC email addresses|
|subscription|Name of the Subscription to be used|Specify the subscription name to be used.|
|tfe_workspaces|JSON list|Specify the purpose of TFE workspace and TFE workspace suffix.|
||||


> # **Manage TFE Credentials**

## Purpose

This API is used to update/recycle the Azure credentials vaulted in the secure variables on the TFE Workspaces for an application environment. The SPNs are created dynamically via NGC Vault and are short -lived for the duration of the deployment. It is expected to recycle the credentials for every deployment.

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/pwc_nextgen_request/manage_tfe_credentials

**Request Type:** POST

**Parameters:** 
| Label(name) | Options | Description |
|-------|-------|-------|
|requested_for|Email of the person the request is being submitted on behalf of|Specify the PWC email address of the person for whom the request is being submitted.|
|environment_id|App Environment Id|Specify the Application Environment ID of the Application Environment.|
||||

> # **Get environment details**

## Purpose

This API is used to retrieve all relevant details and config parameters of an environment.

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/pwc_nextgen_request/environment_details

**Request Type:** GET

**Query Parameters:** 
| Label(name) | Options | Description |
|-------|-------|-------|
|environment_id|App Environment ID of the Application Environment|Specify the Application Environment ID of the Application Environment.|
||||

> # **Create config Params**

## Purpose

This API is used to create config parameters for an environment.

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/pwc_nextgen_request/create_params

**Request Type:** POST

**Parameters:** 
| Label(name) | Options | Description |
|-------|-------|-------|
|environment_id|App Environment ID of the Application Environment|Specify the Application Environment ID of the Application Environment.|
|params|Config params details |Specify the config params and values in JSON format.|
||||

> # **Naming services**

This API is used to calculate and return resource names based on the established NextGen naming schema for the various resource types. 

**Endpoint:** https://api-central-sit.pwc.com/ngc-sandbox-service/v3/pwc_nextgen_request/naming_service

**Request Type:** POST

**Parameters:** 
**Note :** Parameters for this API vary based on the Resource Type being requested. 