## bicep

### Variables
```bicep
var location = resourceGroup().location
var storageAccountName = 'barathstorage0981'

resource storage 'Microsoft.Storage/storageAccounts@2022-09-01' = {
  name: storageAccountName
  location: location
  sku: {
    name: 'Standard_LRS'
  }
  kind: 'StorageV2'
  properties: {}
}
```

## interpolated expressions
```bicep
var location = resourceGroup().location
var environment = 'prod'
var storageAccountName = '{environment}-barathstorage}'

resource storage 'Microsoft.Storage/storageAccounts@2022-09-01' = {
  name: storageAccountName
  location: location
  sku: {
    name: 'Standard_LRS'
  }
  kind: 'StorageV2'
  properties: {}
}
```
