This template and params file builds a CentosOS system with the following:
- basic networking and disk
- public ssh key and password
  - password is from keyvault and provided in params file 
  - ssh key was generated in cloudshell and public key provided in params file.
    - this requires creating an rsa key pair prior to deployment.


New-AzResourceGroupDeployment `
    -ResourceGroupName RG2 `
    -TemplateFile ".\azuredeploy.json" `
    -TemplateParameterFile ".\azuredeploy.parameters.json" `
    -location eastus `
    -dnsLabelPrefix 'linux123'