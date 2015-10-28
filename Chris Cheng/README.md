## Minecraft Player Tracking

I plan to do a project involving the use of [OpenComputers](http://oc.cil.li/index.php?/page/index.html) - a Minecraft mod that implements LUA-controlled computers - as well as [Computronics](http://wiki.vex.tty.sh/wiki:computronics) - an add-on that adds a Radar block an OpenComputer computer block can control - to track a player's position relative to it over a period of time, such as over a week or two.

While I'll be tracking myself during the time, the completed program could feasibly be configured to track any player, potentially without their knowledge if hidden well.  This project is meant to be a proof-of-concept, showing that such a thing can be done.

Information gathered by a program could be used to generate a heatmap of player positions (for purposes ranging from the beneficial (beacon placement), annoying (advertisement placement) to *downright harmful* (when and where to launch an attack)).  And because OpenComputers implement invisible point-to-point networks via the [Linked Card](http://ocdoc.cil.li/item:linked_card), as well as allowing for HTTP requests or opening TCP connections via the [Internet Card](http://ocdoc.cil.li/item:internet_card), the data could be routed anywhere.  The latter could be additionally bad, because a malicious player could effectively snoop on a person without even logging into the game.
