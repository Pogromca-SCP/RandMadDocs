# Functions

### ReloadJson(FileName)
Reloads JSON serverdata with a provided server file if it exists.

### ResetJson()
Reloads JSON serverdata with default file.

### ChangeMap(MapURL)
Opens a map from URL (Lua VM will be reloaded). The server will open it's default map if the map from url doesn't exist.

### ResetMap()
Restarts current server map (Lua VM will be reloaded).

### ServerScript(FileName)
Executes Lua script from a provided server file if it exists.

### ServerLog(Message)
Prints the message into the server log.

### ForceStart()
Forces a match to start if it hasn't already.

### MsgAll(Message[, R, G, B])
Sends a message with a specific color for all players.

### MsgTo(Message, PlayerId[, R, G, B])
Sends a message with a specific color for selected player.

### SetPlayerLoc(PlayerId, X[, Y, Z])
Sets selected player's position.

### DamagePlayer(PlayerId, DamageAmount)
Applies damage amount to the selected player.

### ThrowPlayer(PlayerId, X[, Y, Z])
Applies knockback to the selected player.
