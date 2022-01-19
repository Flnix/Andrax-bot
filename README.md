<h1 align="center"> 
    ✨ Andrax Bot ✨ 
</h1>

<h3 align="center"> 
    Telegram Group Manager Bot + Userbot Written In Python Using Pyrogram.
</h3>

<p align="center">
    <a href="https://python.org">
        <img src="http://forthebadge.com/images/badges/made-with-python.svg" alt="made-with-python">
    </a>
    <img src="https://img.shields.io/github/repo-size/thehamkercat/WilliamButcherBot?style=for-the-badge&logo=appveyor" alt="Repository Size"> <br>
    <img src="https://img.shields.io/badge/python-3.9-green?style=for-the-badge&logo=appveyor" alt="Python Version">
</p>

<h3 align="center"> 
    Ready to use method
</h3>

<h2 align="center"> 
   ⇝ Requirements ⇜
</h2>

<p align="center">
    <a href="https://www.python.org/downloads/release/python-390/"> Python3.9 </a> |
    <a href="https://docs.pyrogram.org/intro/setup#api-keys"> Telegram API Key </a> |
    <a href="https://t.me/botfather"> Telegram Bot Token </a> | 
    <a href="https://telegra.ph/How-To-get-Mongodb-URI-04-06"> MongoDB URI </a>
</p>

<h2 align="center"> 
   ⇝ Install Locally Or On A VPS ⇜
</h2>

```console
flnix007@kali:~$ git clone https://github.com/Flnix/Andrax-bot
flnix007@kali:~$ cd Andrax-bot
flnix007@kali:~$ pip3 install -U -r requirements.txt
flnix007@kali:~$ cp sample_config.py config.py
```
 
<h3 align="center"> 
    Edit <b>config.py</b> with your own values
</h3>

<h2 align="center"> 
   ⇝ Run Directly ⇜
</h2>

```console
flnix007@kali:~$ python3 -m wbb
```
<h1>
    <p align="center">
        <a href="https://railway.app/new/template?template=https%3A%2F%2Fgithub.com%2FTheHamkerCat%2FWilliamButcherBot&plugins=mongodb&envs=BOT_TOKEN%2CAPI_ID%2CAPI_HASH%2CSESSION_STRING%2CSUDO_USERS_ID%2CLOG_GROUP_ID%2CGBAN_LOG_GROUP_ID%2CWELCOME_DELAY_KICK_SEC%2CARQ_API_URL%2CMESSAGE_DUMP_CHAT%2CARQ_API_KEY%2CLOG_MENTIONS%2CUSERBOT_PREFIX%2CRSS_DELAY%2CPM_PERMIT&optionalEnvs=SESSION_STRING%2CUSERBOT_PREFIX&BOT_TOKENDesc=Obtain+a+Telegram+bot+token+by+contacting+%40BotFather&API_IDDesc=API_ID+of+your+Telegram+Account+my.telegram.org%2Fapps&API_HASHDesc=API_HASH+of+your+Telegram+Account+my.telegram.org%2Fapps&SESSION_STRINGDesc=Need+for+Userbot+Module+So+u+can+execute+.sh+%26+.l+cmd&SUDO_USERS_IDDesc=Sudo+users+have+full+access+to+everythin%2C+don%27t+trust+anyone...+ex%3A-+123456+654311+123456&LOG_GROUP_IDDesc=For+logs+channel+to+note+down+important+bot+level+events%2C+recommend+to+make+this+public.+ex%3A+%27-123456%27&GBAN_LOG_GROUP_IDDesc=gban+logs.+ex%3A+%27-123456%27&WELCOME_DELAY_KICK_SECDesc=Welcome+Delay+Kick+Sec&ARQ_API_URLDesc=For+Music+Downloading+And+Many+More+Things...+Don%27t+change+this+value&MESSAGE_DUMP_CHATDesc=Chat_id+of+the+group+where+useless+things+will+go&ARQ_API_KEYDesc=Get+this+from+%40ARQRobot.&LOG_MENTIONSDesc=Fill+1+to+turn+this+on%2C+or+0+to+turn+it+off.&USERBOT_PREFIXDesc=Userbot+command+prefix%2C+Leave+it+empty+if+you+don%27t+know+what+that+is.&RSS_DELAYDesc=Delay+in+which+RSS+will+send+updates+in+chat&PM_PERMITDesc=Pm+permit%2C+fill+1+to+enable+or+0+to+disable+it.&WELCOME_DELAY_KICK_SECDefault=300&ARQ_API_URLDefault=https%3A%2F%2Fthearq.tech&LOG_MENTIONSDefault=1&RSS_DELAYDefault=300&PM_PERMITDefault=1&referralCode=QLc1H6">
            <img src="https://railway.app/button.svg" alt="Deploy on Railway">
        </a>
    </p>
</h1>

<h1>
    <p align="center">
        <a href="https://heroku.com/deploy?template=https://github.com/thehamkercat/WilliamButcherBot">
            <img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy">
        </a>
    </p>
</h1>

<h3 align="center"> 
   Generating Pyrogram Session For Heroku
</h3>

```console
flnix007@kali:~$ git clone https://github.com/Flnix/Andrax-bot
flnix007@kali:~$ cd Andrax-bot
flnix007@kali:~$ pip3 install pyrogram TgCrypto
flnix@007kali:~$ python3 str_gen.py
```

<h1 align="center"> 
   ⇝ Docker ⇜
</h1>

```console
flnix007@kali:~$ https://github.com/Flnix/Andrax-bot
flnix007@kali:~$ cd Andrax-bot
flnix007@kali:~$ cp sample_config.env config.env
```

<h3 align="center"> 
    Edit <b> config.env </b> with your own values
</h3>

```console
flnix007@kali:~$ sudo docker build . -t wbb
flnix007@kali:~$ sudo docker run wbb
```

<h2 align="center"> 
   ⇝ Write new modules ⇜
</h2>

```py
# Add license text here, get it from below

from wbb import app # This is bot's client
from wbb import app2 # userbot client, import it if module is related to userbot
from pyrogram import filters # pyrogram filters
...


# For /help menu
__MODULE__ = "Module Name"
__HELP__ = "Module help message"


@app.on_message(filters.command("start"))
async def some_function(_, message):
    await message.reply_text("I'm already up!!")

# Many useful functions are in, wbb/utils/, wbb, and wbb/core/
```

<h3 align="center"> 
   And put that file in wbb/modules/, restart and test your bot.
</h3>
