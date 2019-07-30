# Biwse\AppApi

All URIs are relative to *https://api.biwse.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createAddress**](AppApi.md#createAddress) | **POST** /app/{appId}/{coin}/address | Create new address
[**createInvoice**](AppApi.md#createInvoice) | **POST** /app/{appId}/invoice | Create invoice
[**createWalletInvoice**](AppApi.md#createWalletInvoice) | **POST** /app/{appId}/{coin}/invoice | Create wallet invoice
[**getBalance**](AppApi.md#getBalance) | **GET** /app/{appId}/{coin}/balance | Retrieve wallet balance
[**getInvoice**](AppApi.md#getInvoice) | **GET** /app/{appId}/invoice/{invoiceId} | Retreive invoice info
[**sendOnePayment**](AppApi.md#sendOnePayment) | **POST** /app/{appId}/{coin}/send | Send one payment
[**sendPayments**](AppApi.md#sendPayments) | **POST** /app/{appId}/{coin}/multi_send | Send payments



## createAddress

> \Biwse\Model\Address createAddress($app_id, $coin)

Create new address

Create new receive address for yor wallet.

### Example

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
$app_id = 'app_id_example'; // string | The application identidier
$coin = 'coin_example'; // string | The wallet identidier

try {
    $result = $apiInstance->createAddress($app_id, $coin);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->createAddress: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app_id** | **string**| The application identidier |
 **coin** | **string**| The wallet identidier |

### Return type

[**\Biwse\Model\Address**](../Model/Address.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## createInvoice

> \Biwse\Model\AppInvoiceCreated createInvoice($app_id, $app_invoice)

Create invoice

Create new invoice. In response you get url of invoice page

### Example

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
$app_id = 'app_id_example'; // string | The application identidier
$app_invoice = new \Biwse\Model\AppInvoice(); // \Biwse\Model\AppInvoice | 

try {
    $result = $apiInstance->createInvoice($app_id, $app_invoice);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->createInvoice: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app_id** | **string**| The application identidier |
 **app_invoice** | [**\Biwse\Model\AppInvoice**](../Model/AppInvoice.md)|  |

### Return type

[**\Biwse\Model\AppInvoiceCreated**](../Model/AppInvoiceCreated.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## createWalletInvoice

> \Biwse\Model\WalletInvoiceCreated createWalletInvoice($app_id, $coin, $wallet_invoice)

Create wallet invoice

Create new invoice for specific wallet. In response you get url of invoice page.

### Example

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
$app_id = 'app_id_example'; // string | The application identidier
$coin = 'coin_example'; // string | The wallet identidier
$wallet_invoice = new \Biwse\Model\WalletInvoice(); // \Biwse\Model\WalletInvoice | 

try {
    $result = $apiInstance->createWalletInvoice($app_id, $coin, $wallet_invoice);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->createWalletInvoice: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app_id** | **string**| The application identidier |
 **coin** | **string**| The wallet identidier |
 **wallet_invoice** | [**\Biwse\Model\WalletInvoice**](../Model/WalletInvoice.md)|  |

### Return type

[**\Biwse\Model\WalletInvoiceCreated**](../Model/WalletInvoiceCreated.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getBalance

> \Biwse\Model\WalletBalance getBalance($app_id, $coin)

Retrieve wallet balance

Retrieve wallet confirmed and total balance

### Example

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
$app_id = 'app_id_example'; // string | The application identidier
$coin = 'coin_example'; // string | The wallet identidier

try {
    $result = $apiInstance->getBalance($app_id, $coin);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->getBalance: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app_id** | **string**| The application identidier |
 **coin** | **string**| The wallet identidier |

### Return type

[**\Biwse\Model\WalletBalance**](../Model/WalletBalance.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getInvoice

> \Biwse\Model\InvoiceStatus getInvoice($app_id, $invoice_id)

Retreive invoice info

Retrieve invoice with specified identifier string

### Example

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
$app_id = 'app_id_example'; // string | The application identidier
$invoice_id = 'invoice_id_example'; // string | Invoice ID

try {
    $result = $apiInstance->getInvoice($app_id, $invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->getInvoice: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app_id** | **string**| The application identidier |
 **invoice_id** | **string**| Invoice ID |

### Return type

[**\Biwse\Model\InvoiceStatus**](../Model/InvoiceStatus.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## sendOnePayment

> \Biwse\Model\Transaction sendOnePayment($app_id, $coin, $payment)

Send one payment

Send one payments from wallet to one recipient

### Example

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
$app_id = 'app_id_example'; // string | The application identidier
$coin = 'coin_example'; // string | The wallet identidier
$payment = new \Biwse\Model\Payment(); // \Biwse\Model\Payment | 

try {
    $result = $apiInstance->sendOnePayment($app_id, $coin, $payment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->sendOnePayment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app_id** | **string**| The application identidier |
 **coin** | **string**| The wallet identidier |
 **payment** | [**\Biwse\Model\Payment**](../Model/Payment.md)|  |

### Return type

[**\Biwse\Model\Transaction**](../Model/Transaction.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## sendPayments

> \Biwse\Model\Transaction sendPayments($app_id, $coin, $payments)

Send payments

Send payments from wallet to one or many recipents

### Example

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
$app_id = 'app_id_example'; // string | The application identidier
$coin = 'coin_example'; // string | The wallet identidier
$payments = new \Biwse\Model\Payments(); // \Biwse\Model\Payments | 

try {
    $result = $apiInstance->sendPayments($app_id, $coin, $payments);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->sendPayments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app_id** | **string**| The application identidier |
 **coin** | **string**| The wallet identidier |
 **payments** | [**\Biwse\Model\Payments**](../Model/Payments.md)|  |

### Return type

[**\Biwse\Model\Transaction**](../Model/Transaction.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

