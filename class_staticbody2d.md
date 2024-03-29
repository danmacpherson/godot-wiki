#  StaticBody2D  
####**Inherits:** [PhysicsBody2D](class_physicsbody2d)
####**Category:** Core

###  Brief Description  
Static body for 2D Physics.

###  Member Functions 
  * void  **[set&#95;constant&#95;linear&#95;velocity](#set_constant_linear_velocity)**  **(** [Vector2](class_vector2) vel  **)**
  * void  **[set&#95;constant&#95;angular&#95;velocity](#set_constant_angular_velocity)**  **(** [real](class_real) vel  **)**
  * [Vector2](class_vector2)  **[get&#95;constant&#95;linear&#95;velocity](#get_constant_linear_velocity)**  **(** **)** const
  * [real](class_real)  **[get&#95;constant&#95;angular&#95;velocity](#get_constant_angular_velocity)**  **(** **)** const
  * void  **[set&#95;friction](#set_friction)**  **(** [real](class_real) friction  **)**
  * [real](class_real)  **[get&#95;friction](#get_friction)**  **(** **)** const
  * void  **[set&#95;bounce](#set_bounce)**  **(** [real](class_real) bounce  **)**
  * [real](class_real)  **[get&#95;bounce](#get_bounce)**  **(** **)** const

###  Description  
Static body for 2D Physics. A static body is a simple body that is not intended to move. They don't consume any CPU resources in contrast to a [RigidBody2D](class_rigidbody2d) so they are great for scenaro collision.

	A static body also can be animated by using simulated motion mode, this is useful for implementing functionalities such as moving platforms, when this mode is active the body can be animated and automatically compute linear and angular velocity to apply in that frame and to influence other bodies.
	Alternatively, a constant linear or angular velocity can be set for the static body, so even if it doesn't move, it affects other bodies as if it was moving (this is useful for simulating conveyor belts or conveyor wheels).

###  Member Function Description  

#### <a name="set_constant_linear_velocity">set_constant_linear_velocity</a>
  * void  **set&#95;constant&#95;linear&#95;velocity**  **(** [Vector2](class_vector2) vel  **)**

Set a constant linear velocity for the body.

#### <a name="set_constant_angular_velocity">set_constant_angular_velocity</a>
  * void  **set&#95;constant&#95;angular&#95;velocity**  **(** [real](class_real) vel  **)**

Set a constant angular velocity for the body.

#### <a name="get_constant_linear_velocity">get_constant_linear_velocity</a>
  * [Vector2](class_vector2)  **get&#95;constant&#95;linear&#95;velocity**  **(** **)** const

Return the constant linear velocity for the body.

#### <a name="get_constant_angular_velocity">get_constant_angular_velocity</a>
  * [real](class_real)  **get&#95;constant&#95;angular&#95;velocity**  **(** **)** const

Return the constant angular velocity for the body.
