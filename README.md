Обязательно проверить .htaccess и работу mod_rewrite
Должен быть включен AllowOverRide в настройка virtualhost

Для файлов сайта на Wordpress права 775 и пользователь www-data
	chmod -R 775 *
	chown -R www-data:www-data *
	
Для дампа базы данных также выставить такие же разрешения 
	chmod -R 775 *
	chown -R www-data:www-data *

Настройка соединения с базой данных в файле wp-config.php

// ** Параметры MySQL: Эту информацию можно получить у вашего хостинг-провайдера ** //
/** Имя базы данных для WordPress */
define( 'DB_NAME', getenv('DB_DB') );

/** Имя пользователя MySQL */
define( 'DB_USER', getenv('DB_USER') );

/** Пароль к базе данных MySQL */
define( 'DB_PASSWORD', getenv('DB_PASS') );

/** Имя сервера MySQL */
define( 'DB_HOST', getenv('DB_HOST') );




!!!! Дальше подключиться к phpmyadmin изменить homeurl и siteurl в таблице wp_options !!!
