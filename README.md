![Green Kukuruznick](https://i.ibb.co/x2P8hg8/kukuruz.jpg)
# Мы поможем вам найти самые дешёвые авиабилеты.

## Поиск и сравнение цен на авиабилеты среди 200 агентств и 500 авиакомпаний.

**Зеленый Кукурзник** — поисковик авиабилетов по всему миру. 
По вашему запросу мы ищем все варианты перелета, а потом направляем вас для покупки на официальные сайты авиакомпаний и агентств.

**А теперь поподробней: в чем же преимущества нашей платформы?**

1. ***Стоимость билетов***

  > Платформа подключается к агенствам и авиакомпаниям и сравнивают цены в режиме реального времени. В выдаче вариантов вы получаете лучшую цену на конкретный билет.

2. ***Онлайн обмен***

  > Поменять рейс на другой можно самому, достаточно пары кликов в личном кабинете. Система автоматически подберет удобные варианты.

3. ***100% возврат***

  > Можно сдать невозвратный билет на самолет и получить все деньги назад.

4. ***Поддержка 24/7***

  > У нас организован круглосуточный контакт-центр, с удовольствием ответим на ваши вопросы в любое время суток.
  >

## Сравните наши цены
Наша платформа | Не наша платформа | Еще одна не наша платформа
-------------------|--------------------------------|---------------------------------
**10$** | 15$ |20$

# Как работает наша платформа

## Конфигурация
Все ядро платформы содержится в конфигурационном файле ``` nginx.conf ```. Файл конфигурации может быть в любом из следующих мест: ```$HOME/.nginx```, ```$HOME/.nginx/config```, ```$HOME/.config/nginx```, ```$HOME/.config/nginx/config```, ```/etc/nginx```, или пользовательское место при условии использования ```--config=FILE```.

Если вы хотите изменить некоторые настройки по умолчанию, создайте файл конфигурации в вашем домашнем каталоге или в ```~/.config/nginx.conf```  
**Вот пример файла конфигурации:**

```
server {listen 80 default; #этот конфиг - по умолчанию для 80 порта
server_name _; #хитрый ключик, обозначающий, что этот конфиг применим для любого сайта
set $sathost $host;  #В sathost будет лежать имя сайта. Так же должна называться директория 
if ( $host ~ ^(www\.)?(.+)$ ) 
{set $sathost $2;}
root   /var/www/all/$sathost; #корень сайта определяем автоматически
index index.php index.html index.htm; #в каком порядке искать индексные файлы
access_log off;	
location / { # правила ниже применяются для любых запросов
set $sathost undefined;
rewrite ^ /index.php last;}
```

## Опции

- `-v, --version`: Отображение номера версии.
- `--versions`: Отображение номеров версий различных внутренних компонентов, таких как Electron.
- `-h, --help`: Показать инструкции по использованию.
- `-d, --devtools`: Открыть с инструментами разработчика.

## Авторы

@Timmonn

## Информация о лицензии
[Посмотреть лицензию](https://ru.wikipedia.org)
