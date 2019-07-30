# Biwse PHP Library

This API documentation generated from OpenAPI specification.


## Requirements

PHP 5.5 and later

## Installation 

Install library via Composer. Run the following command:

```bash
composer require biwse/biwse-php
```

## Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = Biwse\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Biwse\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'YOUR_APP_ID'; // string | The application identidier
$coin = 'btc'; // string | The wallet identidier

try {
    $result = $apiInstance->createAddress($app_id, $coin);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->createAddress: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.biwse.com/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AppApi* | [**createAddress**](docs/Api/AppApi.md#createaddress) | **POST** /app/{appId}/{coin}/address | Create new address
*AppApi* | [**createInvoice**](docs/Api/AppApi.md#createinvoice) | **POST** /app/{appId}/invoice | Create invoice
*AppApi* | [**createWalletInvoice**](docs/Api/AppApi.md#createwalletinvoice) | **POST** /app/{appId}/{coin}/invoice | Create wallet invoice
*AppApi* | [**getBalance**](docs/Api/AppApi.md#getbalance) | **GET** /app/{appId}/{coin}/balance | Retrieve wallet balance
*AppApi* | [**getInvoice**](docs/Api/AppApi.md#getinvoice) | **GET** /app/{appId}/invoice/{invoiceId} | Retreive invoice info
*AppApi* | [**sendOnePayment**](docs/Api/AppApi.md#sendonepayment) | **POST** /app/{appId}/{coin}/send | Send one payment
*AppApi* | [**sendPayments**](docs/Api/AppApi.md#sendpayments) | **POST** /app/{appId}/{coin}/multi_send | Send payments


