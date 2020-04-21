Deployment command below:


New-AzResourceGroupDeployment `
    -ResourceGroupName RG2 `
    -TemplateFile ".\azuredeploy.json" `
    -TemplateParameterFile ".\azuredeploy.parameters.json" `
    -location eastus `
    -dnsLabelPrefix 'linux123'