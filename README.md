INVITE [link](https://discord.com/api/oauth2/authorize?client_id=954351086309892138&permissions=8&scope=bot)

## Usage
### Basics
The bot is usable straight away with given default settings: <br/>
- The bot only listens for commands in a channel named "war-bot" and joins a voice channel "war-channel". Schedule a war with `!scheduleWar [Timestamp]`. The Timestamp has to be in the following format: `hh:mm`. <br /> Example: `!scheduleWar 20:00`
- Unschedule wars by `!unscheduleWar [Timestamp]`
- `!leaveWar` to let the bot leave the war earlier, if you managed to pull up a fast win
### Advanced
To start a war in mm:ss (minutes:seconds):
```
!startWar mm:ss
```

To list all scheduled wars:
```
!list
```
To get a list of commands:
```
!help
```
The bot can be furhter customized by adjusting the settings in the following format: <br />
```
!settings set [SETTING] [OPTIONAL VALUE]
```
Values including spaces have to be put in qoutes.

Settings can be viewed by:
```
!settings get [SETTING]
```

#### Settings
##### channelName
- Channel Name the bot listens on for commands. Make sure that the bot has access to read and write in that channel.
- Example: `!settings set channelName "test-channel"`
- Default value: "war-bot"
##### warChannel
- War Channel the bot joins on war. Make sure that the bot has access to join that channel.
- Example: `!settings set warChannel "test-channel"`
- Default value: "war-channel"
##### preJoinTimer
- Time in seconds before the bot joins the voice channel.
- Example: `!settings set preJoinTimer 300`
- Default value: 300
##### firstCallTimer
- Time in seconds before the bot starts calling respawnwaves. The first respawn waves are very frequent. This is mainly to reduce spam.
- Example: `!settings set firstCallTimer 600`
- Default value: 600
##### callRate
- List of times in seconds before a wave the bot should remind about the respawn wave (use qoutes)
- Example: `!settings set callRate "5 10 15"`
- Default value: "5 10 15"
##### timeZone
- Set the bots time calcluations to match your current time.
- Example: `!settings set timeZone 19:30`
- Default value: normalized for CET
