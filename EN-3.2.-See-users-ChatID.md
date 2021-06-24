The easiest way of doing it, is to run the console program ConsoleReadTelegramBot.exe 

Enter the previously received BotId, ask users to send their login to this bot, and copy the displayed ChatId. 

Please note that sometimes users first need to write 2-3 messages to the bot so that they appear, then everything works from the first message. 
Example application window: 

![ConsoleReadTelegramBot.JPG](https://github.com/Constantine-SRV/ServiceLogonMultifactor2/blob/master/documentation/ConsoleReadTelegramBot.JPG)

Alternatively, you can enter a link like https: //api.telegram.org/bot {botid} / getUpdates  in the browser

https://api.telegram.org/bot1705365690:AAFJNFTPcvPd_oOGsV4rfU3O3v4oNnyasNI/getUpdates 

and take the ChatId from the result:

![chatIdFromBrowser.JPG](https://github.com/Constantine-SRV/ServiceLogonMultifactor2/blob/master/documentation/chatIdFromBrowser.JPG)