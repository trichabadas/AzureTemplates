# AzureTemplates
Barracuda WAF ARM Templates for Azure

##Deploying with CLI, using a parameters file

```
~/Desktop/AWSCFT @ Pinaka (tushar) > azure group create -n "clirunwithparams" -l "Brazil South"
info:    Executing command group create
+ Getting resource group clirunwithparams
+ Creating resource group clirunwithparams
info:    Created resource group clirunwithparams
data:    Id:                  /subscriptions/dc0a59b7-9162-4b6d-94ed-62dfb866f5d6/resourceGroups/clirunwithparams
data:    Name:                clirunwithparams
data:    Location:            brazilsouth
data:    Provisioning State:  Succeeded
data:    Tags: null
data:
info:    group create command OK

~/Desktop/AWSCFT @ Pinaka (tushar) > azure group deployment create -f azureMainTemplateMultiPayG.json -e azureDeployParams.json clirunwithparams clirunwithparamsDeploy -v
info:    Executing command group deployment create
verbose: Initializing template configurations and parameters
verbose: Creating a deployment
info:    Created template deployment "clirunwithparamsDeploy"
verbose: Waiting for deployment to complete
data:    DeploymentName     : clirunwithparamsDeploy
data:    ResourceGroupName  : clirunwithparams
data:    ProvisioningState  : Succeeded
data:    Timestamp          : 2016-06-22T09:21:38.3664238Z
data:    Mode               : Incremental
data:    Name                Type          Value
data:    ------------------  ------------  ----------------
data:    adminPassword       SecureString  undefined
data:    location            String        Brazil South
data:    storageAccountName  String        clirunwithparams
data:    storageAccountType  String        Standard_LRS
data:    vmName              String        clirunwithparams
data:    dnsNameForLBIP      String        clirunwithparams
data:    vNETName            String        clirunwithparams
data:    addressPrefix       String        10.0.0.0/16
data:    subnetPrefix        String        10.0.0.0/16
data:    subnetName          String        clirunwithparams
data:    numberOfInstances   Int           2
data:    vmSize              String        Standard_A1
info:    group deployment create command OK
~/Desktop/AWSCFT @ Pinaka (tushar) >
```

