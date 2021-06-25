You need to configure the Service.Config.xml file, located in the same directory as the service file during manual installation or in the same directory as the installer during automatic installation. 
Use "true" and "false" without capital letters. In this version, there is no automatic casting. 

## Common settings of the service <ServiceConfig/>:

3.3.1.  **botId**="0000000000:AAAaaBBBBBBbbbbCCCCCccccccDDDDdddd"

    Bot ID or HTTP API key see p.3.1. to have it.

3.3.2.  **chatId**="0000000"
    
    Chat ID of the administrator (phone number code in telegram), this chat receives messages about the start and stop of the service, login of a 
    user who is not on the list. Using this chat ID you can also send commands to disconnect sessions and receive information. 
    You can specify several IDs using ";" as a separator.

3.3.3.  **DetailInfoOnServiceStart**="false"

    It determines whether to send the results of command systeminfo, tasklist and configuration settings when the service starts.  
    The results of above mentioned commands can always be obtained by running the command \ <computer name / all> info / config 

3.3.4.  **daysOldDeliteLogs**="0"

    Days to keep log files (0- delete each service start)

3.3.5  **logsLevel**="15"
   
    logging level in binary format. 0-nothing, 13 (1011) optimal, 31 (11111) full.
 
3.3.6.  **waitForAnswerSec**="20"

    waiting for an answer from the user. After this time, any buttons press will be ignored.

3.3.7.  **sendMessageBeforeDisconnectSec**="15"

    time before session disconnection messages appears. command - msg.exe \<session ID> \<text>

3.3.8.  **disconnectIfNoAnswer**="true"

    disconnect session if no answer.

3.3.9.  **notDisconnectIP**="console"

    The list of IPs that do not disconnect when connected.  
    Each user has his list, so this option works for users who cannot change their list and forq users who are not on the list.  
    The program changes this parameter by clicking on the third button in the message "Enable & remIP" / "Disconnect & rem IP" 

3.3.10.  **CommandReadIntervalSec**="30"

    Reading Telegram for commands and Service.Config.xml interval 

3.3.11. **SingleServiceOnTheBot**="false"

    true if you are using only one computer for this Telegram bot

3.3.12. **ClearTelegramRequestsAfterSeconds**="120"

    The time after which old commands will be deleted. If **SingleServiceOnTheBot**="true", then this parameter does not have any
    value. It should be specified to be more beforehand, than **CommandReadIntervalSec**="30" on other computers, which use the 
    same botId, in order to make sure that the rest of the services had time to read the command.

3.3.13. **LinesPerSessionInTaskList**="10"
    
    Number of string's for each session into results for the command tasklist

3.3.14. **systemInfoOnStartFields**="OS Name;System Boot Time;Total Physical Memory;Available Physical Memory;Domain"
    
    Headers list of fields from command "systeminfo.exe fo table", which would be sent at the start of the service. Or by request 
    \<computer name>/all> info

3.3.15. **systemInfoOnEventFields**="OS Name;System Boot Time;Total Physical Memory;Available Physical Memory;Domain"
    
     Headers list of fields from command "systeminfo.exe fo table", which would be sent with response on button clicks if user is
     administrator. This command is pretty slow, and in order to make it react faster on button clicks, it would be better to leave its
     parameter empty.

3.3.16. **LOGON_TIME**\_**fieldName**="LOGON TIME"

3.3.17. **USERNAME_fieldName**="USERNAME"

3.3.18. **SESSIONNAME_fieldName**="SESSIONNAME"

     Regional setting: you should execute quser command and check the name of these сolumns for your OS language. Please, keep in mind,
     that if you originally set the  English version and then change your interface language, most likely your system still has the same
     language as before, it is still English. The execution result of this command under system account can be found in the log file
     after the launch of the service and after the first login (file \\log\\full\\logfull-yyyy-mm-dd.txt)

3.3.19. **LastUpdateRecived**="45770444"

3.3.20. **ThreIsNewChanges**="false"

3.3.21. **LastConfigRead**="2021-05-26T10:57:07.54406+03:00"

    Service fields can be edit by program.

## User settings \<Users> \<user /> \</Users></span>

3.3.22.  **name**="user1"

    name of the user, the same as execution result of quser (without domen) 

3.3.23.  **chatId**="00000000"

    Chat id of the current user, these two parameters are minimum configuration, the rest of the data may be left empty, default values will be used. 
    You can specify a few chat ids using a delimiter ; (**chatId**="00000000;111111;22222222") in the case where the user has a multiple telegram 
    accounts or if multiple users use the same account. All users will receive a message of a log in attempt, who clicks the button first, his/her
    command will execute.

3.3.24.  **waitForAnswerSec**="0" 

    0-value from default settings

3.3.25.  **sendMessageBeforeDisconnectSec**="0" 

    0-value from default settings

3.3.26.  **notDisconnectIP**="console" 

    list of IP addresses or console from which user can not be disconnected

3.3.27. **CanChangeIP**="true"
     
    User can modify the list of IP addresses, by default it is set to true

3.3.28.  **IsAdmin**="false"
    If user is able to send commands that can disconnect sessions and requests regarding system information, by default set to false
