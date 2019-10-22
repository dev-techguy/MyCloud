# <p align="center"><a href="https://tpay.co.ke/" target="_blank"><img src="https://tpay.co.ke/img/logo-black.png"></a></p>

<p align="center">
  <b>Make It Happen</b><br>
  <a href="https://github.com/dev-tecksolke/tecksolke-tpay-app-api/issues">
  <img src="https://img.shields.io/github/issues/dev-tecksolke/tecksolke-tpay-app-api.svg">
  </a>
  <a href="https://github.com/dev-tecksolke/tecksolke-tpay-app-api/network/members">
  <img src="https://img.shields.io/github/forks/dev-tecksolke/tecksolke-tpay-app-api.svg">
  </a>
  <a href="https://github.com/dev-tecksolke/tecksolke-tpay-app-api/stargazers">
  <img src="https://img.shields.io/github/stars/dev-tecksolke/tecksolke-tpay-app-api.svg">
  </a>
  <br><br>
  <img src="http://s.4cdn.org/image/title/105.gif">
</p>

T-Pay API is REST-API that makes it easy for one to make request to the T-Pay Payment Gateway for his/her App.

- The API is simple and easy to install.
- Has both B2C and C2B API for your App's.
- The API can only be used by those having apps, in T-Pay Payment Gateway.
- The API is based on PHP *[Laravel Framework](https://laravel.com/)*. But you can try to install and customize it basing on your *PHP* development platform.

## Help and docs

- [API Documentation](https://dev.tpay.co.ke/)


## Installing

The recommended way to install tpay-api is through
[Composer](http://getcomposer.org).

```bash
# Install package via composer
composer require tecksolke-tpay/app-api
```

Next, run the Composer command to install the latest stable version of *tpay/api*:

```bash
# Update package via composer
 composer update tecksolke-tpay/app-api --lock
```

After installing, the package will be auto discovered, But if need you may run:

```php
# run for auto discovery <-- If the package is not detected automatically -->
composer dump-autoload
```

Then run this, to get the *config/tpay.php* for api configurations:

```php
# run this to get the configuartion file at config/tpay.php <-- read through it -->
php artisan vendor:publish --provider="TPay\API\TPayServiceProvider"
```

You will have to provide this in the *.env* for the api configurations:

```php
# https://sandbox.tpay.co.ke/api/t-pay/v1/oauth2/
T_PAY_END_POINT_URL=

# TP4*****82F <-- keep this key secret -->
T_PAY_APP_KEY=

# <-- keep this code secret -->
T_PAY_APP_SECRET_CODE=

# 60 <-- The access token session lifetime is in minutes i.e 60 minutes --> ->default(58 minutes);
T_PAY_TOKEN_SESSION=

# 120 <-- Response timeout 120 seconds -->
# This is not a must you may choose to use the dafault value defined in the config/tpay.php;
T_PAY_RESPONSE_TIMEOUT=

# 60 <-- Connection timeout 60 seconds -->
# This is not a must you may choose to use the dafault value defined in the config/tpay.php;
T_PAY_CONNECTION_TIMEOUT=
```

## Usage
Follow the steps below on how to use the api:

#### How to use the API
This how the api will be accessed via this package...

```php
     /**
        * ---------------------------------
        *  Test for requesting app balance
        * ---------------------------------
        * @throws \Exception
        */
       public function appBalance() {
           try {
               //Set request options as shown here
               $options = [
                   'secretCode' => '',//This has to be your app T_PAY_APP_SECRET_CODE
               ];
   
               //make request here
               $response = AppBalances::appBalances($options);
   
               //continue with what you what to do with the $response here
           } catch (\Exception $exception) {
               //TODO If an exception occurs
           }
       }
   
       /**
        * ------------------------------------
        * Making app stk push request for c2b
        * ------------------------------------
        */
       public function appC2BSTKPush() {
           try {
               //Set request options as shown here
               $options = [
                   'secretCode' => '',//This has to be your app T_PAY_APP_SECRET_CODE
                   'phoneNumber' => '',//The phone number has to be 2547xxxxxxx
                   'referenceCode' => '',//The secret code should be unique in every request you send and must start with TPXXXX
                   'amount' => 1,//Amount has to be an integer and less than or equal to KES 70000
                   'resultURL' => '',//This has to be your callback i.e https://mydomain/callback or http://mydomain/callback
               ];
   
               //make the c2b stk push here
               $response = AppC2BSTKPush::appC2BSTKPush($options);
   
               //continue with what you what to do with the $response here
           } catch (\Exception $exception) {
               //TODO If an exception occurs
           }
       }
   
       /**
        * ------------------------------------
        * Making app withdraw request for b2c
        * ------------------------------------
        */
       public function appB2C() {
           try {
               //Set request options as shown here
               $options = [
                   'secretCode' => '',//This has to be your app T_PAY_APP_SECRET_CODE
                   'phoneNumber' => '',//The phone number has to be 2547xxxxxxx
                   'referenceCode' => '',//The secret code should be unique in every request you send and must start with TPXXXX
                   'amount' => 1,//Amount has to be an integer and has to be greater than KES 10
                   'resultURL' => '',//This has to be your callback i.e https://mydomain/callback or http://mydomain/callback
               ];
   
               //make the b2c withdraw here
               $response = AppB2C::appB2C($options);
   
               //continue with what you what to do with the $response here
           } catch (\Exception $exception) {
               //TODO If an exception occurs
           }
       }
    
    
```

## Version Guidance

| Version | Status     | Packagist           | Namespace    | Repo                |
|---------|------------|---------------------|--------------|---------------------|
| 1.x     | Latest     | `tecksolke-tpay/app-api` | `TPay\API` | [v1.0.0](https://github.com/dev-tecksolke/tecksolke-tpay-app-api/tree/1.0)|

[tpay-api-1-repo]: https://github.com/dev-tecksolke/tpay-api.git

## Security Vulnerabilities
 For any security vulnerabilities, please email to [TecksolKE](mailto:client@tecksol.co.ke).
 
## License
 This package is open-source API licensed under the [MIT license](https://opensource.org/licenses/MIT).
