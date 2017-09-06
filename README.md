# WordPress-coding-best-practices
Some tips develop a plugin or theme for WordPress without affecting the users site.

1.Do not use require to add a file.

`require PLUGIN_DIR . 'Exception/Exception.php';`

If something breaks in the updates then Exception.php is missing from the update process somehow then your plugin give you fatal error and break the site completely. So always 

`include_once ( PLUGIN_DIR . 'Exception/Exception.php' );`

