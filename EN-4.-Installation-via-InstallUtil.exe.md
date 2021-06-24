If you don`t want to use installer, and would like to build and compile execution file from source code or you would like
to launch the service and hide its presence in programs and features, then you can install this service using default utility InstallUtil.exe.


Put compiled or [downloaded](https://github.com/Constantine-SRV/ServiceLogonMultifactor2/blob/master/Distr_MSI_EXE/ServiceLogonMultifactor.exe)
file ServiceLogonMultifactor.exe in working directory, [edit](https://github.com/Constantine-SRV/ServiceLogonMultifactor2/wiki/EN-3.-Settings)
and put it beside Service.Config.xml

Further from command line or PowerShell with administration permissions:
 
 Installation:

    C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe <your folder>ServiceLogonMultifactor.exe

First launch (since then service starts automatically):
 
    net start ServiceLogonMultifactor

Uninstall:
 
    C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe /u <your folder>ServiceLogonMultifactor.exe

Installation of service with non-standard name and description:

By default, service will be named "ServiceLogonMultifactor" with description "Service for logging of logon and unlock events and send notification to telegram bot".

In order to change service name and description it is possible with InstallUtil.exe and arguments /ServiceName=  и /description=.

    C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe /ServiceName=”service101” /description=”test service 101”    <your_folder>ServiceLogonMultifactor.exe

<img src="https://github.com/Constantine-SRV/ServiceLogonMultifactor2/blob/master/documentation/ServiceCustomName.jpg" style="width:7.75in;height:0.37778in" />

When you uninstall you should specify name of the service, if you used non-standard name.

    C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe /ServiceName=”service101” /u \<your_folder>ServiceLogonMultifactor.exe

If configuration file Service.Config.xml correct, then after service launch on ChatId, specified in general setting of service, you 
will receive the next message:

     23:11:03 SRV-TERM (192.168.0.43)
     Service  2.2.2.17 STARTED
