#  TreeItem  
####**Inherits:** [Object](class_object)
####**Category:** Core

###  Brief Description  


###  Member Functions 
  * void  **[set&#95;cell&#95;mode](#set_cell_mode)**  **(** [int](class_int) column, [int](class_int) mode  **)**
  * [int](class_int)  **[get&#95;cell&#95;mode](#get_cell_mode)**  **(** [int](class_int) column  **)** const
  * void  **[set&#95;checked](#set_checked)**  **(** [int](class_int) column, [bool](class_bool) checked  **)**
  * [bool](class_bool)  **[is&#95;checked](#is_checked)**  **(** [int](class_int) column  **)** const
  * void  **[set&#95;text](#set_text)**  **(** [int](class_int) column, [String](class_string) text  **)**
  * [String](class_string)  **[get&#95;text](#get_text)**  **(** [int](class_int) column  **)** const
  * void  **[set&#95;icon](#set_icon)**  **(** [int](class_int) column, [Texture](class_texture) texture  **)**
  * [Texture](class_texture)  **[get&#95;icon](#get_icon)**  **(** [int](class_int) column  **)** const
  * void  **[set&#95;icon&#95;region](#set_icon_region)**  **(** [int](class_int) column, [Rect2](class_rect2) region  **)**
  * [Rect2](class_rect2)  **[get&#95;icon&#95;region](#get_icon_region)**  **(** [int](class_int) column  **)** const
  * void  **[set&#95;icon&#95;max&#95;width](#set_icon_max_width)**  **(** [int](class_int) column, [int](class_int) width  **)**
  * [int](class_int)  **[get&#95;icon&#95;max&#95;width](#get_icon_max_width)**  **(** [int](class_int) column  **)** const
  * void  **[set&#95;range](#set_range)**  **(** [int](class_int) column, [real](class_real) value  **)**
  * [real](class_real)  **[get&#95;range](#get_range)**  **(** [int](class_int) column  **)** const
  * void  **[set&#95;range&#95;config](#set_range_config)**  **(** [int](class_int) column, [real](class_real) min, [real](class_real) max, [real](class_real) step, [bool](class_bool) expr=false  **)**
  * [Dictionary](class_dictionary)  **[get&#95;range&#95;config](#get_range_config)**  **(** [int](class_int) column  **)**
  * void  **[set&#95;metadata](#set_metadata)**  **(** [int](class_int) column, var meta  **)**
  * void  **[get&#95;metadata](#get_metadata)**  **(** [int](class_int) column  **)** const
  * void  **[set&#95;custom&#95;draw](#set_custom_draw)**  **(** [int](class_int) column, [Object](class_object) object, [String](class_string) callback  **)**
  * void  **[set&#95;collapsed](#set_collapsed)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[is&#95;collapsed](#is_collapsed)**  **(** **)**
  * [TreeItem](class_treeitem)  **[get&#95;next](#get_next)**  **(** **)**
  * [TreeItem](class_treeitem)  **[get&#95;prev](#get_prev)**  **(** **)**
  * [TreeItem](class_treeitem)  **[get&#95;parent](#get_parent)**  **(** **)**
  * [TreeItem](class_treeitem)  **[get&#95;children](#get_children)**  **(** **)**
  * [TreeItem](class_treeitem)  **[get&#95;next&#95;visible](#get_next_visible)**  **(** **)**
  * [TreeItem](class_treeitem)  **[get&#95;prev&#95;visible](#get_prev_visible)**  **(** **)**
  * void  **[remove&#95;child](#remove_child)**  **(** [Object](class_object) child  **)**
  * void  **[set&#95;selectable](#set_selectable)**  **(** [int](class_int) column, [bool](class_bool) selectable  **)**
  * [bool](class_bool)  **[is&#95;selectable](#is_selectable)**  **(** [int](class_int) column  **)** const
  * [bool](class_bool)  **[is&#95;selected](#is_selected)**  **(** [int](class_int) column  **)**
  * void  **[select](#select)**  **(** [int](class_int) column  **)**
  * void  **[deselect](#deselect)**  **(** [int](class_int) column  **)**
  * void  **[set&#95;editable](#set_editable)**  **(** [int](class_int) column, [bool](class_bool) enabled  **)**
  * [bool](class_bool)  **[is&#95;editable](#is_editable)**  **(** [int](class_int) column  **)**
  * void  **[set&#95;custom&#95;color](#set_custom_color)**  **(** [int](class_int) column, [Color](class_color) color  **)**
  * void  **[clear&#95;custom&#95;color](#clear_custom_color)**  **(** [int](class_int) column  **)**
  * void  **[set&#95;custom&#95;bg&#95;color](#set_custom_bg_color)**  **(** [int](class_int) column, [Color](class_color) color  **)**
  * void  **[clear&#95;custom&#95;bg&#95;color](#clear_custom_bg_color)**  **(** [int](class_int) column  **)**
  * [Color](class_color)  **[get&#95;custom&#95;bg&#95;color](#get_custom_bg_color)**  **(** [int](class_int) column  **)** const
  * void  **[add&#95;button](#add_button)**  **(** [int](class_int) column, [Texture](class_texture) button, [int](class_int) arg2  **)**
  * [int](class_int)  **[get&#95;button&#95;count](#get_button_count)**  **(** [int](class_int) column  **)** const
  * [Texture](class_texture)  **[get&#95;button](#get_button)**  **(** [int](class_int) column, [int](class_int) button_idx  **)** const
  * void  **[erase&#95;button](#erase_button)**  **(** [int](class_int) column, [int](class_int) button_idx  **)**
  * void  **[set&#95;tooltip](#set_tooltip)**  **(** [int](class_int) column, [String](class_string) tooltip  **)**
  * [String](class_string)  **[get&#95;tooltip](#get_tooltip)**  **(** [int](class_int) column  **)** const
  * void  **[move&#95;to&#95;top](#move_to_top)**  **(** **)**
  * void  **[move&#95;to&#95;bottom](#move_to_bottom)**  **(** **)**

###  Numeric Constants  
  * **CELL_MODE_STRING** = **0**
  * **CELL_MODE_CHECK** = **1**
  * **CELL_MODE_RANGE** = **2**
  * **CELL_MODE_ICON** = **3**
  * **CELL_MODE_CUSTOM** = **4**

###  Member Function Description  
