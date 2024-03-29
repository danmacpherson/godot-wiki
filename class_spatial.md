#  Spatial  
####**Inherits:** [Node](class_node)
####**Category:** Core

###  Brief Description  
Base class for all 3D nodes.

###  Member Functions 
  * void  **[set&#95;transform](#set_transform)**  **(** [Transform](class_transform) local  **)**
  * [Transform](class_transform)  **[get&#95;transform](#get_transform)**  **(** **)** const
  * void  **[set&#95;translation](#set_translation)**  **(** [Vector3](class_vector3) translation  **)**
  * [Vector3](class_vector3)  **[get&#95;translation](#get_translation)**  **(** **)** const
  * void  **[set&#95;rotation](#set_rotation)**  **(** [Vector3](class_vector3) rotation  **)**
  * [Vector3](class_vector3)  **[get&#95;rotation](#get_rotation)**  **(** **)** const
  * void  **[set&#95;scale](#set_scale)**  **(** [Vector3](class_vector3) scale  **)**
  * [Vector3](class_vector3)  **[get&#95;scale](#get_scale)**  **(** **)** const
  * void  **[set&#95;global&#95;transform](#set_global_transform)**  **(** [Transform](class_transform) global  **)**
  * [Transform](class_transform)  **[get&#95;global&#95;transform](#get_global_transform)**  **(** **)** const
  * [Object](class_object)  **[get&#95;parent&#95;spatial](#get_parent_spatial)**  **(** **)** const
  * void  **[set&#95;ignore&#95;transform&#95;notification](#set_ignore_transform_notification)**  **(** [bool](class_bool) enabled  **)**
  * void  **[set&#95;as&#95;toplevel](#set_as_toplevel)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[is&#95;set&#95;as&#95;toplevel](#is_set_as_toplevel)**  **(** **)** const
  * [World](class_world)  **[get&#95;world](#get_world)**  **(** **)** const
  * void  **[update&#95;gizmo](#update_gizmo)**  **(** **)**
  * void  **[set&#95;gizmo](#set_gizmo)**  **(** SpatialGizmo gizmo  **)**
  * SpatialGizmo  **[get&#95;gizmo](#get_gizmo)**  **(** **)** const

###  Numeric Constants  
  * **NOTIFICATION_TRANSFORM_CHANGED** = **29** - Spatial nodes receive this notifacation with their global transform changes. This means that either the current or a parent node changed it's transform.
  * **NOTIFICATION_ENTER_WORLD** = **41**
  * **NOTIFICATION_EXIT_WORLD** = **42**

###  Description  
Spatial is the base for every type of 3D [Node](class_node). It contains a 3D [Transform](class_transform) which can be set or get as local or global. If a Spatial [Node](class_node) has Spatial children, their transforms will be relative to the parent.

###  Member Function Description  

#### <a name="set_transform">set_transform</a>
  * void  **set&#95;transform**  **(** [Transform](class_transform) local  **)**

Set the transform locally, relative to the parent spatial node.

#### <a name="get_transform">get_transform</a>
  * [Transform](class_transform)  **get&#95;transform**  **(** **)** const

Return the local transform, relative to the bone parent.

#### <a name="set_global_transform">set_global_transform</a>
  * void  **set&#95;global&#95;transform**  **(** [Transform](class_transform) global  **)**

Set the transform globally, relative to worldspace.

#### <a name="get_global_transform">get_global_transform</a>
  * [Transform](class_transform)  **get&#95;global&#95;transform**  **(** **)** const

Return the gloal transform, relative to worldspace.

#### <a name="get_parent_spatial">get_parent_spatial</a>
  * [Object](class_object)  **get&#95;parent&#95;spatial**  **(** **)** const

Return the parent [Spatial](class_spatial), or an empty [Object](class_object) if no parent exists or parent is not of type [Spatial.
