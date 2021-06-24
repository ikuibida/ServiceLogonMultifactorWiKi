# Purpose

****ServiceLogonMultiFactor (SLMF)**** - is an open source software project, which allows you to connect second authentication factor for your users who log into a computer both locally and via RDP. Telegram messenger is used as a second factor by transmitting user-friendly message with allow/decline buttons and the service acts in accordance to pressed button.

SLMF service can not prevent users from loggining into a system, but if the service won`t receive verification during specific period of time (section 3.5) user disconnects. Futhermore, by clicking button decline the service will disconnect user at once, which may help you to protect your system from an unkown user.

In addition, the service enables you to get an execution result of the following commands, if you have relevant operational privileges:

* systeminfo
* quser 
* tasklist

SLMF is a flexible tool that can disconnect users, check status and settings of service operation.
