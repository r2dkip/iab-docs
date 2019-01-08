# Server Side NPCs

The NPC object can be accessed by the identifier this. If you change a property (such as image or ani) and want it to be permanent, then call `this.save()`.
Most attributes can also be changed by calling `setATTRIBUTE(name)` such as `this.setchat(text)`.
NPC functions are currently also available as global functions, so that you can call either `this.say(text)` or `say(text)`, although the use of `this.say` is recommended.

The following properties and functions are available:

## Property: this.map
- Type: `Object`

map object, structure:
```javascript 
{
    name,
    template,
    width, height,
    iswater(x,y), iswall(x,y),
    [onlytiles])
}
```

## Property: this.hp
- Type: `Integer`

hitpoints, read-only

## Property: this.isdead
- Type: `Boolean`

read-only

## Property: this.maxhp
- Type: `Integer`

max-hitpoints, read-only

## Property: this.name
- Type: `String`

## Property: this.chat
- Type: `String`

## Property: this.weapon
- Type: `String`

## Property: this.weapondata
- Type: `Object`

## Property: this.body
- Type: `String`

## Property: this.head
- Type: `String`

## Property: this.hat
- Type: `String`

## Property: this.bow
- Type: `String`

## Property: this.mount
- Type: `String`

## Property: this.image
- Type: `String`

image of the NPC

## Property: this.ani
- Type: `String`

## Property: this.aniarg1..9
- Type: `String`

the ARG1..9 values in the .bani files

## Property: this.x, y, z, dir
- Type: `Number`

current NPC position and direction

## Property: this.zoom
- Type: `Number`

default 1

## Property: this.storyid
- Type: `Integer`

current story played back by the NPC

## Property: this.waypoints
- Type: `Object[]`

play back the specified waypoints, get waypoints by clicking on the waypoints button in story windows

## Property: this.scriptclasses
- Type: `String[]`

read-only, lists the join()ed classes

## Function: this.say(text:string [,delay:number])
shows text, by default for 5 seconds but you can optionally specify the number of seconds

## Function: this.setimg(image:string)
changes the image of the NPC, must include the file extensions and exist in the npcs/ folder of the Files project

## Function: this.setani(ani:string)
sets the animation (.bani file) of the NPC, without file extension

## Function: this.move(timeinseconds:number, x:number, y:number)
moves to the specified position in the specified time, updates the direction of the NPC. On server this is currently updating the position of the NPC immediately, but players see it moving smoothly.

## Function: this.play(sound:string)
plays a sound effect to near players

## Function: this.settimeout(timeinseconds:number)
schedules a "timeout" event which is invoked after the specified time on the same script

## Function: this.scheduleevent(delayinseconds:number, eventname:string [, ...additional parameters])
schedules a custom event which is invoked after the specified time with optional additional parameters which are passed to the onEventname function

## Function: this.cancelevents(event:string)

## Function: this.save()
saves the NPC to database

## Function: this.join(classname)
joins a script class, call save() afterwards to make it permanent

## Function: this.leave(classname)
leaves a script class