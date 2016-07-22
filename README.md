# Opencart-2.2
Opencart 2.2 SSL make admin doesn't work solution


system/library/url.php

if ($this->ssl && $secure) {
			$url = 'https://' . $_SERVER['HTTP_HOST'] . rtrim(dirname($_SERVER['SCRIPT_NAME']), '/.\\') . '/index.php?route=' . $route;
		} else {
			$url = 'http://' . $_SERVER['HTTP_HOST'] . rtrim(dirname($_SERVER['SCRIPT_NAME']), '/.\\') . '/index.php?route=' . $route;
		}
		
		
		change to
		
		
if ($this->ssl && $secure) {
			$url = 'https://' . $_SERVER['HTTP_HOST'] . rtrim(dirname($_SERVER['SCRIPT_NAME']), '/.\\') . '/index.php?route=' . $route;
		} else {
			$url = 'https://' . $_SERVER['HTTP_HOST'] . rtrim(dirname($_SERVER['SCRIPT_NAME']), '/.\\') . '/index.php?route=' . $route;
		}
		
		
		
system/config/catalog.php and system/config/admin.php.

Set

$_['site_ssl'] = false;

to
$_['site_ssl'] = true;


it should works good , not more http url shows in open cart 2.2 and admin should works good too.


if you still have question,it's ok leave comment to me.

THe example website for opencart 2.2 with https(SSL)  https://8pmshop.com
