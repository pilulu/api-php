# Swagger\Client\UserApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiToken**](UserApi.md#deleteapitoken) | **DELETE** /api/users/api-token/{id} | Delete API token
[**getMeUser**](UserApi.md#getmeuser) | **GET** /api/users/me | Fetch current user
[**getUser**](UserApi.md#getuser) | **GET** /api/users/{id} | Fetch user
[**getUsers**](UserApi.md#getusers) | **GET** /api/users | Fetch users
[**patchAppApiUserUpdateuserpreference**](UserApi.md#patchappapiuserupdateuserpreference) | **PATCH** /api/users/{id}/preferences | Update user preferences
[**patchUser**](UserApi.md#patchuser) | **PATCH** /api/users/{id} | Update an existing user
[**postUser**](UserApi.md#postuser) | **POST** /api/users | Create user

# **deleteApiToken**
> deleteApiToken($id)

Delete API token

This ONLY works if the given API token exists and belongs to the current user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The API token ID to remove

try {
    $apiInstance->deleteApiToken($id);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->deleteApiToken: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The API token ID to remove |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMeUser**
> \Swagger\Client\Model\UserEntity getMeUser()

Fetch current user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getMeUser();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->getMeUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\UserEntity**](../Model/UserEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUser**
> \Swagger\Client\Model\UserEntity getUser($id)

Fetch user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | User ID to fetch

try {
    $result = $apiInstance->getUser($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->getUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| User ID to fetch |

### Return type

[**\Swagger\Client\Model\UserEntity**](../Model/UserEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUsers**
> \Swagger\Client\Model\UserCollection[] getUsers($visible, $orderBy, $order, $term, $full)

Fetch users

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$visible = "1"; // string | Visibility status to filter users: 1=visible, 2=hidden, 3=all
$orderBy = "orderBy_example"; // string | The field by which results will be ordered. Allowed values: id, username, alias, email (default: username)
$order = "order_example"; // string | The result order. Allowed values: ASC, DESC (default: ASC)
$term = "term_example"; // string | Free search term
$full = "full_example"; // string | Allows to fetch full objects including subresources. Allowed values: 0|1|false|true (default: false)

try {
    $result = $apiInstance->getUsers($visible, $orderBy, $order, $term, $full);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->getUsers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **visible** | **string**| Visibility status to filter users: 1&#x3D;visible, 2&#x3D;hidden, 3&#x3D;all | [optional] [default to 1]
 **orderBy** | **string**| The field by which results will be ordered. Allowed values: id, username, alias, email (default: username) | [optional]
 **order** | **string**| The result order. Allowed values: ASC, DESC (default: ASC) | [optional]
 **term** | **string**| Free search term | [optional]
 **full** | **string**| Allows to fetch full objects including subresources. Allowed values: 0|1|false|true (default: false) | [optional]

### Return type

[**\Swagger\Client\Model\UserCollection[]**](../Model/UserCollection.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchAppApiUserUpdateuserpreference**
> \Swagger\Client\Model\UserEntity patchAppApiUserUpdateuserpreference($body, $id)

Update user preferences

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array(new \Swagger\Client\Model\UserPreference()); // \Swagger\Client\Model\UserPreference[] | 
$id = "id_example"; // string | User ID to set the custom-field value for

try {
    $result = $apiInstance->patchAppApiUserUpdateuserpreference($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->patchAppApiUserUpdateuserpreference: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\UserPreference[]**](../Model/UserPreference.md)|  |
 **id** | **string**| User ID to set the custom-field value for |

### Return type

[**\Swagger\Client\Model\UserEntity**](../Model/UserEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchUser**
> \Swagger\Client\Model\UserEntity patchUser($body, $id)

Update an existing user

Update an existing user, you can pass all or just a subset of all attributes (passing roles will replace all existing ones)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\UserEditForm(); // \Swagger\Client\Model\UserEditForm | 
$id = "id_example"; // string | User ID to update

try {
    $result = $apiInstance->patchUser($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->patchUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\UserEditForm**](../Model/UserEditForm.md)|  |
 **id** | **string**| User ID to update |

### Return type

[**\Swagger\Client\Model\UserEntity**](../Model/UserEntity.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postUser**
> postUser($body)

Create user

Creates a new user and returns it afterwards

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\UserCreateForm(); // \Swagger\Client\Model\UserCreateForm | 

try {
    $apiInstance->postUser($body);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->postUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\UserCreateForm**](../Model/UserCreateForm.md)|  |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

