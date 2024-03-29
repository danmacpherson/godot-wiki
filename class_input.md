#  Input  
####**Inherits:** [Object](class_object)
####**Category:** Core

###  Brief Description  


###  Member Functions 
  * [bool](class_bool)  **[is&#95;key&#95;pressed](#is_key_pressed)**  **(** [int](class_int) scancode  **)**
  * [bool](class_bool)  **[is&#95;mouse&#95;button&#95;pressed](#is_mouse_button_pressed)**  **(** [int](class_int) button  **)**
  * [bool](class_bool)  **[is&#95;joy&#95;button&#95;pressed](#is_joy_button_pressed)**  **(** [int](class_int) device, [int](class_int) button  **)**
  * [bool](class_bool)  **[is&#95;action&#95;pressed](#is_action_pressed)**  **(** [String](class_string) action  **)**
  * [real](class_real)  **[get&#95;joy&#95;axis](#get_joy_axis)**  **(** [int](class_int) device, [int](class_int) axis  **)**
  * [Vector3](class_vector3)  **[get&#95;accelerometer](#get_accelerometer)**  **(** **)**
  * [Vector2](class_vector2)  **[get&#95;mouse&#95;pos](#get_mouse_pos)**  **(** **)** const
  * [Vector2](class_vector2)  **[get&#95;mouse&#95;speed](#get_mouse_speed)**  **(** **)** const
  * void  **[set&#95;mouse&#95;mode](#set_mouse_mode)**  **(** [int](class_int) mode  **)**
  * [int](class_int)  **[get&#95;mouse&#95;mode](#get_mouse_mode)**  **(** **)** const

###  Numeric Constants  
  * **MOUSE_MODE_VISIBLE** = **0**
  * **MOUSE_MODE_HIDDEN** = **1**
  * **MOUSE_MODE_CAPTURED** = **2**

###  Member Function Description  

#### <a name="get_mouse_pos">get_mouse_pos</a>
  * [Vector2](class_vector2)  **get&#95;mouse&#95;pos**  **(** **)** const

Return the global, unscaled, screen pointer coordinates.
			If the 2D viewport has been scaled, it may not work well
			with [Camera](class_camera) or controls.
