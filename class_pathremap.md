##  PathRemap  
**Inherits:** [[object|Object]]\\
**Category:** Core\\
##  Brief Description  
Singleton containing the list of remapped resources.
##  Member Functions 
  * void [[#add_remap|add_remap]]**(** [String](class_string) from, [String](class_string) to, [String](class_string) locale="" **)**
  * [bool](class_bool) [[#has_remap|has_remap]]**(** [String](class_string) path **)** const
  * [String](class_string) [[#get_remap|get_remap]]**(** [String](class_string) path **)** const
  * void [[#erase_remap|erase_remap]]**(** [String](class_string) path **)**
  * void [[#clear_remaps|clear_remaps]]**(****)**
##  Description  
When exporting, the types of some resources may change internally so they are converted to more optimized versions. While it's not usually necesary to access to this directly (path remapping happens automatically when opeining a file), it's exported just for information.
##  Member Function Description  
==  add_remap  ==
  * void [[#add_remap|add_remap]]**(** [String](class_string) from, [String](class_string) to, [String](class_string) locale="" **)**
\\
Add a remap from a file to another.
==  has_remap  ==
  * [bool](class_bool) [[#has_remap|has_remap]]**(** [String](class_string) path **)** const
\\
Return true if a file is being remapped.
==  get_remap  ==
  * [String](class_string) [[#get_remap|get_remap]]**(** [String](class_string) path **)** const
\\
Return the remapped new path of a file.
==  erase_remap  ==
  * void [[#erase_remap|erase_remap]]**(** [String](class_string) path **)**
\\
Erase a remap.
==  clear_remaps  ==
  * void [[#clear_remaps|clear_remaps]]**(****)**
\\
Clear all remaps.