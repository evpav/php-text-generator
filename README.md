# php-text-generator
Fast SEO text generator on a mask.

Written in PHP. I do not use regular expressions and the fastest.
I covered tests and simple! Supporting recursive text generation rules.
It supports multiple encodings.

This package implements the functionality of a similar package for Go Lang – [text-generator](https://github.com/liderman/text-generator).

Installation
------------

    composer install liderman/php-text-generator
    
Usage
-----
An example of a simple template text generation:
```php
$textGen = new TextGenerator();
echo $textGen->generate("Good {morning|day}!");
// Displays: Good morning!
// or
// Good day!
```

An example of a complex generation template text:
```php
$textGen = new TextGenerator();
echo $textGen->generate("{Good {morning|evening|day}|Goodnight|Hello}, {friend|brother}! {How are you|What's new with you}?");
// Displays: Good morning, friend! How are you?
// or
// Good day, brother! What's new with you?
// or
// Hello, friend! How are you?
// ...
```

Features
--------
* It supports multiple encodings
* Supporting recursive text generation rules
* Fast! Does not use regular expressions
* Easy wrapping thanks to the integrated interface
* Covered tests
* Written by PSR standards and 100% covered with documentation (PHP-Doc)

Requirements
-----------

* PHP >= 5.5.9.

