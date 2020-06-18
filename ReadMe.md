# PhpStorm + Docker + Xdebug
#### 1 sudo chomod 777 /var/run/docker.sock
#### 2 Add Docker Server
> Если он у Вас еще не добавлен, конечно. Для этого откройте настройки: «Build, Execution, Deployment» — Docker. Затем нажмите плюсик, чтобы добавить новое подключение к докеру. У меня все подключилось сразу же в режиме Unix socket. Нажмите Apply.

#### 3 Add external interpreter
> «Languages & Frameworks» — PHP
> From Docker….\
> Always start a new container
#### 4 Проверить конфигурацию Xdebug
> Откройте настройки: «Languages & Frameworks» — PHP — Debug. И нажмите на ссылку Validate.
#### 5 Добавить PHP сервер
> Откройте настройки: «Languages & Frameworks» — PHP — Servers и нажмите плюсик, чтобы добавить новый.
> Укажите имя сервера Docker (должно совпадать с переменной окружения PHP_IDE_CONFIG в docker-compose.yml) и хост 127.0.0.1. Затем ниже включите опцию Use path mappings и укажите соответствие между локальным каталогом проекта и этим же каталогом проекта внутри Docker-контейнера. Это соответствие изначально настраивается в docker-composer.yml для службы php-fpm в разделе volumes. Затем нажмите OK.
#### 6 Добавить конфигурацию для запуска
> Остался последний штрих — добавление конфигурации запуска. Мы добавим простую Web-страницу.

## Full instructions here -> [PhpStorm + Docker + Xdebug](https://blog.denisbondar.com/post/phpstorm_docker_xdebug)
