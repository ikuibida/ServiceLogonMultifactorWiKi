Самым простым способом является запустить консольную программу [ConsoleReadTelegramBot.exe](https://github.com/Constantine-SRV/ServiceLogonMultifactor/blob/master/downloadAll/ConsoleReadTelegramBot.exe) 

Ввести полученный ранее BotId, попросить пользователей написать этому боту свой логин и скопировать отображённые ChatId.

Обратите внимание, что иногда пользователям вначале надо написать 2-3 сообщения боту, чтобы сообщения появились, далее все работает с первого сообщения.

Пример окна приложения:

![ConsoleReadTelegramBot.JPG](https://github.com/Constantine-SRV/ServiceLogonMultifactor2/blob/master/documentation/ConsoleReadTelegramBot.JPG)

В качестве альтернативы можно ввести в браузер ссылку вида https ://api.telegram.org/bot{_**botid**_}/getUpdates
https://api.telegram.org/bot1705365690:AAFJNFTPcvPd_oOGsV4rfU3O3v4oNnyasNI/getUpdates

и взять ChatId из результата:

![chatIdFromBrowser.JPG](https://github.com/Constantine-SRV/ServiceLogonMultifactor2/blob/master/documentation/chatIdFromBrowser.JPG)