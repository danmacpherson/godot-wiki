#  RigidBody  
####**Inherits:** [PhysicsBody](class_physicsbody)
####**Category:** Core

###  Brief Description  


###  Member Functions 
  * void  **[&#95;integrate&#95;forces](#_integrate_forces)**  **(** [PhysicsDirectBodyState](class_physicsdirectbodystate) state  **)** virtual
  * void  **[set&#95;mode](#set_mode)**  **(** [int](class_int) mode  **)**
  * [int](class_int)  **[get&#95;mode](#get_mode)**  **(** **)** const
  * void  **[set&#95;mass](#set_mass)**  **(** [real](class_real) mass  **)**
  * [real](class_real)  **[get&#95;mass](#get_mass)**  **(** **)** const
  * void  **[set&#95;weight](#set_weight)**  **(** [real](class_real) weight  **)**
  * [real](class_real)  **[get&#95;weight](#get_weight)**  **(** **)** const
  * void  **[set&#95;friction](#set_friction)**  **(** [real](class_real) friction  **)**
  * [real](class_real)  **[get&#95;friction](#get_friction)**  **(** **)** const
  * void  **[set&#95;bounce](#set_bounce)**  **(** [real](class_real) bounce  **)**
  * [real](class_real)  **[get&#95;bounce](#get_bounce)**  **(** **)** const
  * void  **[set&#95;linear&#95;velocity](#set_linear_velocity)**  **(** [Vector3](class_vector3) linear_velocity  **)**
  * [Vector3](class_vector3)  **[get&#95;linear&#95;velocity](#get_linear_velocity)**  **(** **)** const
  * void  **[set&#95;angular&#95;velocity](#set_angular_velocity)**  **(** [Vector3](class_vector3) angular_velocity  **)**
  * [Vector3](class_vector3)  **[get&#95;angular&#95;velocity](#get_angular_velocity)**  **(** **)** const
  * void  **[set&#95;max&#95;contacts&#95;reported](#set_max_contacts_reported)**  **(** [int](class_int) amount  **)**
  * [int](class_int)  **[get&#95;max&#95;contacts&#95;reported](#get_max_contacts_reported)**  **(** **)** const
  * void  **[set&#95;use&#95;custom&#95;integrator](#set_use_custom_integrator)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[is&#95;using&#95;custom&#95;integrator](#is_using_custom_integrator)**  **(** **)**
  * void  **[set&#95;contact&#95;monitor](#set_contact_monitor)**  **(** [bool](class_bool) enabled  **)**
  * [bool](class_bool)  **[is&#95;contact&#95;monitor&#95;enabled](#is_contact_monitor_enabled)**  **(** **)** const
  * void  **[set&#95;use&#95;continuous&#95;collision&#95;detection](#set_use_continuous_collision_detection)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[is&#95;using&#95;continuous&#95;collision&#95;detection](#is_using_continuous_collision_detection)**  **(** **)** const
  * void  **[set&#95;axis&#95;velocity](#set_axis_velocity)**  **(** [Vector3](class_vector3) axis_velocity  **)**
  * void  **[apply&#95;impulse](#apply_impulse)**  **(** [Vector3](class_vector3) pos, [Vector3](class_vector3) impulse  **)**
  * void  **[set&#95;active](#set_active)**  **(** [bool](class_bool) active  **)**
  * [bool](class_bool)  **[is&#95;active](#is_active)**  **(** **)** const
  * void  **[set&#95;can&#95;sleep](#set_can_sleep)**  **(** [bool](class_bool) able_to_sleep  **)**
  * [bool](class_bool)  **[is&#95;able&#95;to&#95;sleep](#is_able_to_sleep)**  **(** **)** const

###  Signals  
  *  **body&#95;enter**  **(** [Object](class_object) body  **)**
  *  **body&#95;enter&#95;shape**  **(** [int](class_int) body_id, [Object](class_object) body, [int](class_int) body_shape, [int](class_int) local_shape  **)**
  *  **body&#95;exit**  **(** [Object](class_object) body  **)**
  *  **body&#95;exit&#95;shape**  **(** [int](class_int) body_id, [Object](class_object) body, [int](class_int) body_shape, [int](class_int) local_shape  **)**

###  Numeric Constants  
  * **MODE_STATIC** = **1**
  * **MODE_KINEMATIC** = **3**
  * **MODE_RIGID** = **0**
  * **MODE_CHARACTER** = **2**

###  Member Function Description  
