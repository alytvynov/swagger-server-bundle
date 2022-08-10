# Swagger\Server\Api\PetApiInterface

All URIs are relative to *https://petstore.swagger.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deletePet**](PetApiInterface.md#deletePet) | **DELETE** /pet/{petId} | Deletes a pet
[**getPetById**](PetApiInterface.md#getPetById) | **GET** /pet/{petId} | Find pet by ID
[**updatePetWithForm**](PetApiInterface.md#updatePetWithForm) | **POST** /pet/{petId} | Updates a pet in the store with form data


## Service Declaration
```yaml
# src/Acme/MyBundle/Resources/services.yml
services:
    # ...
    acme.my_bundle.api.pet:
        class: Acme\MyBundle\Api\PetApi
        tags:
            - { name: "swagger_server.api", api: "pet" }
    # ...
```

## **deletePet**
> deletePet($petId, $apiKey)

Deletes a pet



### Example Implementation
```php
<?php
// src/Acme/MyBundle/Api/PetApiInterface.php

namespace Acme\MyBundle\Api;

use Swagger\Server\Api\PetApiInterface;

class PetApi implements PetApiInterface
{

    /**
     * Configure OAuth2 access token for authorization: petstore_auth
     */
    public function setpetstore_auth($oauthToken)
    {
        // Retrieve logged in user from $oauthToken ...
    }

    // ...

    /**
     * Implementation of PetApiInterface#deletePet
     */
    public function deletePet($petId, $apiKey = null)
    {
        // Implement the operation ...
    }

    // ...
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **int**| Pet id to delete |
 **apiKey** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

[petstore_auth](../../README.md#petstore_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

## **getPetById**
> Swagger\Server\Model\Pet getPetById($petId)

Find pet by ID

Returns a single pet

### Example Implementation
```php
<?php
// src/Acme/MyBundle/Api/PetApiInterface.php

namespace Acme\MyBundle\Api;

use Swagger\Server\Api\PetApiInterface;

class PetApi implements PetApiInterface
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
     * Implementation of PetApiInterface#getPetById
     */
    public function getPetById($petId)
    {
        // Implement the operation ...
    }

    // ...
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **int**| ID of pet to return |

### Return type

[**Swagger\Server\Model\Pet**](../Model/Pet.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

## **updatePetWithForm**
> updatePetWithForm($petId, $name, $status)

Updates a pet in the store with form data



### Example Implementation
```php
<?php
// src/Acme/MyBundle/Api/PetApiInterface.php

namespace Acme\MyBundle\Api;

use Swagger\Server\Api\PetApiInterface;

class PetApi implements PetApiInterface
{

    /**
     * Configure OAuth2 access token for authorization: petstore_auth
     */
    public function setpetstore_auth($oauthToken)
    {
        // Retrieve logged in user from $oauthToken ...
    }

    // ...

    /**
     * Implementation of PetApiInterface#updatePetWithForm
     */
    public function updatePetWithForm($petId, $name = null, $status = null)
    {
        // Implement the operation ...
    }

    // ...
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **int**| ID of pet that needs to be updated |
 **name** | **string**| Updated name of the pet | [optional]
 **status** | **string**| Updated status of the pet | [optional]

### Return type

void (empty response body)

### Authorization

[petstore_auth](../../README.md#petstore_auth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

