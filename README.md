# BulkDeployUAG

PowerShell script to bulk deploy or redeploy VMware Unified Access Gateway (UAG) appliances. This allows the selection of multiple UAGs, updates their deployment INI files to use the new installation OVA, and optionally updates the target string to use the supplied credentials.

	* GUI that allows selection of Unified Access Gateways from a list.
	* List generated from ini files in the chosen directory.
	* Select the installation OVA file to use.

## Usage
.\BulkDeployUAG.ps1 [vCenterUser] [vCenterPassword]

## Where
* vCenterUser     = Username for vCenter Server.
* vCenterPassword  = Password for vCenter Server user.

## Examples
* .\BulkDeployUAG.ps1
* .\BulkDeployUAG.ps1 administrator@vsphere.local Password

## Requirements
* uagdeploy PowerShell scripts provided with the Unified Access Gateway download (uagdeploy.ps1, uagdeploy.psm1, etc.) extracted and in the same directory as this script.
* ovftool installed
* Edit the settings.ini file and change entries to match your environment
* UAG ini files available (either in the ini folder, the folder you specified in settings.ini, or in a folder you will select when using the script.
* Unified Access Gateway installation OVA