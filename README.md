# mysql-php-api
## the R in REST API

Simple PHP to read MySQL and serve as JSON API for web applications

Change the config.php file to match the DB

```
// the first argument is the route and the secund is the query
// the route can have 1 or 2 parts
// with 1 part will return a multi level array
// with 2 parts will return a simple array
//    the first is compared to the http call
//    the secund is the variable name that can be used inside the query

$paths = [
    [
      '/projects',
      'SELECT * FROM public_projects'
    ],[
      '/projects/id',
      'SELECT * FROM public_projects WHERE id = $id'
    ],[
      '/projectsname/name',
      'SELECT * FROM public_projects WHERE name_id LIKE $name'
    ],[
      '/social',
      'SELECT * FROM public_social'
    ],[
      '/highlights',
      'SELECT * FROM public_highlights'
    ]
];

router($paths);
```
