# Scripting

### Introduction

Much has been said about tools that allow users to create video games without programming. It's been a dream for many independent developers to create games without learning how to code. This need has been around for a long time, even inside companies, where game designers wish to have more control of the game flow.

Many products have been shipped promising a no-programming environment, but the result is often incomplete, too complex or inefficient compared to traditional code. As a result, programming is here to stay for a long time. In fact, the general direction in game engines has been to add tools that try to reduce the amount of code that needs to be written for specific tasks, to speed up development. 

In that sense, Godot has taken some useful design decisions towards that goal. The first and most important is the scene system. The aim of it is not obvious at first, but works well later on. That is, to relieve programmers from the responsibility of architecting code. 

When designing games using the scene system, the whole project is fragmented in *complementary* scenes (not individual ones). Scenes complement each other, instead of being separate. There will be plenty of examples  about this later on, but it's very important to remember it.

For those with a good amount of programming expertise, this means a different design pattern to MVC. Godot promises efficiency at the expense of dropping the MVC habits, which are replaced by the *scenes as a complement* pattern.

Godot also uses the [extend](http://c2.com/cgi/wiki?EmbedVsExtend) pattern for scripting, meaning that scripts extends from all the available engine classes.

### GDScript

[GDScript](gdscript) (click link for reference) is a dynamically typed scripting language to fit inside Godot. It was designed with the following goals:

*  First and most importantly, making it simple, familiar and as easy to learn as possible.
*  Making the code readable and error safe. The syntax is mostly borrowed from Python.

Programmers generally take a few days to learn it, and within two weeks feel comfortable with it.

As with most dynamically typed languages though, the higher productivity (code is easier to learn, faster to write, no compilation, etc) is balanced with a performance penalty, but most critical code is written in C++ already in the engine (vector ops, physics, math, indexing, etc), making the resulting performance more than enough for most types of games.

In any case, if more performance is required, critical sections can be rewritten in C++ and exposed transparently to the script. This allows for replacing a GDScript class with a C++ class without altering the rest of the game.

### Scripting a Scene

Before continuing, please make sure to read the [GDScript](gdscript) reference. It's a simple language and the reference is short, should not take more than a few minutes to glance.

#### Scene Setup

This tutorial will begin by scripting a simple GUI scene. Use the add node dialog to create the following hierarchy, with the following nodes:

*  Panel
    * Label
    * Button

It should look like this in the scene tree:

<p align="center"><img src="images/scriptscene.png"></p>

And try to make it look like this in the 2D editor, so it makes sense:

<p align="center"><img src="images/scriptsceneimg.png"></p>

Finally, save the scene, a fitting name could be "sayhello.scn"

#### Adding a Script

Select the Panel node, then press the "Add Script" Icon as follows:

<p align="center"><img src="images/addscript.png"></p>

The script creation diallog will popup. This dialog allows to select the language, class name, etc. 
GDScript does not use class names in script files, so that field is not editable.
The script should inherit from "Panel" (as it is meant to extend the node, which is of Panel type, this is automatically filled anyway).
Select the filename for the script (if you saved the scene previously, one will be automatically generated as sayhello.gd) and push "Create":

<p align="center"><img src="images/scriptcreate.png"></p>

Once this is done, the script will be created and added to the node. You can see this both as an extra icon in the node, as well as in the script property:

<p align="center"><img src="images/scriptadded.png"></p>


To edit the script, pushing the icon above should do it (although, the UI will take you directly to the Script editor screen). So, here's the template script:

<p align="center"><img src="images/script_template.png"></p>

There is not much in there. The "_ready()" function is called when the node (and all it's children) entered the active scene. (Remember, It's not a constructor, the constructor is "_init()" ). 

#### Handling a Signal

Signals are used mostly in GUI nodes, (although other nodes have them too). Signals are "emitted" when some specific kind of action happens, and can be connected to any function of any script instance. In this step, the "pressed" signal from the button will be connected to a custom function.

There is a GUI for connecting signals, just select the node and press the "Signals" button:

<p align="center"><img src="images/signals.png"></p>

Which will show the list of signals a Button can emit.

<p align="center"><img src="images/button_connections.png"></p>

But this example will not use it. We don't want to make things *too* easy. So please close that screen!
In any case, at this point it is clear that that we are interested in the "pressed" signal, so instead of doing it with the visual interface, the connection will be done using code. 

For this, there is a function that is probably the one that Godot programmers will use the most, this is [get_node](class_node#get_node)(). This function uses paths to fetch nodes in the current tree or anywhere in the scene, relative to the node holding the script.

To fetch the button, the following must be used:

```python

get_node("Button")

```

So, next, a callback will be added for when a button is pressed, that will change the label's text:

```python

func _on_button_pressed():	
	get_node("Label").set_text("HELLO!")

```

Finally, the button "pressed" signal will be connected to that callback in _ready(), by using [connect](class_object#connect)().

```python

func _ready():
	get_node("Button").connect("pressed",self,"_on_button_pressed")
```

The final script should look like this:

```python


extends Panel

# member variables here, example:

# var a=2
# var b="textvar"

func _on_button_pressed():
	get_node("Label").set_text("HELLO!")

func _ready():
	get_node("Button").connect("pressed",self,"_on_button_pressed")


```

Running the scene should have the expected result when pressing the button:

<p align="center"><img src="images/scripthello.png"></p>








 --- //[Juan Linietsky](reduzio@gmail.com) 2013/12/08 07:54//
