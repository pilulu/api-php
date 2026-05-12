# Swagger\Client\ActionsApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getActivityActions**](ActionsApi.md#getactivityactions) | **GET** /api/actions/activity/{id}/{view}/{locale} | Fetch item actions for Activity
[**getCustomerActions**](ActionsApi.md#getcustomeractions) | **GET** /api/actions/customer/{id}/{view}/{locale} | Fetch item actions for Customer
[**getProjectActions**](ActionsApi.md#getprojectactions) | **GET** /api/actions/project/{id}/{view}/{locale} | Fetch item actions for Project
[**getTimesheetActions**](ActionsApi.md#gettimesheetactions) | **GET** /api/actions/timesheet/{id}/{view}/{locale} | Fetch item actions for Timesheet

# **getActivityActions**
> \Swagger\Client\Model\PageAction getActivityActions($id, $view, $locale)

Fetch item actions for Activity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Activity ID to fetch
$view = "view_example"; // string | View to display the actions at (e.g. index, custom)
$locale = "locale_example"; // string | Language to translate the action title to (e.g. de, en)

try {
    $result = $apiInstance->getActivityActions($id, $view, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActionsApi->getActivityActions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Activity ID to fetch |
 **view** | **string**| View to display the actions at (e.g. index, custom) |
 **locale** | **string**| Language to translate the action title to (e.g. de, en) |

### Return type

[**\Swagger\Client\Model\PageAction**](../Model/PageAction.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomerActions**
> \Swagger\Client\Model\PageAction getCustomerActions($id, $view, $locale)

Fetch item actions for Customer

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Customer ID to fetch
$view = "view_example"; // string | View to display the actions at (e.g. index, custom)
$locale = "locale_example"; // string | Language to translate the action title to (e.g. de, en)

try {
    $result = $apiInstance->getCustomerActions($id, $view, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActionsApi->getCustomerActions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Customer ID to fetch |
 **view** | **string**| View to display the actions at (e.g. index, custom) |
 **locale** | **string**| Language to translate the action title to (e.g. de, en) |

### Return type

[**\Swagger\Client\Model\PageAction**](../Model/PageAction.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getProjectActions**
> \Swagger\Client\Model\PageAction getProjectActions($id, $view, $locale)

Fetch item actions for Project

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Project ID to fetch
$view = "view_example"; // string | View to display the actions at (e.g. index, custom)
$locale = "locale_example"; // string | Language to translate the action title to (e.g. de, en)

try {
    $result = $apiInstance->getProjectActions($id, $view, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActionsApi->getProjectActions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Project ID to fetch |
 **view** | **string**| View to display the actions at (e.g. index, custom) |
 **locale** | **string**| Language to translate the action title to (e.g. de, en) |

### Return type

[**\Swagger\Client\Model\PageAction**](../Model/PageAction.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTimesheetActions**
> \Swagger\Client\Model\PageAction getTimesheetActions($id, $view, $locale)

Fetch item actions for Timesheet

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Timesheet ID to fetch
$view = "view_example"; // string | View to display the actions at (e.g. index, custom)
$locale = "locale_example"; // string | Language to translate the action title to (e.g. de, en)

try {
    $result = $apiInstance->getTimesheetActions($id, $view, $locale);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActionsApi->getTimesheetActions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Timesheet ID to fetch |
 **view** | **string**| View to display the actions at (e.g. index, custom) |
 **locale** | **string**| Language to translate the action title to (e.g. de, en) |

### Return type

[**\Swagger\Client\Model\PageAction**](../Model/PageAction.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

