Обязательно проверить .htaccess и работу mod_rewrite
Должен быть включен AllowOverRide в настройка virtualhost

Для файлов сайта на Wordpress права 775 и пользователь www-data
	chmod -R 775 *
	chown -R www-data:www-data *
