# Server Side NPCs

The player who was causing the event can be access with the identifier **player**.


The following properties and functions are available:

## Property: player.id
- Type: `Integer`

the unique player id, read-only

## Property: player.map
- Type: `Object`

map object {name, template, width, height, iswater(x,y), iswall(x,y), [onlytiles])}

## Property: player.hp
- Type: `Integer`

hitpoints, read-only

## Property: player.isdead
- Type: `Boolean`

read only

## Property: player.maxhp
- Type: `Integer`

max-hitpoints, read-only

## Property: player.name
- Type: `String`

read-only

## Property: player.chat
- Type: `String`

## Property: player.weapon
- Type: `String`

## Property: player.weapondata
- Type: `Object`

## Property: player.body
- Type: `String`

## Property: player.head
- Type: `String`

## Property: player.hat
- Type: `String`

## Property: player.bow
- Type: `String`

## Property: player.mount
- Type: `String`

## Property: player.ani
- Type: `String`

## Property: player.aniarg1..9
- Type: `String`

the ARG1..9 values in the .bani files

## Property: player.x, y, z, dir
- Type: `Number`

current player position and direction

## Property: player.zoom
- Type: `Number`

default 1

## Property: player.onlinetime
- Type: `Integer`

seconds of playing the game

## Property: player.kills, player.streak, player.mobkills, player.sparwins
- Type: `Integer`

## Property: player.adminlevel
- Type: `Integer`

## Property: player.clanname
- Type: `String`

the current clan name / tag of the player

## Property: player.clanid
- Type: `Integer`

the id of the current clan

## Function: player.hasitem(itemid:string)
- Type: `Boolean`

tells you if the player has a certain item

## Function: player.additem(itemid:string)
- Type: `Boolean`

the item must be configured with `"addbyscript":true` and `"addinmaps":["mapofnpc"]`

## Function: player.setani(ani:string)
shows an animation until the player moves again, filename without file extension

## Function: player.showurl(url:string)
opens the URL in a new window, currently only works on mobile because of popup blocker

## Function: player.showmessage(message:string)
shows a message at the top of the screen

## Function: player.setmap(map:string, template:string, x:number, y:number)
moves the player, do `("outside", "unknown", 0, 0)` to move out of a house

## Function: player.unstick()
unsticks the player