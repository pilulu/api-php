# Swagger\Client\ExportApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteExportTemplate**](ExportApi.md#deleteexporttemplate) | **DELETE** /api/export/{id} | Delete export template

# **deleteExportTemplate**
> deleteExportTemplate($id)

Delete export template

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ExportApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Export template ID to delete

try {
    $apiInstance->deleteExportTemplate($id);
} catch (Exception $e) {
    echo 'Exception when calling ExportApi->deleteExportTemplate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Export template ID to delete |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

