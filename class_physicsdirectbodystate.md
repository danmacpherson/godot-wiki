#  PhysicsDirectBodyState  
####**Inherits:** [Object](class_object)
####**Category:** Core

###  Brief Description  


###  Member Functions 
  * [Vector3](class_vector3)  **[get&#95;total&#95;gravity](#get_total_gravity)**  **(** **)** const
  * [real](class_real)  **[get&#95;total&#95;density](#get_total_density)**  **(** **)** const
  * [real](class_real)  **[get&#95;inverse&#95;mass](#get_inverse_mass)**  **(** **)** const
  * [Vector3](class_vector3)  **[get&#95;inverse&#95;inertia](#get_inverse_inertia)**  **(** **)** const
  * void  **[set&#95;linear&#95;velocity](#set_linear_velocity)**  **(** [Vector3](class_vector3) velocity  **)**
  * [Vector3](class_vector3)  **[get&#95;linear&#95;velocity](#get_linear_velocity)**  **(** **)** const
  * void  **[set&#95;angular&#95;velocity](#set_angular_velocity)**  **(** [Vector3](class_vector3) velocity  **)**
  * [Vector3](class_vector3)  **[get&#95;angular&#95;velocity](#get_angular_velocity)**  **(** **)** const
  * void  **[set&#95;transform](#set_transform)**  **(** [Transform](class_transform) transform  **)**
  * [Transform](class_transform)  **[get&#95;transform](#get_transform)**  **(** **)** const
  * void  **[add&#95;force](#add_force)**  **(** [Vector3](class_vector3) force, [Vector3](class_vector3) pos  **)**
  * void  **[set&#95;sleep&#95;state](#set_sleep_state)**  **(** [bool](class_bool) enabled  **)**
  * [bool](class_bool)  **[is&#95;sleeping](#is_sleeping)**  **(** **)** const
  * [int](class_int)  **[get&#95;contact&#95;count](#get_contact_count)**  **(** **)** const
  * [Vector3](class_vector3)  **[get&#95;contact&#95;local&#95;pos](#get_contact_local_pos)**  **(** [int](class_int) contact_idx  **)** const
  * [Vector3](class_vector3)  **[get&#95;contact&#95;local&#95;normal](#get_contact_local_normal)**  **(** [int](class_int) contact_idx  **)** const
  * [int](class_int)  **[get&#95;contact&#95;local&#95;shape](#get_contact_local_shape)**  **(** [int](class_int) contact_idx  **)** const
  * [RID](class_rid)  **[get&#95;contact&#95;collider](#get_contact_collider)**  **(** [int](class_int) contact_idx  **)** const
  * [Vector3](class_vector3)  **[get&#95;contact&#95;collider&#95;pos](#get_contact_collider_pos)**  **(** [int](class_int) contact_idx  **)** const
  * [int](class_int)  **[get&#95;contact&#95;collider&#95;id](#get_contact_collider_id)**  **(** [int](class_int) contact_idx  **)** const
  * [Object](class_object)  **[get&#95;contact&#95;collider&#95;object](#get_contact_collider_object)**  **(** [int](class_int) contact_idx  **)** const
  * [int](class_int)  **[get&#95;contact&#95;collider&#95;shape](#get_contact_collider_shape)**  **(** [int](class_int) contact_idx  **)** const
  * [Vector3](class_vector3)  **[get&#95;contact&#95;collider&#95;velocity&#95;at&#95;pos](#get_contact_collider_velocity_at_pos)**  **(** [int](class_int) contact_idx  **)** const
  * [real](class_real)  **[get&#95;step](#get_step)**  **(** **)** const
  * void  **[integrate&#95;forces](#integrate_forces)**  **(** **)**
  * [PhysicsDirectSpaceState](class_physicsdirectspacestate)  **[get&#95;space&#95;state](#get_space_state)**  **(** **)**

###  Member Function Description  
