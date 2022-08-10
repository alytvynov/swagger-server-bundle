# Swagger\Server\Api\CityApiInterface

All URIs are relative to *https://fixturecalendar.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCityById**](CityApiInterface.md#getCityById) | **GET** /cities/{cityId} | Find City by ID


## Service Declaration
```yaml
# src/Acme/MyBundle/Resources/services.yml
services:
    # ...
    acme.my_bundle.api.city:
        class: Acme\MyBundle\Api\CityApi
        tags:
            - { name: "swagger_server.api", api: "city" }
    # ...
```

## **getCityById**
> Swagger\Server\Model\City getCityById($cityId)

Find City by ID

Returns a single City

### Example Implementation
```php
<?php
// src/Acme/MyBundle/Api/CityApiInterface.php

namespace Acme\MyBundle\Api;

use Swagger\Server\Api\CityApiInterface;

class CityApi implements CityApiInterface
{

    /**
     * Configure API key authorization: api_key
     */
    public function setapi_key($apiKey)
    {
        // Retrieve logged in user from $apiKey ...
    }

    // ...

    /**
     * Implementation of CityApiInterface#getCityById
     */
    public function getCityById($cityId)
    {
        // Implement the operation ...
    }

    // ...
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cityId** | **int**| ID of City to return |

### Return type

[**Swagger\Server\Model\City**](../Model/City.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

