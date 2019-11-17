# test-phpunit

Using phpunit example to create a test. Link: https://phpunit.de/getting-started/phpunit-8.html

Create a directory and change to it, and execute below command:

```bash
 composer require --dev phpunit/phpunit
```

This will create a composer.json file and a vendor directory with all the code needed to perform your tests. Make sure your composer.json is as follows:

```bash
{
    "autoload": {
        "classmap": [
            "src /"
        ]
    },
    "require-dev": {
        "phpunit / phpunit": "^ 8"
    }
}
```

if versioning your code, create a .gitignore file with this content at https://github.com/sebastianbergmann/phpunit/blob/master/.gitignore

After that check the PHPUnit version with the command below.

```bash
./vendor/bin/phpunit --version
```

Create a src/ directory for the sources and another one named tests/ for the tests classes.

Then create the main class in src/Email.php and the test class tests/EmailTest.php, and run the test using PHPUnit

```bash
./vendor/bin/phpunit --bootstrap vendor/autoload.php tests/EmailTest
```

If "Error: Class 'Email' not found" error message appears, execute the command below:

```json
composer dump 
```

Below is a clearer way to see test results:

```bash
./vendor/bin/phpunit --bootstrap vendor/autoload.php --testdox tests
```
