# test-phpunit

using phpunit example to create a test

from: https://phpunit.de/getting-started


Create a directory and change to him, and execute below command:

 composer require --dev phpunit/phpunit

This will create a composer.json file and a vendor directory with all the code needed to perform your tests. Make sure your composer.json is as follows:

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

If you versed your code, create a .gitignore file with this content at https://github.com/sebastianbergmann/phpunit/blob/master/.gitignore

After that check the PHPUnit version with the command below.

./vendor/bin/phpunit --version

I created src directory / where the sources were and the tests directory / where the tests were.

Then create the main class in src / Email.php and the test class tests / EmailTest.php

Run the test using PHPUnit

./vendor/bin/phpunit --bootstrap vendor / autoload.php tests / EmailTest

If "Error: Class 'Email' not found" error message appears, execute the command below:

 dump composer

Below is a more readable way to see test results:

./vendor/bin/phpunit --bootstrap vendor / autoload.php --testdox tests