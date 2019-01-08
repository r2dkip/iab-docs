# Server Functions

Trigger actions to be set on the game server itself.

## Function: Server.searchplayers(options:{})
returns an array of players which match the options. Possible combinations for options are: `{id:number}`, `{map:string}`, `{clanname:string}`, `{clanid:integer}`, `{map:string, clanname:string}`, `{map:string, clanid:integer}`

## Function: Server.searchnpcs({map, area:{x,y,w,h}})
returns an array of NPCs in that rectangle

## Function: Server.getconfig(filewithoutextension: string, [indexAttribute], [categoryAttribute])
loads a configuration file (fast), the configuration should have the structure `{filename:[objects]}`, the returned object also contains ways for quick lookup: objects: array of all objects, index[name] one object, category[name] array of objects

Examples:
```javascript
echo("default weapon: " + Server.getconfig("main").defaultweapon);
  -> sword1
echo("config skeleton: ", Server.getconfig("monsters", "type").index["skeleton"]);
  -> { type: 'skeleton', name: 'Pirate Skeleton', ...}
echo("config item nr: " + Server.getconfig("items", "itemid", "itemtype").objects.length);
  -> 591
echo("config weapon nr: " + Server.getconfig("items", "itemid", "itemtype").categories["weapon"].length);
  -> 97
echo("config sword1: ", Server.getconfig("items", "itemid", "itemtype").index["sword1"]);
  -> { itemid: 'sword1', name: 'Standard Sword', itemtype: 'weapon', ...}  
```
