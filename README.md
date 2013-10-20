Naming conventions
==================

A collection of abstract naming conventions so I don't have to think about this kind of stuff anymore.

* `Collection`: A group of `CollectionItems`. Example: `BlogPostCollection` has many `BlogPost`s https://github.com/doctrine/collections/blob/master/lib/Doctrine/Common/Collections/ArrayCollection.php
* `CollectionItem`: Belongs to a `Collection`: 
* `Period`: The span of two Dates. Example: http://www.php.net/manual/en/class.dateperiod.php
* `Interval`: A repeating unit in a `Period`. Example: `P2W` http://php.net/manual/en/class.dateinterval.php
* `Range`: An array of elements with a predefined set of steps
* `Criteria`: Any kind of condition / clause for searches, where statements etc
