# RandMadDocs
This repository contains technical details about data, scripts, formats, etc. used by "RandoMadness".

## Server configuration
Values for properties below can be changed in file `{GameDirectory}/RandoMadness/Saved/Config/{PlatformName}/Game.ini` (if this directory doesn't exist, launching the server/game once will fix it) under section `[/Script/RandoMadness.RandMadInstance]`. Values are set using key/value syntax (PropertyName=Value).

### ServerPath
This path is used by server as a root directory when looking for custom data and script files. The directory can contain anything but it has to provide `defaults.json` file and can (definitely should) provide `lib.lua` file. The server won't work properly without a valid server path!

### AdminPassword
This is a password that can be used to get access to server commands in game. If left empty, accessing server commands from within the game won't be possible.

## Lua API
The server has built-in Lua support which allows server hosts to change game behaviour at runtime using their own scripts. Currently supported Lua version: `5.4.0`.

### lib.lua
`lib.lua` file is loaded/executed each time the server opens a new map which makes it a good place to bind events and initialize variables.

### Functions
The game provides many global functions that can be used to change game's behaviour. Every global Lua function that is loaded can be also used as a command. This includes predefined functions as well as the custom ones. Keep in mind that certain functions may do nothing if the provided arguments are incorrect or Lua can't access game elements for some reasons. [Click here to learn more about available functions](RandoLua/Functions.md).

### Events
Events are Lua functions that are called by server when certain conditions are met. They have no default implementation, so they can be binded by server hosts to execute custom logic. The best place to do this is `lib.lua` as it's always loaded but it can be done in a different script as well. To bind an event, simply create a global function that has the same name as the event. [Click here to learn more about available events](RandoLua/Events.md).

## Using commands in game
Every text-chat message starting with `/` will be send to server as a command. The server parses commands into Lua function calls. Whitespaces are used as argument seperetors. To provide a string argument, enclose the text inside quotation marks. Examples:

Text-chat message: /MsgAll "Hello There!" 56 0 120

Lua code equivalent: MsgAll("Hello There!",56,0,120)

Text-chat message: /DamagePlayer 2 400

Lua code equivalent: DamagePlayer(2,400)

Text-chat message: /MsgAll MyVar 100

Lua code equivalent: MsgAll(MyVar,100)

Text-chat message: /MsgTo "He_llo W" 3

Lua code equivalent: MsgTo("He_llo W",3)

## JSON API
JSON files store gameplay configuration. The server uses settings from `defaults.json` by default but the source file can be changed using commands. [Click here to learn more about gameplay configuration](JSONTypes/Game.md).

### Custom JSON Types
In addition to the standard JSON types, the game also uses it's own custom JSON types. All custom types are JSON objects with additional properties. Some custom types may inherit from other types, the derived type has all properties of the base type, but may interpret them differently. Missing properties are interpreted as null, 0 etc.
