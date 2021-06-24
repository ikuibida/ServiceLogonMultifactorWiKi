Grab installer 
[ServiceLogonMultiFactor.msi](https://github.com/Constantine-SRV/ServiceLogonMultifactor2/blob/master/Distr_MSI_EXE/ServiceLogonMultiFactor.msi), file with parameters of installer [ServiceLogonMultiFactor.ini](https://github.com/Constantine-SRV/ServiceLogonMultifactor2/blob/master/Distr_MSI_EXE/ServiceLogonMultiFactor.ini) and configuration file of the service Service.Config.xml [(look at section 3)](https://github.com/Constantine-SRV/ServiceLogonMultifactor/wiki/EN-3.-Settings)

Check, if file has digital signature:
![cert msi](https://github.com/Constantine-SRV/ServiceLogonMultifactor2/blob/master/documentation/MSI-CERT-2.JPG)

If you want to edit default setting, edit file ServiceLogonMultiFactor.ini

Launch installer

If installation was successful, on ChatId specified in configuration section of service you receive a message. 
![ServiceStart](https://github.com/Constantine-SRV/ServiceLogonMultifactor2/blob/master/documentation/service_start.PNG)

