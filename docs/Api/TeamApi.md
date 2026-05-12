# Swagger\Client\TeamApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteTeam**](TeamApi.md#deleteteam) | **DELETE** /api/teams/{id} | Delete team
[**deleteTeamActivity**](TeamApi.md#deleteteamactivity) | **DELETE** /api/teams/{id}/activities/{activityId} | Revoke activity access
[**deleteTeamCustomer**](TeamApi.md#deleteteamcustomer) | **DELETE** /api/teams/{id}/customers/{customerId} | Revoke customer access
[**deleteTeamMember**](TeamApi.md#deleteteammember) | **DELETE** /api/teams/{id}/members/{userId} | Remove team member
[**deleteTeamProject**](TeamApi.md#deleteteamproject) | **DELETE** /api/teams/{id}/projects/{projectId} | Revoke project access
[**getTeam**](TeamApi.md#getteam) | **GET** /api/teams/{id} | Fetch team
[**getTeams**](TeamApi.md#getteams) | **GET** /api/teams | Fetch teams
[**patchTeam**](TeamApi.md#patchteam) | **PATCH** /api/teams/{id} | Update team
[**postTeam**](TeamApi.md#postteam) | **POST** /api/teams | Create team
[**postTeamActivity**](TeamApi.md#postteamactivity) | **POST** /api/teams/{id}/activities/{activityId} | Grant activity access
[**postTeamCustomer**](TeamApi.md#postteamcustomer) | **POST** /api/teams/{id}/customers/{customerId} | Grant customer access
[**postTeamMember**](TeamApi.md#postteammember) | **POST** /api/teams/{id}/members/{userId} | Add team member
[**postTeamProject**](TeamApi.md#postteamproject) | **POST** /api/teams/{id}/projects/{projectId} | Grant project access

# **deleteTeam**
> deleteTeam($id)

Delete team

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Team ID to delete

try {
    $apiInstance->deleteTeam($id);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->deleteTeam: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Team ID to delete |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteTeamActivity**
> \Swagger\Client\Model\Team deleteTeamActivity($id, $activityId)

Revoke activity access

This removes access to the activity from the team.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The team whose permission will be revoked
$activityId = "activityId_example"; // string | The activity to remove (Activity ID)

try {
    $result = $apiInstance->deleteTeamActivity($id, $activityId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->deleteTeamActivity: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The team whose permission will be revoked |
 **activityId** | **string**| The activity to remove (Activity ID) |

### Return type

[**\Swagger\Client\Model\Team**](../Model/Team.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteTeamCustomer**
> \Swagger\Client\Model\Team deleteTeamCustomer($id, $customerId)

Revoke customer access

This removes access to the customer from the team.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The team whose permission will be revoked
$customerId = "customerId_example"; // string | The customer to remove (Customer ID)

try {
    $result = $apiInstance->deleteTeamCustomer($id, $customerId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->deleteTeamCustomer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The team whose permission will be revoked |
 **customerId** | **string**| The customer to remove (Customer ID) |

### Return type

[**\Swagger\Client\Model\Team**](../Model/Team.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteTeamMember**
> \Swagger\Client\Model\Team deleteTeamMember($id, $userId)

Remove team member

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The team from which the member will be removed
$userId = "userId_example"; // string | The team member to remove (User ID)

try {
    $result = $apiInstance->deleteTeamMember($id, $userId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->deleteTeamMember: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The team from which the member will be removed |
 **userId** | **string**| The team member to remove (User ID) |

### Return type

[**\Swagger\Client\Model\Team**](../Model/Team.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteTeamProject**
> \Swagger\Client\Model\Team deleteTeamProject($id, $projectId)

Revoke project access

This removes access to the project from the team.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The team whose permission will be revoked
$projectId = "projectId_example"; // string | The project to remove (Project ID)

try {
    $result = $apiInstance->deleteTeamProject($id, $projectId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->deleteTeamProject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The team whose permission will be revoked |
 **projectId** | **string**| The project to remove (Project ID) |

### Return type

[**\Swagger\Client\Model\Team**](../Model/Team.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTeam**
> \Swagger\Client\Model\Team getTeam($id)

Fetch team

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getTeam($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->getTeam: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\Swagger\Client\Model\Team**](../Model/Team.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTeams**
> \Swagger\Client\Model\TeamCollection[] getTeams()

Fetch teams

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getTeams();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->getTeams: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\TeamCollection[]**](../Model/TeamCollection.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchTeam**
> \Swagger\Client\Model\Team patchTeam($body, $id)

Update team

Update an existing team, you can pass all or just a subset of all attributes (passing members will replace all existing ones)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\TeamEditForm(); // \Swagger\Client\Model\TeamEditForm | 
$id = "id_example"; // string | Team ID to update

try {
    $result = $apiInstance->patchTeam($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->patchTeam: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TeamEditForm**](../Model/TeamEditForm.md)|  |
 **id** | **string**| Team ID to update |

### Return type

[**\Swagger\Client\Model\Team**](../Model/Team.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTeam**
> \Swagger\Client\Model\Team postTeam($body)

Create team

Creates a new team and returns it afterwards

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\TeamEditForm(); // \Swagger\Client\Model\TeamEditForm | 

try {
    $result = $apiInstance->postTeam($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->postTeam: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TeamEditForm**](../Model/TeamEditForm.md)|  |

### Return type

[**\Swagger\Client\Model\Team**](../Model/Team.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTeamActivity**
> \Swagger\Client\Model\Team postTeamActivity($id, $activityId)

Grant activity access

The team is granted access to the activity.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The team that is granted access
$activityId = "activityId_example"; // string | The activity to grant acecess to (Activity ID)

try {
    $result = $apiInstance->postTeamActivity($id, $activityId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->postTeamActivity: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The team that is granted access |
 **activityId** | **string**| The activity to grant acecess to (Activity ID) |

### Return type

[**\Swagger\Client\Model\Team**](../Model/Team.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTeamCustomer**
> \Swagger\Client\Model\Team postTeamCustomer($id, $customerId)

Grant customer access

The team is granted access to the customer.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The team that is granted access
$customerId = "customerId_example"; // string | The customer to grant acecess to (Customer ID)

try {
    $result = $apiInstance->postTeamCustomer($id, $customerId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->postTeamCustomer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The team that is granted access |
 **customerId** | **string**| The customer to grant acecess to (Customer ID) |

### Return type

[**\Swagger\Client\Model\Team**](../Model/Team.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTeamMember**
> \Swagger\Client\Model\Team postTeamMember($id, $userId)

Add team member

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The team which will receive the new member
$userId = "userId_example"; // string | The team member to add (User ID)

try {
    $result = $apiInstance->postTeamMember($id, $userId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->postTeamMember: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The team which will receive the new member |
 **userId** | **string**| The team member to add (User ID) |

### Return type

[**\Swagger\Client\Model\Team**](../Model/Team.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTeamProject**
> \Swagger\Client\Model\Team postTeamProject($id, $projectId)

Grant project access

The team is granted access to the project.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\TeamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The team that is granted access
$projectId = "projectId_example"; // string | The project to grant acecess to (Project ID)

try {
    $result = $apiInstance->postTeamProject($id, $projectId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamApi->postTeamProject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The team that is granted access |
 **projectId** | **string**| The project to grant acecess to (Project ID) |

### Return type

[**\Swagger\Client\Model\Team**](../Model/Team.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

