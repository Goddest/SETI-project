# Tradingview-Telegram-Bot
This is a bot for Tradingview users who want to send alerts to Telegram channels.
<hr>
It allows to capture webhooks from tradingview (and it's capable to parse any JSON actually) and send parsed text to telegram channel. I have also added feature to capture screenshot of tradingview chart and send it with usage of asyncronous POST query.
<hr>

# Usage
Usage is pretty simple - you have only to paste telegram api and channel to global variables (environmental variables), as shown belown in JSON format:
<hr>

    ```
    {
    "TOKEN": "yyyyyyyyy:XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
    "CHANNEL": "zzzzzzzzz"
    }
    ```
<hr>
Where y is a number, X is a letter and z is a number, 
combination of y and X makes your telegram bot API key (take it from https://telegram.me/BotFather) 
And the next chapter of our readme is about how to obtain channel id

# How to get channel TOKEN
Everything you have to do - add bot to the group and open  
```
https://api.telegram.org/bot<YourBOTToken>/getUpdates
```
Whis is a GET query and would allow you to obtain id. There are a lot of information but it is easily to find what we need.

# How to use it

1. Simply launch 'main.py' file with python, then use following template:
``` https://<your-external-ip>:5000/webhook ```

And paste it to tradingview or wherever you want to receive alerts from.
add '&chart=True', as follows, if you want to have chart screenshot.

``` https://<your-external-ip>:5000/webhook&chart=True ```

# Author
Fomberg Vladislav, B05-875