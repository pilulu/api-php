# ProjectEditForm

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | 
**number** | **string** |  | [optional] 
**comment** | **string** |  | [optional] 
**invoiceText** | **string** |  | [optional] 
**orderNumber** | **string** |  | [optional] 
**orderDate** | [**\DateTime**](\DateTime.md) |  | [optional] 
**start** | [**\DateTime**](\DateTime.md) |  | [optional] 
**end** | [**\DateTime**](\DateTime.md) |  | [optional] 
**customer** | **int** | Customer ID | 
**teams** | **int[]** | Array of Team IDs | [optional] 
**color** | **string** | The hexadecimal color code (default: auto-calculated by name) | [optional] 
**budget** | [****](.md) | The money budget | [optional] 
**timeBudget** | **string** | Duration - supports various formats: https://www.kimai.org/documentation/duration-format.html | [optional] 
**budgetType** | **string** | The type of budget. Only submit if you want to use a monthly budget. | [optional] 
**globalActivities** | **bool** |  | [optional] 
**visible** | **bool** |  | [optional] 
**billable** | **bool** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

