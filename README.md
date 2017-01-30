# xCloud - Информация
Система пользовательского управления сервером, манипуляций файлами с рядом системных и вспомогательных ПО. Эту систему можно назвать домашним облаком с поддержкой многозадачности и более расширенным функционалом.
- Разработчик: RVA ( Quareal Foundation )
- Сайт Quareal: https://quareal.ru/
- Сайт проекта ( в разработке ): https://projects.quareal.ru/
- Страница GitHub: https://github.com/rvasources/
![Главная страница](https://github.com/rvasources/xCloud/blob/master/main.jpg)
- Платформы: Desktop, Mobile
- Браузеры: Все современные браузеры с включенным JS
- Серверная часть: PHP, MySQL
- Язык: Русский ( Российская Федерация )

# xCloud - Приложения
В системе есть 3 типа приложений, которые размещены в каталоге ./apps/, информация о них записана в DB.
- Обычное приложение - иконка приложения показывается в рабочей области, открывается через стандартное окно
- Скрытое приложение - не показывается на главной странице, но открывается через окно
- Мини приложение - не показывается на главной странице и контент приложения находится в вкладке уведомления ( например плеер музыки )

Каждое приложение обязательно имеет главный файл `code.php` в котором распологается php код приложения. При создании приложения, вы можете пользоваться API системой по средствам обращения к глобальной переменной `$APP`. Приложения и система общаются по средствам POST запросов. Каждое приложение в конце имеет обязательный `return array(тут параметры, в записимости от приложения);`
![Пример оконного приложения](https://github.com/rvasources/xCloud/blob/master/window.jpg)
В системе имеется ряд стандартных приложений: Настройки, Менеджер памяти, Apps Market, dolphx, Обозреватель картинок, Плеер, Текстовый редактор, Редактор аккаунта. Все приложения от разработчика ( RVA & Quareal ) можно скачать через Apps Market. Сверху окна находится 2 кнопки, желтая - развернуть окно во всю длину, второе - закрыть приложение. В некоторых ситуациях красная кнопка будет вас возвращать в приложение открытое ранее ( если открыто несколько программ ).

# xCloud - Реестры
Предусматриваются несколько реестров. 
- Реестр аккаунтов ( в нем вы создаете аккаунты для авторизации )
- Реестр приложений ( список приложений, их конфигураций )
- Реестр зависимостей ( определяет, какой файл какой программой следует открывать )
Каждый из перечисленных реестров можно редактировать в программе `Настройки`
