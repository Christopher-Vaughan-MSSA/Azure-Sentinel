# MDTI-Intel-Reputation

## Overview
This playbook uses the [Microsoft Defender Threat Intelligence](https://learn.microsoft.com/en-us/defender/threat-intelligence/what-is-microsoft-defender-threat-intelligence-defender-ti) Reputation Data to automatically enrich incidents generated by Microsoft Sentinel. [Reputation](https://learn.microsoft.com/en-us/defender/threat-intelligence/reputation-scoring) information provides analyst with a decision as to whether an indicator is considered benign, suspicious or malicious. Analysts can leverage this playbook in order to enrich indicators found within an incident. Each reputation result is contained within a comment and will include detailed scoring information noting why a given indicator is considered suspicious or malicious with links back to the MDTI platform for more information.

## Prerequisites
1. This playbook inherits API connections created and established within a base playbook. Ensure you have deployed [MDTI-Base](https://raw.githubusercontent.com/Azure/Azure-Sentinel/master/Solutions/Microsoft%20Defender%20Threat%20Intellingence/Playbooks/MDTI-Base/azuredeploy.json) playbook. If you have trouble accessing your account or your credentials contact your account representative or reach out to discussMDTI[@]microsoft.com.
2. This playbook requires "Microsoft Sentinel Contributor" role to update Incidents.

## Deployment

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FAzure-Sentinel%2Fmaster%2FSolutions%2FMicrosoft%20Defender%20Threat%20Intellingence%2FPlaybooks%2FMDTI-Intel-Reputation%2Fazuredeploy.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>
<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FAzure-Sentinel%2Fmaster%2FSolutions%2FMicrosoft%20Defender%20Threat%20Intellingence%2FPlaybooks%2FMDTI-Intel-Reputation%2Fazuredeploy.json" target="_blank">
    <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>
</a>

### Post-Deployment Instructions
After deploying the playbook, you must authorize the connections leveraged.

1. Visit the playbook resource.
2. Under "Development Tools" (located on the left), click "API Connections".
3. Ensure each connection has been authorized.

**Note: If you've deployed the [MDTI-Base](https://raw.githubusercontent.com/Azure/Azure-Sentinel/master/Solutions/Microsoft%20Defender%20Threat%20Intellingence/Playbooks/MDTI-Base/azuredeploy.json) playbook, you will only need to authorize the Microsoft Sentinel connection.**
