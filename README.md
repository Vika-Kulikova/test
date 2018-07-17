#Базовая структура проекта с настроенными webpack, less, babel
#### LINK https://ilyalytvynov.github.io/wa_group_1905/.
Для использования скачать, разархивировать, и выполнить следующие команды в терминал(командной строке)
1. npm install
2. npm start -команда которая запустит dev сервер, необходимо для авоматической компиляции less/ES6 файлов
3. Перейти в браузере по адресу http://localhost:8080
4. Для остановки дев сервера в консоле(терминале) необходимо нажать два раза CTRL+C
Если возникают ошибки компиляции то в терминале будут красные
сообщения об ошибке, в самом начале сообщения достаточно
точно описывается что пошло не так, обращайте на это внимание. Так же в случае проблем со сборкой просьба к вопросу прикладывать скриншот с текстом ошибки консоли

### Файловая структура

assets - дирректория для хранения асеетов - шрифты изображения пример использования смотреть в common/styles/header.less
###
``` 
src
.
|
├──index - старница index.html и все что к ней относится
|   |
|   +-- scripts - скрипты, обязательно необходимо импортить в index.js  
|   +-- styles - все стили разделенные по файлам, так же необходимо импортить в index.less
|   +-- index.html - основной документ html, домашняя страница вашего сайта
|   +-- index.js - главный фаил js, весь скрипт который относится к данной странице импортится в данном файле(из дирректории scripts)
|   +-- index.less - основной фаил стилей
+- common - дирректория в которой хранятся общие файлы для всех страниц вашего сайта например стили и скрипты для использования нужно имопртить в главных файла страниц смотреть index/index.less
    |
    +- scripts
    |
    +- styles     
```
Если есть неоходимость добавления новой страницы, необходимо создать дирректорию с именем вашей страницы, html, js и less фаил должен называться так же как и имя дирретории пример смотреть src/about. После создания дирректории необходимо подключить данную страницу к вебпак сборке. Открываем config/base.js в entry - добавляем следующую строку имя вашей папки например test, значит строка будет выглядеть как test: ['babel-polyfill', './src/test/test.js'], в итоге entry должен выглядеть как
```
сonst entry = {
        index: ['babel-polyfill', './src/index/index.js'],
        about: ['babel-polyfill', './src/about/about.js'],
        test: ['babel-polyfill', './src/test/test.js']
    };
```

Для перехода на другие страницы не index, в адресной строке добавить к http://localhost:8080 /имя_страницы.html например http://localhost:8080/about.hml

This is the Hello World example from the git tutorial
git commit -m "Changed README in original repo"

This is the Hello World example from the git tutorial
git commit -m "Changed README in original repo"

This is the Hello World example from the git tutorial
git commit -m "Changed README in original repo"
