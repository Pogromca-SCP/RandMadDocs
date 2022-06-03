# Game
Contains the entire gameplay configuration.

### Properties
- `default-movement-speed` - `Number` - Defines default movement speed for all players. If value is lesser than 0 then the movement controls will be reversed. If set to 0, players won't be able to move.
- `default-jump-height` - `Number` - Defines default jump height value for all players. If value is lesser than 0 then the jump will pull players towards the ground instead. If set to 0 , players won't be able to jump.
- `default-air-control` - `Number` - Defines default air control value for all players. This works exactly the same way as movement speed except it works only when player is mid-air.
- `default-fire-rate` - `Number` - Defines default fire rate for all players. Negative values will change player shots from projectiles to hitscans. If set to 0, players won't be able to shoot.
- `default-damage` - `Number` - Defines default damage value for all players. If value is lesser than 0 then player attacks will heal targets instead of damaging them.
- `default-knockback` - `Number` - Defines default knockback value for all players. Negative values will pull targets towards damage source instead of pushing them away from it.
- `default-shot-type` - `Number` - Defines default shot type for all players. [Click here to see possible values](../Values/ShotTypes.md).
- `medkits-damage` - `Number` - Amount of damage applied by medkits. Negative values heal targets instead of damaging them.
- `items` - `Array<`[Item](Item.md)`>` - Contains all items that can be spawned during gameplay.
