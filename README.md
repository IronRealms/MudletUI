# MudletUI
Open source Mudlet UI for Iron Realms games

## Components
### IRE.core
The core namespace for IRE-wide applicable code. This contains within it:
#### IRE.core.inventory
The character inventory functions and handling. The inventory is stored in `IRE.core.inventory.list`, which uses the item id as the key and the item JSON from GMCP as the value.
#### IRE.core.room
The room functions and handling. The inventory is stored in `IRE.core.room.inventory`, which uses the item id as the key and the item JSON from GMCP as the value.
### IRE.gmcp
The namespace for GMCP; because these may differ between games they are not present in the core namespace. This namespace contains handlers for GMCP messages, which are then dispatched to the appropriate places in the IRE namespace.
### NumpadNavigation
The namespace for numpad navigation, binding the directions and look to the numpad. Meant to be easily disabled.
## Events
#### IRE.core.inventory
* `IRE.core.inventory.add` fires when an item addition to `IRE.core.inventory.list` completes, passing the item as an argument
* `IRE.core.inventory.listReceived` fires when the character inventory list is received and `IRE.core.inventory.list` is fully populated
* `IRE.core.inventory.remove` fires when an item removal from `IRE.core.inventory.list` completes, passing the item as an argument
#### IRE.core.room
* `IRE.core.room.inventoryAdd` fires when an item addition to `IRE.core.room.inventory` completes, passing the item as an argument
* `IRE.core.room.inventoryReceived` fires when the room inventory list is received and `IRE.core.room.inventory` is fully populated
* `IRE.core.room.inventoryRemove` fires when an item removal from `IRE.core.room.inventory` completes, passing the item as an argument