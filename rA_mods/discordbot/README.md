# roCORD for rAthena
Discord Bot for communication between discord and ingame channel.
The bot prints everything written to #discord into the selected discord server and vice versa.

!!! This is a beta version, somethings might not work as intended and crashes could occure !!!
(See todo or issues)

Any bridge which implements a socket and a discord bot is fine for this.

Provided in bridge/ is a python solution for debugging and a NodeJS solution (written by NOIL).

## Features:
- Basic Discord to ingame channel and ingame channel to Discord.
- Script command, which sends a message to the discord server.
- Supports "rare_drop_announce". (Idea: Stolao)

## Install:
1. copy discordbot.cpp/.h into src/map/
2. apply diffs (can be found in diffs/) onto existing files in src/
3. (optional) configure channel
4. configure bot by changing index.js (you need to providea token and define a discord channel id)
5. start bot before starting rathena.

## How to configure:
Basic Config:
```
	char* name = "#discord";     
	char* alias = "[Discord]";
	tmp_chn.color = channel_getColor("Blue");
```
(To see supported colors check channel.conf)

## Script commands:
Example scirpt: TODO

```
Command: 
  discord(<string>);
Sends a message to discord.
```
## Ideas:
- Multi channel support.

## TODO:
- Remove \<Username\> palceholder.
- Fix |00 message bug. (Currently fixed by a workarround)
- Add auto reconnect to bridge.
- Add manual reconnect to bridge.

## Working with:
(This is updated once per month or upon a request)

rev 042b886
