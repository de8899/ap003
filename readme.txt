Deployment commands below:

$location = Read-Host -Prompt "Enter the same location that is used for creating the key vault (i.e. centralus)"


New-AzResourceGroupDeployment `
    -ResourceGroupName RG2 `
    -TemplateFile ".\template.json" `
    -TemplateParameterFile ".\parameters.json"