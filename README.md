## VNPay Integration for Laravel
This package provides a simple integration for VNPay payment gateway with Laravel web applications.

### Installation
To install the package, simply run the following command:

``` javascript
composer require your-username/vnpay-laravel
```
Next, publish the configuration file by running the following command:

``` lua
php artisan vendor:publish --tag=vnpay
```
This will create a vnpay.php file in your application's config directory.

### Usage
To create a new payment, you can use the VNPayment class provided by the package, like so:

```php
use App\Http\Services\VNPay\src\Models\VNPayment;

$payment = new VNPayment($txnRef, $amount, $orderInfo, $returnUrl);
$vnpUrl = $payment->execute();
```
To handle the return from VNPay, you can use the following code in your controller:

```php
use App\Http\Services\VNPay\src\Models\VNPayment;

if (VNPayment::checkSum($_GET)) {
    // Process payment success
} else {
    // Process payment failed
}
```
## Configuration
The config/vnpay.php file contains the necessary configuration for VNPay integration. You will need to provide your own VNPay credentials and settings in this file.

```php
return [
    'tmn_code' => env('VN_TMN_CODE', ''),
    'hash_secret' => env('VN_HASH_SECRET', ''),
    'vnp_url' => env('VN_VNP_URL', 'http://sandbox.vnpayment.vn/merchant_webapi/merchant.html'),
    'payment_type' => env('VN_PAYMENT_TYPE', 'ATM'),
    'bank_code' => env('VN_BANK_CODE', ''),
];
```
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
This package is licensed under the MIT License.
