# Spring-Config_Demo 

### Create a config service in PCF

```sh
cf create-service p-config-server trial myConfigService -c repo.json
```

### Push API code to PCF
```sh
cf push -f manifest.yml -p .\publish
```

Switch ASPNETCORE_ENVIRONMENT between development and staging. Push and see changes in the API response



