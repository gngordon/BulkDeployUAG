# BulkDeployUAG

PowerShell script to bulk deploy or redeploy Omnissa Unified Access Gateway (UAG) appliances. This allows the selection of multiple UAGs, For each selected, it generates a runtime version of the deployment INI files to use the new installation OVA, optionally updates the target string to use the supplied credentials, and then deploys the UAG. Deploys multiple UAGs concurrently, the number of which can be controlled by the settings.ini file.

	* GUI that allows selection of Unified Access Gateways from a list.
	* List generated from ini files in the chosen directory.
	* Select the installation OVA file to use.

## Usage
.\BulkDeployUAG.ps1 [vCenterUser] [vCenterPassword]

### Where
* vCenterUser     = Username for vCenter Server.
* vCenterPassword  = Password for vCenter Server user.

### Examples
* .\BulkDeployUAG.ps1
* .\BulkDeployUAG.ps1 administrator@vsphere.local Password

## Requirements
* uagdeploy PowerShell scripts, available with the Unified Access Gateway download (uagdeploy.ps1, uagdeploy.psm1, etc.), extracted and in the same directory as this script.
* ovftool installed
* UAG ini files available in either the folder you specified in settings.ini, or in a folder you will select when using the script.
* Unified Access Gateway installation OVA
* Edit the settings.ini file and customize entries to match your environment and requirements.
