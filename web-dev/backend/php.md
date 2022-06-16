# PHP
- [PHP Tutorial.net](https://www.phptutorial.net/)
- [PHP Tutorial W3School](https://www.w3schools.com/php/) 
- [PHP in 100 seconds](https://www.youtube.com/watch?v=a7_WFUlFS94)

# Crash Courses
- [Traversy Media - PHP Crash Course](https://www.youtube.com/playlist?list=PLillGF-Rfqbap2IB6ZS4BBBcYPagAjpjn)
- [Traversy Media - PHP for beginner](https://www.youtube.com/watch?v=BUCiSSyIGGU)


# Code Quality & Static Analysis
There are different libraries in PHP that perform code analysis and linting:

- [PHP CS Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) - A coding standards fixer library
- [PHP Mess Detector](https://github.com/phpmd/phpmd) - A library that scans code for bugs, sub-optimal code, unused parameters and more
- [Psalm](https://github.com/vimeo/psalm) - A static analysis tool for finding errors in PHP applications
- [PHPStan](https://github.com/phpstan/phpstan) - A PHP Static Analysis Tool
- [PHPCS Security Audit](https://github.com/FloeDesignTechnologies/phpcs-security-audit) - Set of PHP_CodeSniffer rules that finds vulnerabilities

When developing in PHP we always try to follow the PSR-12 standard, which extends PSR-1 and PSR-2 in terms of coding style.
 
# Testing
There are two main libraries for testing in php. The most famous is [PHPUnit](https://github.com/sebastianbergmann/phpunit), which is part of the X Unit family and is used to write unit tests. Another library used for testing is [PHPSpec](https://github.com/phpspec/phpspec), which is a SpecBDD framework useful for writing behavioral tests. Another interesting library for writing tests is [Infection](https://github.com/infection/infection), which deals with measuring the effectiveness of a set of tests in terms of the ability to detect errors.

# Utility
Below is a set of libraries that can be very useful within any PHP project:

- [php-collections](https://github.com/danielgsims/php-collections) - set of classes to facilitate the use and manipulation of arrays
- [phunctional](https://github.com/Lambdish/phunctional) - little library that tries to bring to PHP some aspects of functional programing
- [functional-php](https://github.com/lstrojny/functional-php) - a set of functional primitives for PHP, heavily inspired by Scala's traversable collection
- [webmozarts-assert](https://github.com/webmozarts/assert): assertions to validate method input / output with nice error messages
- [php-option](https://github.com/schmittjoh/php-option): option type for PHP
- [rector](https://github.com/rectorphp/rector): Instant Upgrades and Automated Refactoring of any PHP code
