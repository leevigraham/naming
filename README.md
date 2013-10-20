Naming conventions
==================

A collection of abstract thoughts and naming conventions.

Objects
-------

* `Collection`: A group of `CollectionItems`. Example: `BlogPostCollection` has many `BlogPost`s https://github.com/doctrine/collections/blob/master/lib/Doctrine/Common/Collections/ArrayCollection.php
* `CollectionItem`: Belongs to a `Collection`: 
* `Period`: The span of two Dates. Example: http://www.php.net/manual/en/class.dateperiod.php
* `Interval`: A repeating unit in a `Period`. Example: `P2W` http://php.net/manual/en/class.dateinterval.php
* `Range`: An array of elements with a predefined set of steps
* `Criteria`: Any kind of condition / clause for searches, where statements etc

Relationships
-------------

* Access major relationships through repository methods rather than getters.
  * Smaller joins on initial object load
  * Allows filtering on relationship
* Consider  [preloading loading `many to one` and `one to one`](http://whitewashing.de/2013/02/19/extending_symfony2__paramconverter.html)

URLS
----

* *BREAD* is preferable to CRUD. Browse, Read, Edit, Add, Delete
  * Browse: GET `/projects`
  * Read: GET `/projects/1`
  * Edit: PATCH `/projects/1`
  * Add: POST `/projects`
  * Delete: REMOVE `/projects/1`
* `?page=` & `?perPage=` for url pagination params. Example: `?page=2&perPage=10`
* `?orderBy=` for sort / ordering. Example: `?orderBy=submittedAt:ASC,totalPrice:DESC`.
* `?select=` for partial responses. Example: `?select=Project.{id,title}` 
  * https://developers.google.com/youtube/2.0/developers_guide_protocol_partial
  * http://docs.doctrine-project.org/en/latest/reference/partial-objects.html
