# MDTI-Automated-Triage

## Overview
This playbook uses the [Microsoft Defender Threat Intelligence](https://learn.microsoft.com/en-us/defender/threat-intelligence/what-is-microsoft-defender-threat-intelligence-defender-ti) Reputation data to automatically enrich incidents generated by Microsoft Sentinel. Indicators from an incident will be evaluated with MDTI [Reputation](https://learn.microsoft.com/en-us/defender/threat-intelligence/reputation-scoring) data. If any indicators are labeled as "suspicious", the incident will be tagged as such and its severity will be marked as "medium". If any indicators are labeled as "malicious", the incident will be tagged as such and its severity will be marked as "high". Regardless of the reputation state, comments will be added to the incident outlining the reputation details with links to further information if applicable.

## Prerequisites
1. This playbook inherits API connections created and established within a base playbook. Ensure you have deployed [MDTI-Base](https://raw.githubusercontent.com/Azure/Azure-Sentinel/master/Solutions/Microsoft%20Defender%20Threat%20Intellingence/Playbooks/MDTI-Base/azuredeploy.json) this playbook. If you have trouble accessing your account or your credentials contact your account representative or reach out to discussMDTI[@]microsoft.com.
2. This playbook requires "Microsoft Sentinel Contributor" role to update Incidents.


## Deployment

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FAzure-Sentinel%2Fmaster%2FSolutions%2FMicrosoft%20Defender%20Threat%20Intellingence%2FPlaybooks%2FMDTI-Automated-Triage%2Fincident-trigger%2Fazuredeploy.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>
<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FAzure-Sentinel%2Fmaster%2FSolutions%2FMicrosoft%20Defender%20Threat%20Intellingence%2FPlaybooks%2FMDTI-Automated-Triage%2Fincident-trigger%2Fazuredeploy.json" target="_blank">
    <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>
</a>

## Post-Deployment Instructions
After deploying the playbook, you must authorize the connections leveraged.

1. Visit the playbook resource.
2. Under "Development Tools" (located on the left), click "API Connections".
3. Ensure each connection has been authorized.

**Note: If you've deployed the [MDTI-Base](https://raw.githubusercontent.com/Azure/Azure-Sentinel/master/Solutions/Microsoft%20Defender%20Threat%20Intellingence/Playbooks/MDTI-Base/azuredeploy.json) playbook, you will only need to authorize the Microsoft Sentinel connection.**
