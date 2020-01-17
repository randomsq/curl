# curl
Get file contents through curl and an example to get share counts through an api using curl
## Method one
```php
<?php
$url = "http://count-server.sharethis.com/v2.0/get_counts?wd=true&url=https://lawstreet.co/executive/pm-modi-denies-the-existence-of-detention-centers/";
//  Initiate curl
$ch = curl_init();
// Will return the response, if false it print the response
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
// Set the url
curl_setopt($ch, CURLOPT_URL,$url);
// Execute
$result=curl_exec($ch);
// Closing
curl_close($ch);

// Will dump a beauty json :3
var_dump(json_decode($result, true));
```
## Method Two
```php
<?php
$result = file_get_contents($url);
// Will dump a beauty json :3
var_dump(json_decode($result, true));
```
