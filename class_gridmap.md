#  GridMap  
####**Inherits:** [Spatial](class_spatial)
####**Category:** Core

###  Brief Description  


###  Member Functions 
  * void  **[set&#95;theme](#set_theme)**  **(** [MeshLibrary](class_meshlibrary) theme  **)**
  * [MeshLibrary](class_meshlibrary)  **[get&#95;theme](#get_theme)**  **(** **)** const
  * void  **[set&#95;bake](#set_bake)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[is&#95;baking&#95;enabled](#is_baking_enabled)**  **(** **)** const
  * void  **[set&#95;cell&#95;size](#set_cell_size)**  **(** [real](class_real) size  **)**
  * [real](class_real)  **[get&#95;cell&#95;size](#get_cell_size)**  **(** **)** const
  * void  **[set&#95;octant&#95;size](#set_octant_size)**  **(** [int](class_int) size  **)**
  * [int](class_int)  **[get&#95;octant&#95;size](#get_octant_size)**  **(** **)** const
  * void  **[set&#95;cell&#95;item](#set_cell_item)**  **(** [int](class_int) x, [int](class_int) y, [int](class_int) z, [int](class_int) item, [int](class_int) orientation=0  **)**
  * [int](class_int)  **[get&#95;cell&#95;item](#get_cell_item)**  **(** [int](class_int) x, [int](class_int) y, [int](class_int) z  **)** const
  * [int](class_int)  **[get&#95;cell&#95;item&#95;orientation](#get_cell_item_orientation)**  **(** [int](class_int) x, [int](class_int) y, [int](class_int) z  **)** const
  * void  **[resource&#95;changed](#resource_changed)**  **(** [Object](class_object) arg0  **)**
  * void  **[set&#95;center&#95;x](#set_center_x)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[get&#95;center&#95;x](#get_center_x)**  **(** **)** const
  * void  **[set&#95;center&#95;y](#set_center_y)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[get&#95;center&#95;y](#get_center_y)**  **(** **)** const
  * void  **[set&#95;center&#95;z](#set_center_z)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[get&#95;center&#95;z](#get_center_z)**  **(** **)** const
  * void  **[set&#95;clip](#set_clip)**  **(** [bool](class_bool) enabled, [bool](class_bool) clipabove=true, [int](class_int) floor=0, [int](class_int) axis=0  **)**
  * [int](class_int)  **[crate&#95;area](#crate_area)**  **(** [int](class_int) id, [AABB](class_aabb) area  **)**
  * [AABB](class_aabb)  **[area&#95;get&#95;bounds](#area_get_bounds)**  **(** [int](class_int) area  **)** const
  * void  **[area&#95;set&#95;exterior&#95;portal](#area_set_exterior_portal)**  **(** [int](class_int) area, [bool](class_bool) enable  **)**
  * void  **[area&#95;set&#95;name](#area_set_name)**  **(** [int](class_int) area, [String](class_string) name  **)**
  * [String](class_string)  **[area&#95;get&#95;name](#area_get_name)**  **(** [int](class_int) area  **)** const
  * [bool](class_bool)  **[area&#95;is&#95;exterior&#95;portal](#area_is_exterior_portal)**  **(** [int](class_int) area  **)** const
  * void  **[area&#95;set&#95;portal&#95;disable&#95;distance](#area_set_portal_disable_distance)**  **(** [int](class_int) area, [real](class_real) distance  **)**
  * [real](class_real)  **[area&#95;get&#95;portal&#95;disable&#95;distance](#area_get_portal_disable_distance)**  **(** [int](class_int) area  **)** const
  * void  **[area&#95;set&#95;portal&#95;disable&#95;color](#area_set_portal_disable_color)**  **(** [int](class_int) area, [Color](class_color) color  **)**
  * [Color](class_color)  **[area&#95;get&#95;portal&#95;disable&#95;color](#area_get_portal_disable_color)**  **(** [int](class_int) area  **)** const
  * void  **[erase&#95;area](#erase_area)**  **(** [int](class_int) area  **)**
  * [int](class_int)  **[get&#95;unused&#95;area&#95;id](#get_unused_area_id)**  **(** **)** const
  * void  **[bake&#95;geometry](#bake_geometry)**  **(** **)**
  * void  **[clear](#clear)**  **(** **)**

###  Numeric Constants  
  * **INVALID_CELL_ITEM** = **-1**

###  Member Function Description  
