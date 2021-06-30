Если Вы не хотите использовать инсталлятор, при самостоятельной компиляции исполнительного файла из исходных кодов, либо хотите чтобы этот сервис не появлялся в списке установленных программ, то данный сервис можно установить с помощью стандартной утилиты InstallUtil.exe.

Положите скомпилированный или [скачанный](https://github.com/Constantine-SRV/ServiceLogonMultifactor/blob/master/downloadAll/ServiceLogonMultifactor.exe) файл ServiceLogonMultifactor.exe в рабочий каталог, [отредактируйте ](https://github.com/Constantine-SRV/ServiceLogonMultifactor/wiki/RU-3.-Начальные-настройки.) и положите рядом файл Service.Config.xml 

Далее из командной строки или PowerShell с правами администратора:
 
Установка:

    C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe <your folder>ServiceLogonMultifactor.exe

Первый запуск (в дальнейшем сервис запускается автоматически):
 
    net start ServiceLogonMultifactor

Удаление:
 
    C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe /u <your folder>ServiceLogonMultifactor.exe

Установка сервиса с нестандартным именем и описанием:

По умолчанию сервис будет называться "ServiceLogonMultifactor" с описанием "Service for logging of logon and unlock events and send notification to telegram bot".
Задание другого названия и описания возможно с помощью InstallUtil.exe с параметрами /ServiceName=  и /description=.

    C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe /ServiceName=”service101” /description=”test service 101”    <your_folder>ServiceLogonMultifactor.exe

<img src="https://github.com/Constantine-SRV/ServiceLogonMultifactor/blob/master/documentation/ServiceCustomName.jpg" style="width:7.75in;height:0.37778in" />

При удалении так же необходимо указать имя сервиса, если при установке использовалось имя сервиса не по умолчанию.

    C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe /ServiceName=”service101” /u \<your_folder>ServiceLogonMultifactor.exe

Если файл конфигурации Service.Config.xml правильный, то после запуска сервиса на ChatId, указанный в разделе общих настроек сервиса, придет сообщение:

     23:11:03 SRV-TERM (192.168.0.43)
     Service  2.2.2.17 STARTED
