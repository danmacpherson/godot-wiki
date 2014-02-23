##  BaseButton  
**Inherits:** [[control|Control]]\\
**Category:** Core\\
##  Brief Description  
Provides a base class for different kinds of buttons.
##  Member Functions 
  * void [[#set_pressed|set_pressed]]**(** [bool](class_bool) pressed **)**
  * [bool](class_bool) [[#is_pressed|is_pressed]]**(****)** const
  * void [[#set_toggle_mode|set_toggle_mode]]**(** [bool](class_bool) enabled **)**
  * [bool](class_bool) [[#is_toggle_mode|is_toggle_mode]]**(****)** const
  * void [[#set_disabled|set_disabled]]**(** [bool](class_bool) disabled **)**
  * [bool](class_bool) [[#is_disabled|is_disabled]]**(****)** const
  * void [[#set_click_on_press|set_click_on_press]]**(** [bool](class_bool) enable **)**
  * [bool](class_bool) [[#get_click_on_press|get_click_on_press]]**(****)** const
##  Signals  
  * **toggled****(** [bool](class_bool) pressed **)**
  * **pressed****(****)**
##  Description  
BaseButton is the abstract base class for buttons, so it shouldn't be used directly (It doesnt display anything). Other types of buttons inherit from it.
##  Member Function Description  
==  set_pressed  ==
  * void [[#set_pressed|set_pressed]]**(** [bool](class_bool) pressed **)**
\\
Set the button to pressed state (only if toggle_mode is active).
==  is_pressed  ==
  * [bool](class_bool) [[#is_pressed|is_pressed]]**(****)** const
\\
Return when the button is pressed (only if toggle_mode is active).
==  set_toggle_mode  ==
  * void [[#set_toggle_mode|set_toggle_mode]]**(** [bool](class_bool) enabled **)**
\\
Set the button toggle_mode property. Toggle mode makes the button flip state between pressed and unpressed each time its area is clicked.
==  is_toggle_mode  ==
  * [bool](class_bool) [[#is_toggle_mode|is_toggle_mode]]**(****)** const
\\
Return the toggle_mode property (see [[#set_toggle_mode|set_toggle_mode]]).
==  set_disabled  ==
  * void [[#set_disabled|set_disabled]]**(** [bool](class_bool) disabled **)**
\\
Set the button into disabled state. When a button is disabled, it can"apos;t be clicked or toggled.
==  is_disabled  ==
  * [bool](class_bool) [[#is_disabled|is_disabled]]**(****)** const
\\
Return wether the button is in disabled state (see [[#set_disabled|set_disabled]]).
==  set_click_on_press  ==
  * void [[#set_click_on_press|set_click_on_press]]**(** [bool](class_bool) enable **)**
\\
Set the button click_on_press mode. This mode generates click events when a mousebutton or key is just pressed (by default events are generated when the button/keys are released and both press and release occur in the visual area of the Button).
==  get_click_on_press  ==
  * [bool](class_bool) [[#get_click_on_press|get_click_on_press]]**(****)** const
\\
Return the state of the click_on_press property (see [[#set_click_on_press|set_click_on_press]]).