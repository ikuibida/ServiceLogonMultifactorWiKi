# Purpose

****ServiceLogonMultiFactor (SLMF)**** - is an open source software project, which allows you to connect a second authentication factor for users who log into a computer both locally and via RDP. Telegram messenger is used as a second authentication factor by transmitting a user-friendly message with allow/decline buttons, the service then acts in accordance to the pressed button.

SLMF service can not prevent users from logging into a system, but if the service is not verified within a specific period of time (section 3.5) the user is disconnected. Furthermore, by clicking the decline button the service will disconnect the user immediately, which may help you protect your system from an unknown user.

In addition, the service enables you to get an execution result of the following commands, if you have relevant operational privileges:

* systeminfo
* quser 
* tasklist

SLMF is a flexible tool that can disconnect users, check status and settings of service operation.
