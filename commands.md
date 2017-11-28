cd laraprojects/
git clone https://github.com/narunbabu/ameyem-quiz.git
cd ~/public_html/skills/
mkdir quiz
cd quiz
cp -r ~/laraprojects/ameyem-quiz/public .
cp -r ~/laraprojects/ameyem-quiz/public/index.php .
cp -r ~/laraprojects/ameyem-quiz/.htaccess .
as there was no .htaccess 
cp -r ~/laratest/public/.htaccess .
cp -r index.php index1.php
cp -r ~/public_html/api/index.php index.php
vi index.php

in .env

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=thogativ_quiz
DB_USERNAME=
DB_PASSWORD=

in database/seeds/UserSeed.php
'name'           => 'Arun',
'email'          => 'ab@ameyem.com', and password

chmod -R o+w storage
/opt/cpanel/ea-php70/root/usr/bin/php artisan config:cache
/opt/cpanel/ea-php70/root/usr/bin/php artisan route:cache

curl -sS https://getcomposer.org/installer | /opt/cpanel/ea-php70/root/usr/bin/php
/opt/cpanel/ea-php70/root/usr/bin/php composer.phar install


php artisan key:generate
/opt/cpanel/ea-php70/root/usr/bin/php composer install

/opt/cpanel/ea-php70/root/usr/bin/php artisan key:generate
/opt/cpanel/ea-php70/root/usr/bin/php artisan migrate --seed
php artisan serve
