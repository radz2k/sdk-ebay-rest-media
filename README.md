# SwaggerClient-php
The <b>Media API</b> lets sellers to create, upload, and retrieve files, including:<ul><li>videos</li><li>documents (for GPSR regulations)</li></ul>

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: v1_beta.2.0
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/git_user_id/git_repo_id.git"
    }
  ],
  "require": {
    "git_user_id/git_repo_id": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: api_auth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$content_type = "content_type_example"; // string | This header indicates the format of the request body provided by the client. Its value should be set to <b>application/json</b>. <br><br> For more information, refer to <a href=\"/api-docs/static/rest-request-components.html#HTTP\" target=\"_blank \">HTTP request headers</a>.
$body = new \Swagger\Client\Model\CreateDocumentRequest(); // \Swagger\Client\Model\CreateDocumentRequest | 

try {
    $result = $apiInstance->createDocument($content_type, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentApi->createDocument: ', $e->getMessage(), PHP_EOL;
}

// Configure OAuth2 access token for authorization: api_auth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = "document_id_example"; // string | The unique identifier of the document for which status and metadata is being retrieved.<br><br>This value is returned in the response of the <a href=\"/api-docs/commerce/media/resources/document/methods/createDocument\" target=\"_blank\">createDocument</a> method.

try {
    $result = $apiInstance->getDocument($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentApi->getDocument: ', $e->getMessage(), PHP_EOL;
}

// Configure OAuth2 access token for authorization: api_auth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = "document_id_example"; // string | The unique identifier of the document to be uploaded.<br><br>This value is returned in the response of the <a href=\"/api-docs/commerce/media/resources/document/methods/createDocument\" target=\"_blank\">createDocument</a> method.
$content_type = "content_type_example"; // string | This header indicates the format of the request body provided by the client. Its value should be set to <b>multipart/form-data</b>. <br><br> For more information, refer to <a href=\"/api-docs/static/rest-request-components.html#HTTP\" target=\"_blank \">HTTP request headers</a>.

try {
    $result = $apiInstance->uploadDocument($document_id, $content_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentApi->uploadDocument: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *https://apim.ebay.com{basePath}*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DocumentApi* | [**createDocument**](docs/Api/DocumentApi.md#createdocument) | **POST** /document | 
*DocumentApi* | [**getDocument**](docs/Api/DocumentApi.md#getdocument) | **GET** /document/{document_id} | 
*DocumentApi* | [**uploadDocument**](docs/Api/DocumentApi.md#uploaddocument) | **POST** /document/{document_id}/upload | 
*VideoApi* | [**createVideo**](docs/Api/VideoApi.md#createvideo) | **POST** /video | 
*VideoApi* | [**getVideo**](docs/Api/VideoApi.md#getvideo) | **GET** /video/{video_id} | 
*VideoApi* | [**uploadVideo**](docs/Api/VideoApi.md#uploadvideo) | **POST** /video/{video_id}/upload | 

## Documentation For Models

 - [CreateDocumentRequest](docs/Model/CreateDocumentRequest.md)
 - [CreateDocumentResponse](docs/Model/CreateDocumentResponse.md)
 - [CreateVideoRequest](docs/Model/CreateVideoRequest.md)
 - [DocumentMetadata](docs/Model/DocumentMetadata.md)
 - [DocumentResponse](docs/Model/DocumentResponse.md)
 - [Error](docs/Model/Error.md)
 - [ErrorParameter](docs/Model/ErrorParameter.md)
 - [Image](docs/Model/Image.md)
 - [InputStream](docs/Model/InputStream.md)
 - [Moderation](docs/Model/Moderation.md)
 - [Play](docs/Model/Play.md)
 - [Video](docs/Model/Video.md)

## Documentation For Authorization


## api_auth

- **Type**: OAuth
- **Flow**: accessCode
- **Authorization URL**: https://auth.ebay.com/oauth2/authorize
- **Scopes**: 
 - **https://api.ebay.com/oauth/api_scope/sell.inventory**: View and manage your inventory and offers


## Author



