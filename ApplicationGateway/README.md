
## Deploying App Gateway with ARM Template

In this example, all the parameters are in a parameter.json file
```shell

az group deployment create --name AppGateway20200127A --resource-group SecureDemo --template-file app-gateway-template.json --parameters @app-gateway-parameters.json

```
In this example, there are some standalone parameters loaded from a file
```shell

az group deployment create --name AppGateway20200127B --resource-group SecureDemo --template-file app-gateway-template.json --parameters @app-gateway-parameters.json apiCertificate=@stringContent.txt portalCertificate=@stringContent.txt

```
