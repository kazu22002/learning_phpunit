# learning_phpunit

## 01_init

```
cd docker

docker-compose up -d

composer require --dev phpunit/phpunit ^7

# composer.json編集

composer dump-autoload

./vendor/bin/phpunit --bootstrap vendor/autoload.php tests/EmailTest

./vendor/bin/phpunit --bootstrap vendor/autoload.php --testdox tests

exit
```

composer.json編集

```compose.json
{
    "autoload": {
        "classmap": [
            "src/"
        ]
    },
    "require-dev": {
        "phpunit/phpunit": "^7"
    }
}
```

## reference

[https://phpunit.de/getting-started/phpunit-7.html](phpunit)

