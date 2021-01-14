#### Reset file/folder permissions
````
Folder permission 755
File permission 644
````

#### Change url in MySQL database after domain migration
> NOTE: We recommend to make a backup of your MySQL database before executing the lines above.
````
UPDATE wp_options SET option_value = replace(option_value, 'http://www.myOldUrl.tld', 'http://www.myNewUrl.tld') WHERE option_name = 'home' OR option_name = 'siteurl';
UPDATE wp_posts SET guid = replace(guid, 'http://www.myOldUrl.tld','http://www.myNewUrl.tld');
UPDATE wp_posts SET post_content = replace(post_content, 'http://www.myOldUrl.tld', 'http://www.myNewUrl.tld');
UPDATE wp_postmeta SET meta_value = replace(meta_value,'http://www.myOldUrl.tld','http://www.myNewUrl.tld');
````
