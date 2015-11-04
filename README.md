# query-mysql-
Change and Update WordPress URLS in Database When Site is Moved to new Host

UPDATE wp_options SET option_value = replace(option_value, 'http://localhost/nomesite', 'http://www.nomesite.com.br') WHERE option_name = 'home' OR option_name = 'siteurl';

UPDATE wp_posts SET guid = replace(guid, 'http://localhost/nomesite','http://www.nomesite.com.br');

UPDATE wp_posts SET post_content = replace(post_content, 'http://localhost/nomesite', 'http://www.nomesite.com.br');
