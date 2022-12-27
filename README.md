# okp4bot
OKP4 bot for check status and management server

# Install

1. Register Telegram Bot
  - go to https://t.me/botfather and follow instructions
 
2. Setup
  - as root:
    - <code>wget https://gist.github.com/InViZz/e2c01ed3195b6f57d8c576e163fb171a/raw -O okp4-bot-install.sh && chmod +x ./okp4-bot-install.sh</code>
    - <code>./okp4-bot-install.sh <TELEGRAM_TOKEN></code>
    - That's all =)
  - as user:
    - <code>adduser okp4-bot</code>
    - <code>visudo</code>
    
      add
    
      <code>okp4-bot ALL = NOPASSWD: systemctl restart okp4-botd.service, systemctl restart okp4d.service</code>

      at the end of file 
    - <code>su - okp4-bot</code>
    - <code>wget https://gist.github.com/InViZz/e2c01ed3195b6f57d8c576e163fb171a/raw -O okp4-bot-install.sh && chmod +x ./okp4-bot-install.sh</code>
    - <code>./okp4-bot-install.sh <TELEGRAM_TOKEN></code>
    - That's all =)


# Bot Commands:

   - First of all you can use command: /start for subscribe (in private or channel) 

   ```
   /help - show this help

   /start - first command to subscribe
   /node
       args
           list - list of nodes 
           list d - list of nodes with details
           active - nodename true or false - set node active or not
           check - run check all of nodes
           restart - nodename - restart node
   /user
       args
           list - list of users
           add - add user: "/user add username"
           remove - remove user: "/user remove username"
   /run
       run shell command with(without) args
           example -> "/run df -h"
           
   /script
       run inner command
        args
           sysinfo - server info : SSD RAM CPU etc
           ssdcheck - SSD Available space

   /schedule
      args
          add - add schedule: "/schedule add name;ls;30" - (1st name of schedule; 2nd command "ls -la" or script "./test.sh"; 3th period in min )
          list - list of schedules 
          list d - list of schedules with details
          active - scheduleName true or false - set schedule active or not
          remove - remove schedule: "/schedule remove scheduleName"
          
   /version - show version of Bot 
           
   ATTANTION - all commands are case sensitive and can be used with @username (if you using bot in CHANNEL) in the end of command (or "all" parameter can be added)
```
