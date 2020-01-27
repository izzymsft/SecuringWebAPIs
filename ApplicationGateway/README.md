## Deploying App Gateway with ARM Template

The objective of this set up is to allow the private API M endpoint for the APIs as well as the developer portal to be reachable from oustide the VNet.

This example works with an App Gateway instance that is deployed into a private subnet in the same virtual network as the APIM instance.

It exposes a public IP address that is bound to two HTTPS listeners - one for the APIs and one for the Portal.

The ARM template and the Parameters file in this directory can be used for this exercise.

In this example, all the parameters are in a parameter.json file

```shell

az group deployment create --name AppGateway20200127A --resource-group SecureDemo --template-file app-gateway-template.json --parameters @app-gateway-parameters.json

```
In this example, there are some standalone parameters loaded from a file

```shell

az group deployment create --name AppGateway20200127A --resource-group SecureDemo --template-file app-gateway-template.json --parameters @app-gateway-parameters.json apiCertificate=@stringContent.txt portalCertificate=@stringContent.txt

```