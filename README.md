# PHP-dotenv-Parser

## Usage

```php
include __DIR__.'DotEnv.php';

$dotEnv = DotEnv::getInstance();

// make the class look for the file.
$data = $dotEnv->read();

// or specify the .env file directly.
// $data = $dotEnv->read('/path/to/.env');

// Updates env, $_ENV, $_SERVER if the value doesn't exist already
$dotEnv->updateEnv($data);

// override any existing values
$dot_env->updateEnv($data, true);

// 
$dotEnv->defineConsts($data);

// OR define the consts with this prefix
// 
// $dot_env->defineConsts($data, 'MY_APP_');

// Get an ENV variable.
$dotEnv->get('ENV');

// Checks for several ENV variables until it finds a value.
$dotEnv->get('ENV, APP_ENV');
```

```env
# You can have comments
ENV=dev
db_name = orbisius_db
db_user = orbisius_user
db_pass = orbisius_pass # you can have a comment here too

# Leave some lines blank
api_url = http://

author_url = https://orbisius.com
author_product_1_url = https://orbisius.com
author_product_2_url = https://qsandbox.com
author_product_3_url = https://wpsandbox.net
author_product_4_url = https://wpdemo.net
author_product_5_url = https://go359.com
```
