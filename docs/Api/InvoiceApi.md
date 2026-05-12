# Swagger\Client\InvoiceApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getDownloadInvoice**](InvoiceApi.md#getdownloadinvoice) | **GET** /api/invoices/{id}/download | Download invoice
[**getInvoice**](InvoiceApi.md#getinvoice) | **GET** /api/invoices/{id} | Fetch invoice
[**getInvoices**](InvoiceApi.md#getinvoices) | **GET** /api/invoices | Fetch invoices
[**patchAppApiInvoiceUpdatemetafields**](InvoiceApi.md#patchappapiinvoiceupdatemetafields) | **PATCH** /api/invoices/{id}/custom-fields | Update invoice custom-fields

# **getDownloadInvoice**
> string getDownloadInvoice($id)

Download invoice

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\InvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getDownloadInvoice($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceApi->getDownloadInvoice: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

**string**

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/vnd.openxmlformats-officedocument.wordprocessingml.document, application/vnd.openxmlformats-officedocument.spreadsheetml.sheet, application/vnd.oasis.opendocument.spreadsheet, text/html, application/xml, text/xml, application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getInvoice**
> \Swagger\Client\Model\Invoice getInvoice($id)

Fetch invoice

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\InvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getInvoice($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceApi->getInvoice: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\Swagger\Client\Model\Invoice**](../Model/Invoice.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getInvoices**
> \Swagger\Client\Model\InvoiceCollection[] getInvoices($begin, $end, $customers, $status, $page, $size)

Fetch invoices

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\InvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$begin = "begin_example"; // string | Only invoices created at or after this date-time will be included (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss)
$end = "end_example"; // string | Only invoices created before or at this date-time will be included (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss)
$customers = new \Swagger\Client\Model\array(); // array | List of customer IDs to filter, e.g.: customers[]=1&customers[]=2
$status = new \Swagger\Client\Model\array(); // array | Invoice status: pending, paid, canceled, new. Default: all
$page = "page_example"; // string | The page to display, renders a 404 if not found (default: 1)
$size = "size_example"; // string | The amount of entries for each page (default: 50)

try {
    $result = $apiInstance->getInvoices($begin, $end, $customers, $status, $page, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceApi->getInvoices: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **begin** | **string**| Only invoices created at or after this date-time will be included (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss) | [optional]
 **end** | **string**| Only invoices created before or at this date-time will be included (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss) | [optional]
 **customers** | [**array**](../Model/.md)| List of customer IDs to filter, e.g.: customers[]&#x3D;1&amp;customers[]&#x3D;2 | [optional] [default to []]
 **status** | [**array**](../Model/.md)| Invoice status: pending, paid, canceled, new. Default: all | [optional] [default to []]
 **page** | **string**| The page to display, renders a 404 if not found (default: 1) | [optional]
 **size** | **string**| The amount of entries for each page (default: 50) | [optional]

### Return type

[**\Swagger\Client\Model\InvoiceCollection[]**](../Model/InvoiceCollection.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchAppApiInvoiceUpdatemetafields**
> \Swagger\Client\Model\Invoice patchAppApiInvoiceUpdatemetafields($body, $id)

Update invoice custom-fields

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\InvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array(new \Swagger\Client\Model\InvoiceMeta()); // \Swagger\Client\Model\InvoiceMeta[] | 
$id = "id_example"; // string | Invoice ID to set the custom-fields for

try {
    $result = $apiInstance->patchAppApiInvoiceUpdatemetafields($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceApi->patchAppApiInvoiceUpdatemetafields: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\InvoiceMeta[]**](../Model/InvoiceMeta.md)|  |
 **id** | **string**| Invoice ID to set the custom-fields for |

### Return type

[**\Swagger\Client\Model\Invoice**](../Model/Invoice.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

