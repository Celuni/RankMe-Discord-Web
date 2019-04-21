# Bot Setup
### Hosting
- Create a VPS running ubuntu 16.04 or above.
- Install python3.6 ``sudo add-apt-repository ppa:jonathonf/python-3.6``
- Run ``sudo apt-get install python3.6``
- Install discord.py rewrite ``python3 -m pip install -U discord.py``
- Install aiohttp ``python3 -m pip install aiohttp``
- Install aiomysql ``python3 -m pip install aiomysql``
- Install screen ``sudo apt-get install screen``

### Config
- Edit ``config.json``

#### General
```
language | English = en, hungarian = hu.
bot-token | Discord Bot token, https://github.com/reactiflux/discord-irc/wiki/Creating-a-discord-bot-&-getting-a-token
prefix | Command prefix, e.g. !rank & !top.
command-cooldown | Cool down in seconds per user.
community-name | Name of your community.
```

#### RankMe
```
stats-page-url | Link to profile.php?id={}.
steamid-uk-api-key | Steamid.uk API key, https://steamid.uk/api-manager
steam-api-key | Steam API Key, https://steamcommunity.com/dev/apikey
table-name | Name of rankme table.
top-limit | Amount of players to include in !top.
order-by | Column to order !top command by.
```
##### MySQL
```
servername | Server IP for database.
port | Port for database.
username | Username for database.
password | Password for database.
dbname | Name of database.
```

### Finally
- Upload bot files into the VPS.
- Run ``screen -R rankme``
- Then ``python3 rankme-bot.py``
- Press ``ctrl a, d`` to exit the screen.
- DONE!
