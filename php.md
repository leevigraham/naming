PHP / Symofny2 Stuff
====================

Code Style
----------

* Follow [Symonfy2](http://symfony.com/doc/current/contributing/code/standards.html) coding standards which follow [PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md), [PSR-1](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md) & [PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md)
* 4 Spaces not Tabs
* https://github.com/opensky/Symfony2-coding-standard

Relationships
-------------

* Access major relationships through repository methods rather than getters.
  * Smaller joins on initial object load
  * Allows filtering on relationship
* Consider  [preloading loading `many to one` and `one to one`](http://whitewashing.de/2013/02/19/extending_symfony2__paramconverter.html)

DocBlock / Annotations
----------------------

* Follow [Symonfy2](http://symfony.com/doc/current/contributing/code/standards.html)

### Exceptions

* Symonfy2 custom annotations are after the description / long description and before `@params`
* Symfony2 custom annotations are split with a line break and boundaried by blank lines

```php
/**
 * Description
 *
 * Longer description
 *
 * @View(...)
 * @Route(...)
 *
 * @param string $dummy Some argument description
 * @param array  $options
 *
 * @return string|null Transformed input
 *
 * @throws \RuntimeException
 */
```
