PHP Client for Adobe Connect's API (tested with v9)
==================================================

At the moment, the client not implement methods for all the Adobe Connect's API actions (You're invited to do it :)),
instead, we just implement those that we usually use in our system.

## Installation using [Composer](http://getcomposer.org/)

```bash
$ composer require platforg/adobe-connect
```

## Usage

```php
<?php
require __DIR__ . '/vendor/autoload.php';

$config = new AdobeConnect\Config(
    "your-account.adobeconnect.com",
    "username@gmail.com",
    "password"
);

$client = new AdobeConnect\ApiClient($config);

// Call endpoints
$info = $client->commonInfo();
var_dump($info);

// ...
$scos = $client->scoSearch('term...');
var_dump($scos);
// ...
```

The methods names in the ApiClient class maintain a one-to-one relationship with the [AdobeConnect's endpoints](https://helpx.adobe.com/adobe-connect/webservices/topics/action-reference.html) (in camelCase instead of hyphen).  
Please, see the AdobeConnect\ApiClient for a complete list of endpoints implemented.
Also, you can use/see AdobeConnect\ExtraApiClient for some custom methods.

Frameworks integrations (third-party):
-------------------------------------
- [Laravel](https://github.com/asimov-express/laravel-adobe-connect)


Todo:
-----

- Add unit test.
- Implement more methods.
- Add Documentation.

- - -

*Note: We don't have any relation with Adobe.*
