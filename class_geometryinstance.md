#  GeometryInstance  
####**Inherits:** [VisualInstance](class_visualinstance)
####**Category:** Core

###  Brief Description  
Base node for geometry based visual instances.

###  Member Functions 
  * void  **[set&#95;material&#95;override](#set_material_override)**  **(** [Object](class_object) material  **)**
  * [Object](class_object)  **[get&#95;material&#95;override](#get_material_override)**  **(** **)** const
  * void  **[set&#95;flag](#set_flag)**  **(** [int](class_int) flag, [bool](class_bool) value  **)**
  * [bool](class_bool)  **[get&#95;flag](#get_flag)**  **(** [int](class_int) flag  **)** const
  * void  **[set&#95;draw&#95;range&#95;begin](#set_draw_range_begin)**  **(** [real](class_real) mode  **)**
  * [real](class_real)  **[get&#95;draw&#95;range&#95;begin](#get_draw_range_begin)**  **(** **)** const
  * void  **[set&#95;draw&#95;range&#95;end](#set_draw_range_end)**  **(** [real](class_real) mode  **)**
  * [real](class_real)  **[get&#95;draw&#95;range&#95;end](#get_draw_range_end)**  **(** **)** const

###  Signals  
  *  **visibility&#95;changed**  **(** **)**

###  Numeric Constants  
  * **FLAG_VISIBLE** = **0**
  * **FLAG_CAST_SHADOW** = **3**
  * **FLAG_RECEIVE_SHADOWS** = **4**
  * **FLAG_BILLBOARD** = **1**
  * **FLAG_BILLBOARD_FIX_Y** = **2**
  * **FLAG_DEPH_SCALE** = **5**
  * **FLAG_VISIBLE_IN_ALL_ROOMS** = **6**
  * **FLAG_MAX** = **7**

###  Description  
Base node for geometry based visual instances. Shares some common functionality like visibility and custom materials.

###  Member Function Description  

#### <a name="set_material_override">set_material_override</a>
  * void  **set&#95;material&#95;override**  **(** [Object](class_object) material  **)**

Set the material override for the whole geometry.

#### <a name="get_material_override">get_material_override</a>
  * [Object](class_object)  **get&#95;material&#95;override**  **(** **)** const

Return the material override for the whole geometry.
