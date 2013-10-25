URLs
====

BREAD
-----

*BREAD* (Browse, Read, Edit, Add, Delete) is preferable to CRUD for browser based sites / apps. 

* [B]rowse: GET         `/projects` or `/projects?where[id][]=1&where[id][]=2`
* [R]ead:   GET         `/projects/1`
* [E]dit:   PATCH|GET   `/projects/1/edit`
* [A]dd:    POST|GET    `/projects/add`
* [D]elete: REMOVE|GET  `/projects/1/delete`

Notes:

* Browse may return a subset of the entity properties and associations
* Read may return all details of the entity properties and associations
* Edit, Add and Delete may have GET endpoints for forms / confirmations

URL Query Parameters
--------------------

Query parameters should be underscore.

References:

* http://www.w3.org/TR/WD-html40-970708/htmlweb.html

### Pagination

Use `?page=` & `?per_page=` for url pagination params. Example: `?page=2&per_page=10`

References:

* https://github.com/whiteoctober/Pagerfanta
* http://developer.github.com/v3/#pagination

### Partial Responses

Use `?select=` for partial responses. Example: `?select[0]['entity']=Project&select[0]['props'][]=id&select[0]['props'][]=title`

References:

* https://developers.google.com/youtube/2.0/developers_guide_protocol_partial
* http://docs.doctrine-project.org/en/latest/reference/partial-objects.html

### Search Criteria

Use `?where=` for query criteria. Example: `?where[titleLike]=Proj`

#### Ranges

Suffix ranges with `Range`

Example: `?where[submittedAtRange][start]=2013-31-01&where[submittedAtRange][end]=2013-31-08&where[submittedAtRange][inclusive]=1`

Ranges contain a sub array of paramaters:

* `start`
* `end`
* `inclusive`

### Result Ordering

Use `?orderBy=` for sort / ordering. 

Example: `?orderBy[0]['prop']=submittedAt&orderBy[0]['sort']=ASC`
