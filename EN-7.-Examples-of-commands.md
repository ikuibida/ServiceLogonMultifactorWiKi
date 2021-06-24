 **<span class="smallcaps">Commands, that you can send to the service</span>**

7.1.  Command contains of two or three parts with whitespace as delimeter 

        1.  Computer name or all (all computers)

        2.  Command by itself (dis, sys, quser, task, config, ver, inform)

        3.  Parameter only for dis number - session

7.2.  dis (disconnect) number of session

7.3.  sys (systeminfo) result of execution of the command systeminfo.exe, configuration in section 3.13

7.4.  quser result of execution of the command quser.exe

7.5.  task (tasklist) result of execution of the command tasklist.exe, settings in section 3.12

7.6.  config current configuration (from file Service.Config.xml)

7.7.  ver (version) version of running service and its uptime in hours

7.8.  Inform (information ) sends in one message results of all three commands quser.exe,systeminfo.exe,tasklist.exe

7.9.  Examples

        1.  ws-01 dis 3 disconnect 3 session on computer ws-01

        2.  ws-01 sys will send result of systeminfo c ws-01

        3.  All sys the same result from all computers

        4.  ws-01 quser, all quser, ws-01 config, all config, all ver and etc.
           
7.10. Permissions are defined by parameter IsAdmin (look at section 3.7)
      
      if true then all can be done, if false - service will response that user is not an administrator
      if user is not exist (chatid) in config - there is not going to be any answer