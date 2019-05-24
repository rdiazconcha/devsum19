# devsum19
## DevSum19 - Serverless Microservices with Azure Service Fabric Mesh

### Demo 1
#### Web site containerization

Just run **docker build .** in the folder with the Dockerfile file in order to create the Docker container image in your own machine.  Then, you can push it to your own registry or just use rdiazconcha/devsum19

### Demo 2
#### .NET Core API microservices
##### Based on the following images:
- rdiazconcha/lilsearch
- rdiazconcha/lilcustomers
- rdiazconcha/lilproducts
- rdiazconcha/lilsales

ARM template files in JSON format.

To run, execute **az mesh deployment create** with the proper parameters as follows:

```
az mesh deployment create --resource-group <YOUR_RESOURCE_GROUP> --template-file devsum.json --parameters devsum.parameters.json
```

Just replace <YOUR_REPLACE_GROUP> with the name of an existing resource group in your account
