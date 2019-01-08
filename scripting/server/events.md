# Server Side Events
> When certain things happen, such as the player colliding (touching) with the NPC, then the script of the NPC is started and can react to the collision event.

The current event name is specified as a global boolean variable, which you can check like "if (playersays)".
Alternatively you can react to the event by writing a function "function onEventname" such as
```javascript
function onPlayerSays(pl) {
}
```

The following server-side events exist:
## onUpdated
the script has been updated with the in-game editor

## onCreated
the NPC has been loaded (server or map loaded), important for script classes

## onPlayerTouchsMe
the player collides with the NPC

## onPlayerSays
a player is in a distance of around 300 pixels or less, and is chatting

## onMouseDown
a player taps or clicks on the NPC

## onPlayerGrabs
a player grabs the NPC

## onPlayerAttacks
a player attacks the NPC with sword; there is also **onPlayerHammers** and **onPlayerPicks**

## onTimeout
When calling **settimeout**, this event is automatically invoked after the specified time.