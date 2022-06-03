# Functions

### CheckLua()
Returns true if Lua can access game elements, returns false otherwise. This function should always return true! Lua features won't work properly without access to game elements.

### ReloadJson(FileName)
Reloads JSON serverdata with a provided server file if it exists. Returns true if reload completed successfully, returns false otherwise.

### ResetJson()
Reloads JSON serverdata with default file. Returns true if reload completed successfully, returns false otherwise.

### ChangeMap(MapURL)
Opens a map from URL. The server will open it's default map if the map from url doesn't exist.

### ResetMap()
Restarts current server map.

### ServerScript(FileName)
Executes Lua script from a provided server file if it exists. Returns true if executed without errors, returns false otherwise.

### ServerLog(Message)
Prints the message into the server log.

### Delay(TimeInSeconds, Command)
Calls given server command after specified time delay. Function uses the same command format as in-game console. Calling this function before previous delay ends will replace old delay with the new one. Changing or reseting map will cancel the delay.

### ForceStart()
Forces a match to start if it hasn't already.

### NextStage()
Forces a Campaign match to skip current stage.

### MsgAll(Message[, R, G, B])
Sends a message with a specific color for all players.

### MsgRed(Message[, R, G, B])
Sends a message with a specific color for all players in red team.

### MsgBlu(Message[, R, G, B])
Sends a message with a specific color for all players in blue team.

### MsgTo(Message, PlayerId[, R, G, B])
Sends a message with a specific color for selected player.

### SetPlayerLoc(PlayerId, X[, Y, Z])
Sets selected player's position.

### DamagePlayer(PlayerId, DamageAmount)
Applies damage amount to the selected player.

### ThrowPlayer(PlayerId, X[, Y, Z])
Applies knockback to the selected player.

### DoesPlayerExist(PlayerId)
Returns true if player id is valid, returns false otherwise.

### GetPlayersCount()
Returns current number of players on server (can return -1 if Lua can't access game elements).

### GetItemsCount()
Returns current number of items avaiable on server (can return -1 if Lua can't access game elements).

### DoesItemExist(ItemId)
Returns true if item id is valid, returns false otherwise.

### GetItemName(ItemId)
Returns selected item name or nil if item is invalid.

### AddItem(ItemName[, ItemDescription, MovementSpeed, JumpHeight, AirControl, FireRate, Damage, Knockback, ShotType])
Adds new item to server list.

### RemoveItem(ItemId)
Removes selected item from server list.

### RemoveRandomItem()
Removes random item from server list.

### CleanItems()
Removes all items from server list.

### SetDefaultMovementSpeed(Value)
Sets default movement speed on server.

### GetDefaultMovementSpeed()
Returns default movement speed on server (can return nil if Lua can't access game elements).

### SetDefaultJumpHeight(Value)
Sets default jump height on server.

### GetDefaultJumpHeight()
Returns default jump height on server (can return nil if Lua can't access game elements).

### SetDefaultAirControl(Value)
Sets default air control on server.

### GetDefaultAirControl()
Returns default air control on server (can return nil if Lua can't access game elements).

### SetDefaultFireRate(Value)
Sets default fire rate on server.

### GetDefaultFireRate()
Returns default fire rate on server (can return nil if Lua can't access game elements).

### SetDefaultDamage(Value)
Sets default damage on server.

### GetDefaultDamage()
Returns default damage on server (can return nil if Lua can't access game elements).

### SetDefaultKnockback(Value)
Sets default knockback on server.

### GetDefaultKnockback()
Returns default knockback on server (can return nil if Lua can't access game elements).

### SetDefaultShotType(Value)
Sets default shot type on server.

### GetDefaultShotType()
Returns default shot type on server (can return nil if Lua can't access game elements).

### SetMedkitsDamage(Value)
Sets medkits damage on server.

### GetMedkitsDamage()
Returns medkits damage on server (can return nil if Lua can't access game elements).

### GetPlayerName(PlayerId)
Returns selected player's name or nil if the player id is invalid.

### IsPlayerVer(PlayerId)
Returns true if selected player can use commands, false if player can't or nil if the player id is invalid.

### GiveItem(PlayerId, ItemId)
Gives selected item to selected player if player's inventory has empty slot.

### GiveRandomItem(PlayerId)
Gives random item to selected player if player's inventory has empty slot.

### DropItem(PlayerId, SlotId)
Removes selected player's item from specific slot (1-5).

### DropRandomItem(PlayerId)
Removes selected player's random item.

### CleanInventory(PlayerId)
Removes all selected player's items.
