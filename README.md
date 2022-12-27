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
