# Assign a Role at Subscription Scope

![Azure Public Test Date](https://azurequickstartsservice.blob.core.windows.net/badges/subscription-level-deployments/subscription-role-assigment/PublicLastTestDate.svg)
![Azure Public Test Result](https://azurequickstartsservice.blob.core.windows.net/badges/subscription-level-deployments/subscription-role-assigment/PublicDeployment.svg)

![Azure US Gov Last Test Date](https://azurequickstartsservice.blob.core.windows.net/badges/subscription-level-deployments/subscription-role-assigment/FairfaxLastTestDate.svg)
![Azure US Gov Last Test Result](https://azurequickstartsservice.blob.core.windows.net/badges/subscription-level-deployments/subscription-role-assigment/FairfaxDeployment.svg)

![Best Practice Check](https://azurequickstartsservice.blob.core.windows.net/badges/subscription-level-deployments/subscription-role-assigment/BestPracticeResult.svg)
![Cred Scan Check](https://azurequickstartsservice.blob.core.windows.net/badges/subscription-level-deployments/subscription-role-assigment/CredScanResult.svg)

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fsubscription-level-deployments%2Fsubscription-role-assigment%2Fazuredeploy.json)
[![Deploy To Azure US Gov](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.svg?sanitize=true)](https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fsubscription-level-deployments%2Fsubscription-role-assigment%2Fazuredeploy.json)
[![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fsubscription-level-deployments%2Fcreate-rg-lock-role-assignment%2Fazuredeploy.json)

This template is a subscription level template that will assign a role at subscription scope.

Currently the only supported methods for deploying subscription level templates are the REST apis, some SDKS and the Azure CLI.  For the latest check [here](https://docs.microsoft.com/en-us/azure/azure-resource-manager/create-resource-group-in-template#create-empty-resource-group).

For deploying this template from the CLI you can run the following command from the folder where the sample is located.

<i>NOTE: Role Assigments use a GUID for the name, this must be unique for every role assignment on the group.  The roleAssignmentName parameter is used to seed the guid() function with this value, change it for each deployment.  You can supply a guid or any string, as long as it has not been used before when assigning the role to the resourceGroup.
</i>

```bash
az deployment create -l southcentralus --template-file ./azuredeploy.json --parameters roleAssignmentName={random seed}
```

