# Swagger\Client\ProjectApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteProject**](ProjectApi.md#deleteproject) | **DELETE** /api/projects/{id} | Delete project
[**deleteProjectRate**](ProjectApi.md#deleteprojectrate) | **DELETE** /api/projects/{id}/rates/{rateId} | Delete rate for project
[**getProject**](ProjectApi.md#getproject) | **GET** /api/projects/{id} | Fetch project
[**getProjectRates**](ProjectApi.md#getprojectrates) | **GET** /api/projects/{id}/rates | Fetch rates for project
[**getProjects**](ProjectApi.md#getprojects) | **GET** /api/projects | Fetch projects
[**patchAppApiProjectMeta**](ProjectApi.md#patchappapiprojectmeta) | **PATCH** /api/projects/{id}/meta | Update project custom-field
[**patchProject**](ProjectApi.md#patchproject) | **PATCH** /api/projects/{id} | Update project
[**postProject**](ProjectApi.md#postproject) | **POST** /api/projects | Create project
[**postProjectRate**](ProjectApi.md#postprojectrate) | **POST** /api/projects/{id}/rates | Add rate for project

# **deleteProject**
> deleteProject($id)

Delete project

[DANGER] This will also delete ALL linked activities and timesheets. Do you want to use `PATCH` instead and mark it as inactive with `{visible: false}` instead?

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Project ID to delete

try {
    $apiInstance->deleteProject($id);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->deleteProject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Project ID to delete |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteProjectRate**
> deleteProjectRate($id, $rateId)

Delete rate for project

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The project whose rate will be removed
$rateId = "rateId_example"; // string | The rate to remove

try {
    $apiInstance->deleteProjectRate($id, $rateId);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->deleteProjectRate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The project whose rate will be removed |
 **rateId** | **string**| The rate to remove |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getProject**
> \Swagger\Client\Model\ProjectEntity getProject($id)

Fetch project

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getProject($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->getProject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\Swagger\Client\Model\ProjectEntity**](../Model/ProjectEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getProjectRates**
> \Swagger\Client\Model\ProjectRate[] getProjectRates($id)

Fetch rates for project

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The project whose rates will be returned

try {
    $result = $apiInstance->getProjectRates($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->getProjectRates: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The project whose rates will be returned |

### Return type

[**\Swagger\Client\Model\ProjectRate[]**](../Model/ProjectRate.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getProjects**
> \Swagger\Client\Model\ProjectCollection[] getProjects($customer, $customers, $visible, $start, $end, $ignoreDates, $globalActivities, $order, $orderBy, $term)

Fetch projects

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer = "customer_example"; // string | Customer ID to filter projects
$customers = new \Swagger\Client\Model\array(); // array | List of customer IDs to filter, e.g.: customers[]=1&customers[]=2
$visible = "1"; // string | Visibility status to filter projects: 1=visible, 2=hidden, 3=both
$start = "start_example"; // string | Only projects that started before this date will be included. Allowed format: HTML5 (default: now, if end is also empty)
$end = "end_example"; // string | Only projects that ended after this date will be included. Allowed format: HTML5 (default: now, if start is also empty)
$ignoreDates = "ignoreDates_example"; // string | If set, start and end are completely ignored. Allowed values: 1 (default: off)
$globalActivities = "globalActivities_example"; // string | If given, filters projects by their 'global activity' support. Allowed values: 1 (supports global activities) and 0 (without global activities) (default: all)
$order = "order_example"; // string | The result order. Allowed values: ASC, DESC (default: ASC)
$orderBy = "orderBy_example"; // string | The field by which results will be ordered. Allowed values: id, name, customer (default: name)
$term = "term_example"; // string | Free search term

try {
    $result = $apiInstance->getProjects($customer, $customers, $visible, $start, $end, $ignoreDates, $globalActivities, $order, $orderBy, $term);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->getProjects: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer** | **string**| Customer ID to filter projects | [optional]
 **customers** | [**array**](../Model/.md)| List of customer IDs to filter, e.g.: customers[]&#x3D;1&amp;customers[]&#x3D;2 | [optional] [default to []]
 **visible** | **string**| Visibility status to filter projects: 1&#x3D;visible, 2&#x3D;hidden, 3&#x3D;both | [optional] [default to 1]
 **start** | **string**| Only projects that started before this date will be included. Allowed format: HTML5 (default: now, if end is also empty) | [optional]
 **end** | **string**| Only projects that ended after this date will be included. Allowed format: HTML5 (default: now, if start is also empty) | [optional]
 **ignoreDates** | **string**| If set, start and end are completely ignored. Allowed values: 1 (default: off) | [optional]
 **globalActivities** | **string**| If given, filters projects by their &#x27;global activity&#x27; support. Allowed values: 1 (supports global activities) and 0 (without global activities) (default: all) | [optional]
 **order** | **string**| The result order. Allowed values: ASC, DESC (default: ASC) | [optional]
 **orderBy** | **string**| The field by which results will be ordered. Allowed values: id, name, customer (default: name) | [optional]
 **term** | **string**| Free search term | [optional]

### Return type

[**\Swagger\Client\Model\ProjectCollection[]**](../Model/ProjectCollection.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchAppApiProjectMeta**
> \Swagger\Client\Model\ProjectEntity patchAppApiProjectMeta($id, $body)

Update project custom-field

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Project record ID to set the meta-field value for
$body = new \Swagger\Client\Model\IdMetaBody2(); // \Swagger\Client\Model\IdMetaBody2 | 

try {
    $result = $apiInstance->patchAppApiProjectMeta($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->patchAppApiProjectMeta: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Project record ID to set the meta-field value for |
 **body** | [**\Swagger\Client\Model\IdMetaBody2**](../Model/IdMetaBody2.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\ProjectEntity**](../Model/ProjectEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchProject**
> \Swagger\Client\Model\ProjectEntity patchProject($body, $id)

Update project

Update an existing project, you can pass all or just a subset of all attributes

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\ProjectEditForm(); // \Swagger\Client\Model\ProjectEditForm | 
$id = "id_example"; // string | Project ID to update

try {
    $result = $apiInstance->patchProject($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->patchProject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\ProjectEditForm**](../Model/ProjectEditForm.md)|  |
 **id** | **string**| Project ID to update |

### Return type

[**\Swagger\Client\Model\ProjectEntity**](../Model/ProjectEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postProject**
> \Swagger\Client\Model\ProjectEntity postProject($body)

Create project

Creates a new project and returns it afterwards

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\ProjectEditForm(); // \Swagger\Client\Model\ProjectEditForm | 

try {
    $result = $apiInstance->postProject($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->postProject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\ProjectEditForm**](../Model/ProjectEditForm.md)|  |

### Return type

[**\Swagger\Client\Model\ProjectEntity**](../Model/ProjectEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postProjectRate**
> \Swagger\Client\Model\ProjectRate postProjectRate($body, $id)

Add rate for project

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\ProjectRateForm(); // \Swagger\Client\Model\ProjectRateForm | 
$id = "id_example"; // string | The project to add the rate for

try {
    $result = $apiInstance->postProjectRate($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->postProjectRate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\ProjectRateForm**](../Model/ProjectRateForm.md)|  |
 **id** | **string**| The project to add the rate for |

### Return type

[**\Swagger\Client\Model\ProjectRate**](../Model/ProjectRate.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

