# Invoice

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**createdAt** | [**\DateTime**](\DateTime.md) |  | 
**overdue** | **bool** |  | [optional] 
**id** | **int** |  | [optional] 
**invoiceNumber** | **string** |  | 
**comment** | **string** |  | [optional] 
**customer** | [**\Swagger\Client\Model\Customer**](Customer.md) |  | 
**user** | [**\Swagger\Client\Model\User**](User.md) |  | 
**total** | **float** |  | [optional] [default to 0]
**tax** | **float** |  | [optional] [default to 0]
**currency** | **string** |  | 
**dueDays** | **int** |  | [optional] [default to 30]
**vat** | **float** |  | [optional] [default to 0]
**status** | **string** |  | [optional] [default to 'new']
**invoiceFilename** | **string** |  | 
**paymentDate** | [**\DateTime**](\DateTime.md) |  | [optional] 
**metaFields** | [**\Swagger\Client\Model\InvoiceMeta[]**](InvoiceMeta.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

