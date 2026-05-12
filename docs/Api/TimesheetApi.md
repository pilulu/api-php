# Swagger\Client\TimesheetApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteTimesheet**](TimesheetApi.md#deletetimesheet) | **DELETE** /api/timesheets/{id} | Delete timesheet
[**getActiveTimesheet**](TimesheetApi.md#getactivetimesheet) | **GET** /api/timesheets/active | Fetch active timesheets
[**getRecentTimesheet**](TimesheetApi.md#getrecenttimesheet) | **GET** /api/timesheets/recent | Fetch recent user activities
[**getRestartTimesheetGet**](TimesheetApi.md#getrestarttimesheetget) | **GET** /api/timesheets/{id}/restart | Restart timesheet
[**getStopTimesheetGet**](TimesheetApi.md#getstoptimesheetget) | **GET** /api/timesheets/{id}/stop | Stop active timesheet
[**getTimesheet**](TimesheetApi.md#gettimesheet) | **GET** /api/timesheets/{id} | Fetch timesheet
[**getTimesheets**](TimesheetApi.md#gettimesheets) | **GET** /api/timesheets | Fetch timesheets
[**patchAppApiTimesheetMeta**](TimesheetApi.md#patchappapitimesheetmeta) | **PATCH** /api/timesheets/{id}/meta | Update timesheet custom-field
[**patchDuplicateTimesheet**](TimesheetApi.md#patchduplicatetimesheet) | **PATCH** /api/timesheets/{id}/duplicate | Duplicate timesheet
[**patchExportTimesheet**](TimesheetApi.md#patchexporttimesheet) | **PATCH** /api/timesheets/{id}/export | Toggle timesheet export state
[**patchRestartTimesheet**](TimesheetApi.md#patchrestarttimesheet) | **PATCH** /api/timesheets/{id}/restart | Restart timesheet
[**patchStopTimesheet**](TimesheetApi.md#patchstoptimesheet) | **PATCH** /api/timesheets/{id}/stop | Stop active timesheet
[**patchTimesheet**](TimesheetApi.md#patchtimesheet) | **PATCH** /api/timesheets/{id} | Update timesheet
[**postTimesheet**](TimesheetApi.md#posttimesheet) | **POST** /api/timesheets | Create timesheet

# **deleteTimesheet**
> deleteTimesheet($id)

Delete timesheet

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Timesheet ID to delete

try {
    $apiInstance->deleteTimesheet($id);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->deleteTimesheet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Timesheet ID to delete |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getActiveTimesheet**
> \Swagger\Client\Model\TimesheetCollectionExpanded[] getActiveTimesheet()

Fetch active timesheets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getActiveTimesheet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->getActiveTimesheet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\TimesheetCollectionExpanded[]**](../Model/TimesheetCollectionExpanded.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRecentTimesheet**
> \Swagger\Client\Model\TimesheetCollectionExpanded[] getRecentTimesheet($begin, $size)

Fetch recent user activities

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$begin = "begin_example"; // string | Only records started at or after this date will be included. Default: today - 1 year (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss)
$size = "size_example"; // string | The amount of entries (default: 10)

try {
    $result = $apiInstance->getRecentTimesheet($begin, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->getRecentTimesheet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **begin** | **string**| Only records started at or after this date will be included. Default: today - 1 year (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss) | [optional]
 **size** | **string**| The amount of entries (default: 10) | [optional]

### Return type

[**\Swagger\Client\Model\TimesheetCollectionExpanded[]**](../Model/TimesheetCollectionExpanded.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRestartTimesheetGet**
> \Swagger\Client\Model\TimesheetEntity getRestartTimesheetGet($id, $body)

Restart timesheet

The restarted timesheet will be created for the current user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Timesheet ID to restart
$body = new \Swagger\Client\Model\IdRestartBody(); // \Swagger\Client\Model\IdRestartBody | 

try {
    $result = $apiInstance->getRestartTimesheetGet($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->getRestartTimesheetGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Timesheet ID to restart |
 **body** | [**\Swagger\Client\Model\IdRestartBody**](../Model/IdRestartBody.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\TimesheetEntity**](../Model/TimesheetEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getStopTimesheetGet**
> \Swagger\Client\Model\TimesheetEntity getStopTimesheetGet($id)

Stop active timesheet

This route is available via GET and PATCH, as users over and over again run into errors when stopping. Likely caused by a slow JS engine and a fast-click after page reload.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Timesheet ID to stop

try {
    $result = $apiInstance->getStopTimesheetGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->getStopTimesheetGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Timesheet ID to stop |

### Return type

[**\Swagger\Client\Model\TimesheetEntity**](../Model/TimesheetEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTimesheet**
> \Swagger\Client\Model\TimesheetEntity getTimesheet($id)

Fetch timesheet

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Timesheet ID to fetch

try {
    $result = $apiInstance->getTimesheet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->getTimesheet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Timesheet ID to fetch |

### Return type

[**\Swagger\Client\Model\TimesheetEntity**](../Model/TimesheetEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTimesheets**
> \Swagger\Client\Model\TimesheetCollection[] getTimesheets($user, $users, $customer, $customers, $project, $projects, $activity, $activities, $page, $size, $tags, $orderBy, $order, $begin, $end, $exported, $active, $billable, $full, $term, $modifiedAfter)

Fetch timesheets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user = "user_example"; // string | User ID to filter timesheets. Needs permission 'view_other_timesheet', pass 'all' to fetch data for all user (default: current user)
$users = new \Swagger\Client\Model\array(); // array | List of user IDs to filter, e.g.: users[]=1&users[]=2 (ignored if user=all)
$customer = "customer_example"; // string | Customer ID to filter timesheets
$customers = new \Swagger\Client\Model\array(); // array | List of customer IDs to filter, e.g.: customers[]=1&customers[]=2
$project = "project_example"; // string | Project ID to filter timesheets
$projects = new \Swagger\Client\Model\array(); // array | List of project IDs to filter, e.g.: projects[]=1&projects[]=2
$activity = "activity_example"; // string | Activity ID to filter timesheets
$activities = new \Swagger\Client\Model\array(); // array | List of activity IDs to filter, e.g.: activities[]=1&activities[]=2
$page = "page_example"; // string | The page to display, renders a 404 if not found (default: 1)
$size = "size_example"; // string | The amount of entries for each page (default: 50, max: 500)
$tags = new \Swagger\Client\Model\array(); // array | List of tag names, e.g. tags[]=bar&tags[]=foo
$orderBy = "orderBy_example"; // string | The field by which results will be ordered. Allowed values: id, begin, end, rate (default: begin)
$order = "order_example"; // string | The result order. Allowed values: ASC, DESC (default: DESC)
$begin = "begin_example"; // string | Only records started at or after this date-time will be included (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss)
$end = "end_example"; // string | Only records started at or before this date-time will be included (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss)
$exported = "exported_example"; // string | Use this flag if you want to filter for export state. Allowed values: 0=not exported, 1=exported (default: all)
$active = "active_example"; // string | Filter for running/active records. Allowed values: 0=stopped, 1=active (default: all)
$billable = "billable_example"; // string | Filter for non-/billable records. Allowed values: 0=non-billable, 1=billable (default: all)
$full = "full_example"; // string | Allows to fetch full objects including subresources. Allowed values: 0|1|false|true (default: false)
$term = "term_example"; // string | Free search term
$modifiedAfter = "modifiedAfter_example"; // string | Only records changed after this date will be included. You need to pass in a UTC date-time, as this field is stored in UTC (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss)

try {
    $result = $apiInstance->getTimesheets($user, $users, $customer, $customers, $project, $projects, $activity, $activities, $page, $size, $tags, $orderBy, $order, $begin, $end, $exported, $active, $billable, $full, $term, $modifiedAfter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->getTimesheets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user** | **string**| User ID to filter timesheets. Needs permission &#x27;view_other_timesheet&#x27;, pass &#x27;all&#x27; to fetch data for all user (default: current user) | [optional]
 **users** | [**array**](../Model/.md)| List of user IDs to filter, e.g.: users[]&#x3D;1&amp;users[]&#x3D;2 (ignored if user&#x3D;all) | [optional] [default to []]
 **customer** | **string**| Customer ID to filter timesheets | [optional]
 **customers** | [**array**](../Model/.md)| List of customer IDs to filter, e.g.: customers[]&#x3D;1&amp;customers[]&#x3D;2 | [optional] [default to []]
 **project** | **string**| Project ID to filter timesheets | [optional]
 **projects** | [**array**](../Model/.md)| List of project IDs to filter, e.g.: projects[]&#x3D;1&amp;projects[]&#x3D;2 | [optional] [default to []]
 **activity** | **string**| Activity ID to filter timesheets | [optional]
 **activities** | [**array**](../Model/.md)| List of activity IDs to filter, e.g.: activities[]&#x3D;1&amp;activities[]&#x3D;2 | [optional] [default to []]
 **page** | **string**| The page to display, renders a 404 if not found (default: 1) | [optional]
 **size** | **string**| The amount of entries for each page (default: 50, max: 500) | [optional]
 **tags** | [**array**](../Model/.md)| List of tag names, e.g. tags[]&#x3D;bar&amp;tags[]&#x3D;foo | [optional] [default to []]
 **orderBy** | **string**| The field by which results will be ordered. Allowed values: id, begin, end, rate (default: begin) | [optional]
 **order** | **string**| The result order. Allowed values: ASC, DESC (default: DESC) | [optional]
 **begin** | **string**| Only records started at or after this date-time will be included (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss) | [optional]
 **end** | **string**| Only records started at or before this date-time will be included (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss) | [optional]
 **exported** | **string**| Use this flag if you want to filter for export state. Allowed values: 0&#x3D;not exported, 1&#x3D;exported (default: all) | [optional]
 **active** | **string**| Filter for running/active records. Allowed values: 0&#x3D;stopped, 1&#x3D;active (default: all) | [optional]
 **billable** | **string**| Filter for non-/billable records. Allowed values: 0&#x3D;non-billable, 1&#x3D;billable (default: all) | [optional]
 **full** | **string**| Allows to fetch full objects including subresources. Allowed values: 0|1|false|true (default: false) | [optional]
 **term** | **string**| Free search term | [optional]
 **modifiedAfter** | **string**| Only records changed after this date will be included. You need to pass in a UTC date-time, as this field is stored in UTC (format: HTML5 datetime-local, e.g. YYYY-MM-DDThh:mm:ss) | [optional]

### Return type

[**\Swagger\Client\Model\TimesheetCollection[]**](../Model/TimesheetCollection.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchAppApiTimesheetMeta**
> \Swagger\Client\Model\TimesheetEntity patchAppApiTimesheetMeta($id, $body)

Update timesheet custom-field

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Timesheet ID to set the meta-field value for
$body = new \Swagger\Client\Model\IdMetaBody3(); // \Swagger\Client\Model\IdMetaBody3 | 

try {
    $result = $apiInstance->patchAppApiTimesheetMeta($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->patchAppApiTimesheetMeta: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Timesheet ID to set the meta-field value for |
 **body** | [**\Swagger\Client\Model\IdMetaBody3**](../Model/IdMetaBody3.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\TimesheetEntity**](../Model/TimesheetEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchDuplicateTimesheet**
> \Swagger\Client\Model\TimesheetEntity patchDuplicateTimesheet($id)

Duplicate timesheet

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Timesheet ID to duplicate

try {
    $result = $apiInstance->patchDuplicateTimesheet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->patchDuplicateTimesheet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Timesheet ID to duplicate |

### Return type

[**\Swagger\Client\Model\TimesheetEntity**](../Model/TimesheetEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchExportTimesheet**
> \Swagger\Client\Model\TimesheetEntity patchExportTimesheet($id)

Toggle timesheet export state

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Timesheet ID to switch export state

try {
    $result = $apiInstance->patchExportTimesheet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->patchExportTimesheet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Timesheet ID to switch export state |

### Return type

[**\Swagger\Client\Model\TimesheetEntity**](../Model/TimesheetEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchRestartTimesheet**
> patchRestartTimesheet($id, $body)

Restart timesheet

The restarted timesheet will be created for the current user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$body = new \Swagger\Client\Model\IdRestartBody1(); // \Swagger\Client\Model\IdRestartBody1 | 

try {
    $apiInstance->patchRestartTimesheet($id, $body);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->patchRestartTimesheet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **body** | [**\Swagger\Client\Model\IdRestartBody1**](../Model/IdRestartBody1.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchStopTimesheet**
> patchStopTimesheet($id)

Stop active timesheet

This route is available via GET and PATCH, as users over and over again run into errors when stopping. Likely caused by a slow JS engine and a fast-click after page reload.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->patchStopTimesheet($id);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->patchStopTimesheet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchTimesheet**
> \Swagger\Client\Model\TimesheetEntity patchTimesheet($body, $id)

Update timesheet

Update timesheet, you can pass all or just a subset of the attributes.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\TimesheetEditForm(); // \Swagger\Client\Model\TimesheetEditForm | 
$id = "id_example"; // string | Timesheet ID to update

try {
    $result = $apiInstance->patchTimesheet($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->patchTimesheet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TimesheetEditForm**](../Model/TimesheetEditForm.md)|  |
 **id** | **string**| Timesheet ID to update |

### Return type

[**\Swagger\Client\Model\TimesheetEntity**](../Model/TimesheetEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTimesheet**
> \Swagger\Client\Model\TimesheetEntity postTimesheet($body, $full)

Create timesheet

Creates a new timesheet for the current user and returns it afterwards.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TimesheetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\TimesheetEditForm(); // \Swagger\Client\Model\TimesheetEditForm | 
$full = "full_example"; // string | Allows to fetch fully serialized objects including subresources (TimesheetExpanded). Allowed values: true (default: false)

try {
    $result = $apiInstance->postTimesheet($body, $full);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimesheetApi->postTimesheet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TimesheetEditForm**](../Model/TimesheetEditForm.md)|  |
 **full** | **string**| Allows to fetch fully serialized objects including subresources (TimesheetExpanded). Allowed values: true (default: false) | [optional]

### Return type

[**\Swagger\Client\Model\TimesheetEntity**](../Model/TimesheetEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

