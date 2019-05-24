# devsum19
DevSum19 - Serverless Microservices with Azure Service Fabric Mesh

ARM template files in JSON format.

To run, execute **az mesh deployment create** with the proper parameters as follows:

```
az mesh deployment create --resource-group <YOUR_RESOURCE_GROUP> --template-file devsum.json --parameters devsum.parameters.json
```

Just replace <YOUR_REPLACE_GROUP> with the name of an existing resource group in your account
