# fork from https://github.com/gregzaal/Auto-Voice-Channels/

### A Discord bot that automatically creates voice channels as they are needed.

- [Public bot invite link](https://discordapp.com/api/oauth2/authorize?client_id=996841292246036603&permissions=286280784&scope=bot)

## Requires:

* [Python 3.7+](https://www.python.org/downloads/)
* [discord.py](https://pypi.org/project/discord.py/) (`pip install discord.py`)
* [pytz](https://pypi.org/project/pytz/) (`pip install pytz`)
* [psutil](https://pypi.org/project/psutil/) (`pip install psutil`)
* [Requests](https://pypi.org/project/requests/) (`pip install requests`)

## Optional Extras:

* [uvloop](https://pypi.org/project/uvloop/) (`pip install uvloop`) - **UNIX ONLY**

## Quick start:

### On Linux (Ubuntu/Debian):

* Clone the repository: `git clone https://github.com/ppug/auto-voice-channel.git`
* Go to the directory: `cd Auto-Voice-Channel`
* Install pip: `sudo apt-get -y install python3-pip`
* Install venv: `pip3 install virtualenv`
* Make venv: `python3 -m virtualenv bot-env`
* Use venv: `. bot-env/bin/activate`
* Install requirements: `python3 -m pip install -r requirements.txt`
* Create your application + bot here: <https://discordapp.com/developers/applications>
* Enable both **Presence** and **Server Members** Privileged Gateway Intents in the Bot section.
* Create a `config.json` file in the Auto-Voice-Channels folder and fill it in:
  * `admin_id` is your personal [user ID](https://techswift.org/2020/04/22/how-to-find-your-user-id-on-discord/), for the bot to DM you errors and other important logs.
  * `client_id` is the bot application client ID.
  * `log_timezone` is for the time displayed in logs, see [this list](https://stackoverflow.com/questions/13866926/is-there-a-list-of-pytz-timezones).
  * `token` is your bot's private token you can find [here](https://discordapp.com/developers/applications) - do not share it with anyone else.
  * There are a number of [optional settings](https://wiki.dotsbots.com/en/self-hosting/optional-config) too, which aren't necessary to set but provide some further configuration options if needed.
  * Your `config.json` file should look something like this:

```json
{
    "admin_id":123456789012345678,
    "client_id":987654321098765432,
    "log_timezone":"Africa/Johannesburg",
    "token":"XXXXXXXXXXXXXXXXXXXXXXXX.XXXXXX.XXXXXXXXXXXXXXXXXXXXXXXXXXX"
}
```

* Invite the bot to your own server, replacing `<YOUR BOT ID>` with... your bot ID: `https://discordapp.com/api/oauth2/authorize?client_id=<YOUR BOT ID>&permissions=286280784&scope=bot`
* Start your bot: `python3 auto-voice-channels.py`
