# Graphical User Interfaces (GUIs)

Using the GUI object you can access GUI (HTML Dom objects). Commonly, interactions
are scripted as text-based through either the various chat flags or notifications.
GUI objects allow scripters to personalize information presented to players in a convinient and extensible manner.

An example:
```javascript
function onPlayerTouchsMe(pl) {
    var popup = GUI.showpopup({
        title: "Welcome to " + Server.getconfig().gamename + "!",
        width: 400,
        height: 300
    });
    popup.innerHTML = '<br><center>Hmmm cool!</center>' +
        '<img src="../files/icons/corleone_icon_spar.png">' +
        '<input id="actionbutton1" type="submit" class="button" style="left:100px;top:160px;width:200px;height:40px;" value="Button 1!"></input>' +
        '<input id="actionbutton2" type="submit" class="button" style="left:100px;top:220px;width:200px;height:40px;" value="Button 2!"></input>';

    var self = this;
    GUI.onclick("actionbutton1", function(event) {
        GUI.hidepopup();
        self.triggerserver("clicked", "button1");
    });
    GUI.onclick("actionbutton2", function(event) {
        GUI.hidepopup();
        self.triggerserver("clicked", "button2");
    });
}
```  

The following functions are available:

## Function: GUI.showpopup({title: string, width: integer, height: integer})
shows a popup

## Function: GUI.hidepopup()
hides a popup

## Function: GUI.get("id")
finds the GUI/dom object

## Function: GUI.exists("id")
checks if a GUI object exists

## Function: GUI.show("id" or object)
shows an object

## Function: GUI.hide("id" or object)
hides an object

## Function: GUI.onclick("id", function(event) { })
catches the click event