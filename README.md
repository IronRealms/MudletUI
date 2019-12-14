# MudletUI
Open source Mudlet UI for Iron Realms games

## Components
### IRE.core
The core namespace for IRE-wide applicable code. This contains within it:
#### IRE.core.inventory
#### IRE.core.room
### IRE.gmcp
The namespace for GMCP; because these may differ between games they are not present in the core namespace. This namespace contains handlers for GMCP messages, which are then dispatched to the appropriate places in the IRE namespace.
