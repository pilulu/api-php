# Swagger\Client\ActivityApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteActivity**](ActivityApi.md#deleteactivity) | **DELETE** /api/activities/{id} | Delete activity
[**deleteActivityRate**](ActivityApi.md#deleteactivityrate) | **DELETE** /api/activities/{id}/rates/{rateId} | Delete rate for activity
[**getActivities**](ActivityApi.md#getactivities) | **GET** /api/activities | Fetch activities
[**getActivity**](ActivityApi.md#getactivity) | **GET** /api/activities/{id} | Fetch activity
[**getActivityRates**](ActivityApi.md#getactivityrates) | **GET** /api/activities/{id}/rates | Fetch rates for activity
[**patchActivity**](ActivityApi.md#patchactivity) | **PATCH** /api/activities/{id} | Update activity
[**patchAppApiActivityMeta**](ActivityApi.md#patchappapiactivitymeta) | **PATCH** /api/activities/{id}/meta | Update activity custom-field
[**postActivity**](ActivityApi.md#postactivity) | **POST** /api/activities | Create activity
[**postActivityRate**](ActivityApi.md#postactivityrate) | **POST** /api/activities/{id}/rates | Add rate for activity

# **deleteActivity**
> deleteActivity($id)

Delete activity

[DANGER] This will also delete ALL linked timesheets. Do you want to use `PATCH` instead and mark it as inactive with `{visible: false}` instead?

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Activity ID to delete

try {
    $apiInstance->deleteActivity($id);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->deleteActivity: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Activity ID to delete |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteActivityRate**
> deleteActivityRate($id, $rateId)

Delete rate for activity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The activity whose rate will be removed
$rateId = "rateId_example"; // string | The rate to remove

try {
    $apiInstance->deleteActivityRate($id, $rateId);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->deleteActivityRate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The activity whose rate will be removed |
 **rateId** | **string**| The rate to remove |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getActivities**
> \Swagger\Client\Model\ActivityCollection[] getActivities($project, $projects, $visible, $globals, $orderBy, $order, $term)

Fetch activities

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$project = "project_example"; // string | Project ID to filter activities
$projects = new \Swagger\Client\Model\array(); // array | List of project IDs to filter activities, e.g.: projects[]=1&projects[]=2
$visible = "1"; // string | Visibility status to filter activities: 1=visible, 2=hidden, 3=all
$globals = "globals_example"; // string | Use if you want to fetch only global activities. Allowed values: 0|1 (default: 0 for false)
$orderBy = "orderBy_example"; // string | The field by which results will be ordered. Allowed values: id, name, project (default: name)
$order = "order_example"; // string | The result order. Allowed values: ASC, DESC (default: ASC)
$term = "term_example"; // string | Free search term

try {
    $result = $apiInstance->getActivities($project, $projects, $visible, $globals, $orderBy, $order, $term);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->getActivities: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project** | **string**| Project ID to filter activities | [optional]
 **projects** | [**array**](../Model/.md)| List of project IDs to filter activities, e.g.: projects[]&#x3D;1&amp;projects[]&#x3D;2 | [optional] [default to []]
 **visible** | **string**| Visibility status to filter activities: 1&#x3D;visible, 2&#x3D;hidden, 3&#x3D;all | [optional] [default to 1]
 **globals** | **string**| Use if you want to fetch only global activities. Allowed values: 0|1 (default: 0 for false) | [optional]
 **orderBy** | **string**| The field by which results will be ordered. Allowed values: id, name, project (default: name) | [optional]
 **order** | **string**| The result order. Allowed values: ASC, DESC (default: ASC) | [optional]
 **term** | **string**| Free search term | [optional]

### Return type

[**\Swagger\Client\Model\ActivityCollection[]**](../Model/ActivityCollection.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getActivity**
> \Swagger\Client\Model\ActivityEntity getActivity($id)

Fetch activity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Activity ID to fetch

try {
    $result = $apiInstance->getActivity($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->getActivity: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Activity ID to fetch |

### Return type

[**\Swagger\Client\Model\ActivityEntity**](../Model/ActivityEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getActivityRates**
> \Swagger\Client\Model\ActivityRate[] getActivityRates($id)

Fetch rates for activity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The activity whose rates will be returned

try {
    $result = $apiInstance->getActivityRates($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->getActivityRates: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The activity whose rates will be returned |

### Return type

[**\Swagger\Client\Model\ActivityRate[]**](../Model/ActivityRate.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchActivity**
> \Swagger\Client\Model\ActivityEntity patchActivity($body, $id)

Update activity

Update an existing activity, you can pass all or just a subset of all attributes

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\ActivityEditForm(); // \Swagger\Client\Model\ActivityEditForm | 
$id = "id_example"; // string | Activity ID to update

try {
    $result = $apiInstance->patchActivity($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->patchActivity: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\ActivityEditForm**](../Model/ActivityEditForm.md)|  |
 **id** | **string**| Activity ID to update |

### Return type

[**\Swagger\Client\Model\ActivityEntity**](../Model/ActivityEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchAppApiActivityMeta**
> \Swagger\Client\Model\ActivityEntity patchAppApiActivityMeta($id, $body)

Update activity custom-field

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Activity record ID to set the meta-field value for
$body = new \Swagger\Client\Model\IdMetaBody(); // \Swagger\Client\Model\IdMetaBody | 

try {
    $result = $apiInstance->patchAppApiActivityMeta($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->patchAppApiActivityMeta: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Activity record ID to set the meta-field value for |
 **body** | [**\Swagger\Client\Model\IdMetaBody**](../Model/IdMetaBody.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\ActivityEntity**](../Model/ActivityEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postActivity**
> \Swagger\Client\Model\ActivityEntity postActivity($body)

Create activity

Creates a new activity and returns it afterwards

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\ActivityEditForm(); // \Swagger\Client\Model\ActivityEditForm | 

try {
    $result = $apiInstance->postActivity($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->postActivity: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\ActivityEditForm**](../Model/ActivityEditForm.md)|  |

### Return type

[**\Swagger\Client\Model\ActivityEntity**](../Model/ActivityEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postActivityRate**
> \Swagger\Client\Model\ActivityRate postActivityRate($body, $id)

Add rate for activity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\ActivityRateForm(); // \Swagger\Client\Model\ActivityRateForm | 
$id = "id_example"; // string | The activity to add the rate for

try {
    $result = $apiInstance->postActivityRate($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->postActivityRate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\ActivityRateForm**](../Model/ActivityRateForm.md)|  |
 **id** | **string**| The activity to add the rate for |

### Return type

[**\Swagger\Client\Model\ActivityRate**](../Model/ActivityRate.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

