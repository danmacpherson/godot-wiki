#  Physics2DDirectSpaceState  
####**Inherits:** [Object](class_object)
####**Category:** Core

###  Brief Description  
Direct access object to a space in the [Physics2DServer](class_physics2dserver).

###  Member Functions 
  * void  **[intersect&#95;ray](#intersect_ray)**  **(** [Vector2](class_vector2) from, [Vector2](class_vector2) to, [Array](class_array) exclude=Array(), [int](class_int) umask=0  **)**
  * void  **[intersect&#95;shape](#intersect_shape)**  **(** [RID](class_rid) shape, [Matrix32](class_matrix32) xform, [int](class_int) result_max, [Array](class_array) exclude=Array(), [int](class_int) umask=0  **)**
  * void  **[cast&#95;motion](#cast_motion)**  **(** [RID](class_rid) shape, [Matrix32](class_matrix32) xform, [int](class_int) motion, [Array](class_array) exclude=Array(), [int](class_int) umask=0  **)**

###  Description  
Direct access object to a space in the [Physics2DServer](class_physics2dserver). It's used mainly to do queries against objects and areas residing in a given space.

###  Member Function Description  

#### <a name="intersect_ray">intersect_ray</a>
  * void  **intersect&#95;ray**  **(** [Vector2](class_vector2) from, [Vector2](class_vector2) to, [Array](class_array) exclude=Array(), [int](class_int) umask=0  **)**

Intersect a ray in a given space, the returned object is a dictionary with the following fields: 

			position: place where ray is stopped

			normal: normal of the object at the point where the ray was stopped 

			shape:  shape index of the object agaisnt which the ray was stopped

			collider_: collider agaisnt which the ray was stopped

			collider_id: collider id of the object agaisnt which the ray was stopped

			collider: collider object agaisnt which the ray was stopped

			rid:  [RID](class_rid) of the object agaisnt which the ray was stopped

			If the ray did not intersect anything, then null is returned instead of a [Dictionary](class_dictionary).

#### <a name="intersect_shape">intersect_shape</a>
  * void  **intersect&#95;shape**  **(** [RID](class_rid) shape, [Matrix32](class_matrix32) xform, [int](class_int) result_max, [Array](class_array) exclude=Array(), [int](class_int) umask=0  **)**

Intersect a given shape (RID or [Shape2D](class_shape2d)) against the space, the intersected shapes are returned in a special result object.
