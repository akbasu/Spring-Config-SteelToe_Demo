# Spring-Config_Demo 

### Create a config service in PCF

```sh
cf create-service p-config-server trial myConfigService -c repo.json
```

### Push API code to PCF

Navigate to the project folder and publish the project

```sh
<Repository directory>src\akbasu.ConfigExample> dotnet publish -o .\publish akbasu.ConfigExample.csproj
```

Push to Cloud Foundry
```sh
cf push -f manifest.yml -p .\publish
```

Switch ASPNETCORE_ENVIRONMENT variable value between 'development' and 'staging'. Push and see changes in the API response



