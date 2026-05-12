# TimesheetCollection

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activity** | **int** |  | [optional] 
**project** | **int** |  | [optional] 
**user** | **int** |  | [optional] 
**tags** | **string[]** |  | [optional] 
**id** | **int** |  | [optional] 
**begin** | [**\DateTime**](\DateTime.md) | Attention: Accessor MUST be used, otherwise date will be serialized in UTC. | 
**end** | [**\DateTime**](\DateTime.md) | Attention: Accessor MUST be used, otherwise date will be serialized in UTC. | [optional] 
**duration** | **int** |  | [optional] [default to 0]
**break** | **int** |  | [optional] [default to 0]
**description** | **string** |  | [optional] 
**rate** | **float** |  | [optional] [default to 0]
**internalRate** | **float** |  | [optional] 
**exported** | **bool** |  | [optional] [default to false]
**billable** | **bool** |  | [optional] [default to true]
**metaFields** | [**\Swagger\Client\Model\TimesheetMeta[]**](TimesheetMeta.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

