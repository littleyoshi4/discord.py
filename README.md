# discord.py

discord.py is an API wrapper for Discord written in Python.

This was written to allow easier writing of bots or chat logs.

## Installing

Installing is pretty easy.

```
pip install discord.py
```

Will install the latest 'stable' version of the library.

### This module is alpha!

The discord API is constantly changing and the wrapper API is as well. There will be no effort to keep backwards compatibility.

I recommend that you follow the discussion in the [unofficial Discord API discord channel][ch] and update your installation periodically through `pip install --upgrade discord.py`.

[ch]: https://discord.gg/0SBTUU1wZTUzBx2q

## Quick Example

```py
import discord

client = discord.Client()
client.login('email', 'password')

@client.event
def on_message(message):
    if message.content.startswith('!hello'):
        client.send_message(message.channel, 'Hello was received!')

@client.event
def on_ready():
    print('Logged in as')
    print(client.user.name)
    print(client.user.id)
    print('------')

client.run()
```

You can find examples in the examples directory.

## Requirements

- Python 2.7+ or Python 3.3+.
- `ws4py` library
- `requests` library

Usually `pip` will handle these for you.

## Related Projects

- [discord.js](https://github.com/discord-js/discord.js)
- [discord.io](https://github.com/izy521/discord.io)
- [Discord.NET](https://github.com/RogueException/Discord.Net)
- [DiscordSharp](https://github.com/Luigifan/DiscordSharp)
- [Discord4J](https://github.com/knobody/Discord4J)
- [discordrb](https://github.com/meew0/discordrb)
