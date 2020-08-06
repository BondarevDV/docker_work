
Запуск

docker-compose up

После запуска обязательно зайдите в Администрирование и во всплывающем сообщении нажмите Загрузить схему данных, иначе могут не работать многие функции.

Если хочется ещё и отправки уведомлений на почту, то пишем файл configuration.yml

nano ~/docker/storage/configuration.yml 

с примерно таким содержимым. Настройки почты для каждого отдельного сервиса, будь то gmail, yandex или rambler свои

 production:
   email_delivery:
     delivery_method: :smtp
     smtp_settings:
       enable_starttls_auto: true
       address: "smtp.gmail.com"
       port: 587
       domain: "smtp.gmail.com"
       authentication: :plain
       user_name: "your_email@gmail.com"
       password: "password" 
