##  Mesh  
**Inherits:** [[resource|Resource]]\\
**Category:** Core\\
##  Brief Description  
A [[resource|Resource]] that contains vertex-array based geometry.
##  Member Functions 
  * void [[#add_morph_target|add_morph_target]]**(** [String](class_string) name **)**
  * [int](class_int) [[#get_morph_target_count|get_morph_target_count]]**(****)** const
  * [String](class_string) [[#get_morph_target_name|get_morph_target_name]]**(** [int](class_int) index **)** const
  * void [[#clear_morph_targets|clear_morph_targets]]**(****)**
  * void [[#set_morph_target_mode|set_morph_target_mode]]**(** [int](class_int) mode **)**
  * [int](class_int) [[#get_morph_target_mode|get_morph_target_mode]]**(****)** const
  * void [[#add_surface|add_surface]]**(** [int](class_int) primitive, [Array](class_array) arrays, [Array](class_array) morph_arrays, [bool](class_bool) arg3=Array() **)**
  * [int](class_int) [[#get_surface_count|get_surface_count]]**(****)** const
  * void [[#surface_remove|surface_remove]]**(** [int](class_int) surf_idx **)**
  * [int](class_int) [[#surface_get_array_len|surface_get_array_len]]**(** [int](class_int) surf_idx **)** const
  * [int](class_int) [[#surface_get_array_index_len|surface_get_array_index_len]]**(** [int](class_int) surf_idx **)** const
  * [int](class_int) [[#surface_get_format|surface_get_format]]**(** [int](class_int) surf_idx **)** const
  * [int](class_int) [[#surface_get_primitive_type|surface_get_primitive_type]]**(** [int](class_int) surf_idx **)** const
  * void [[#surface_set_material|surface_set_material]]**(** [int](class_int) surf_idx, [Material](class_material) material **)**
  * [Material](class_material) [[#surface_get_material|surface_get_material]]**(** [int](class_int) surf_idx **)** const
  * void [[#surface_set_name|surface_set_name]]**(** [int](class_int) surf_idx, [String](class_string) name **)**
  * [String](class_string) [[#surface_get_name|surface_get_name]]**(** [int](class_int) surf_idx **)** const
  * void [[#center_geometry|center_geometry]]**(****)**
##  Numeric Constants  
  * **NO_INDEX_ARRAY** = **-1** - Default value used for index_array_len when no indices are present.
  * **ARRAY_WEIGHTS_SIZE** = **4** - Amount of weights/bone indices per vertex (always 4).
  * **ARRAY_VERTEX** = **0** - Vertex array (array of [Vector3]() vertices).
  * **ARRAY_NORMAL** = **1** - Normal array (array of [Vector3]() normals).
  * **ARRAY_TANGENT** = **2** - Tangent array, array of groups of 4 floats. first 3 floats determine the tangent, and the last the binormal direction as -1 or 1.
  * **ARRAY_COLOR** = **3** - Vertex array (array of [Color]() colors).
  * **ARRAY_TEX_UV** = **4** - UV array (array of [Vector3]() UVs or float array of groups of 2 floats (u,v)).
  * **ARRAY_TEX_UV2** = **5**
  * **ARRAY_BONES** = **6** - Array of bone indices, as a float array. Each element in groups of 4 floats.
  * **ARRAY_WEIGHTS** = **7** - Array of bone weights, as a float array. Each element in groups of 4 floats.
  * **ARRAY_INDEX** = **8** - Array of integers, used as indices referencing vertices. No index can be beyond the vertex array size.
  * **ARRAY_FORMAT_VERTEX** = **1** - Array format will include vertices (mandatory).
  * **ARRAY_FORMAT_NORMAL** = **2** - Array format will include normals
  * **ARRAY_FORMAT_TANGENT** = **4** - Array format will include tangents
  * **ARRAY_FORMAT_COLOR** = **8** - Array format will include a color array.
  * **ARRAY_FORMAT_TEX_UV** = **16** - Array format will include UVs.
  * **ARRAY_FORMAT_TEX_UV2** = **32**
  * **ARRAY_FORMAT_BONES** = **64** - Array format will include bone indices.
  * **ARRAY_FORMAT_WEIGHTS** = **128** - Array format will include bone weights.
  * **ARRAY_FORMAT_INDEX** = **256** - Index array will be used.
  * **PRIMITIVE_POINTS** = **0** - Render array as points (one vertex equals one point).
  * **PRIMITIVE_LINES** = **1** - Render array as lines (every two vertices a line is created).
  * **PRIMITIVE_LINE_STRIP** = **2** - Render array as line strip.
  * **PRIMITIVE_LINE_LOOP** = **3** - Render array as line loop (like line strip, but closed).
  * **PRIMITIVE_TRIANGLES** = **4** - Render array as triangles (every three vertices a triangle is created).
  * **PRIMITIVE_TRIANGLE_STRIP** = **5** - Render array as triangle strips.
  * **PRIMITIVE_TRIANGLE_FAN** = **6** - Render array as triangle fans.
##  Description  
Mesh is a type of [[resource|Resource]] that contains vertex-array based geometry, divided in //surfaces//. Each surface contains a completely separate array and a material used to draw it. Design wise, a mesh with multiple surfaces is prefered to a single surface, because objects created in 3D editing software commonly contain multiple materials.
##  Member Function Description  
==  add_surface  ==
  * void [[#add_surface|add_surface]]**(** [int](class_int) primitive, [Array](class_array) arrays, [Array](class_array) morph_arrays, [bool](class_bool) arg3=Array() **)**
\\
Create a new surface ([[#get_surface_count|get_surface_count]] will become surf_idx for this.\\
"#10;"#9;"#9;"#9;Surfaces are created to be rendered using a "primitive", which may be PRIMITIVE_POINTS, PRIMITIVE_LINES, PRIMITIVE_LINE_STRIP, PRIMITIVE_LINE_LOOP, PRIMITIVE_TRIANGLES, PRIMITIVE_TRIANGLE_STRIP, PRIMITIVE_TRIANGLE_FAN. (As a note, when using indices, it is recommended to only use just points, lines or triangles).\\
"#10;"#9;"#9;"#9;The format of a surface determines which arrays it will allocate and hold, so "format" is a combination of ARRAY_FORMAT_* mask constants ORed together. ARRAY_FORMAT_VERTEX must be always present. "array_len" determines the amount of vertices in the array (not primitives!). if ARRAY_FORMAT_INDEX is in the format mask, then it means that an index array will be allocated and "index_array_len" must be passed.
==  get_surface_count  ==
  * [int](class_int) [[#get_surface_count|get_surface_count]]**(****)** const
\\
Return the amount of surfaces that the [[mesh|Mesh]] holds.
==  surface_remove  ==
  * void [[#surface_remove|surface_remove]]**(** [int](class_int) surf_idx **)**
\\
Remove a surface at position surf_idx, shifting greater surfaces one surf_idx slot down.
==  surface_get_array_len  ==
  * [int](class_int) [[#surface_get_array_len|surface_get_array_len]]**(** [int](class_int) surf_idx **)** const
\\
Return the length in vertices of the vertex array in the requested surface (see [[#add_surface|add_surface]]).
==  surface_get_array_index_len  ==
  * [int](class_int) [[#surface_get_array_index_len|surface_get_array_index_len]]**(** [int](class_int) surf_idx **)** const
\\
Return the length in indices of the index array in the requested surface (see [[#add_surface|add_surface]]).
==  surface_get_format  ==
  * [int](class_int) [[#surface_get_format|surface_get_format]]**(** [int](class_int) surf_idx **)** const
\\
Return the format mask of the requested surface (see [[#add_surface|add_surface]]).
==  surface_get_primitive_type  ==
  * [int](class_int) [[#surface_get_primitive_type|surface_get_primitive_type]]**(** [int](class_int) surf_idx **)** const
\\
Return the primitive type of the requested surface (see [[#add_surface|add_surface]]).
==  surface_set_material  ==
  * void [[#surface_set_material|surface_set_material]]**(** [int](class_int) surf_idx, [Material](class_material) material **)**
\\
Set a [[material|Material]] for a given surface. Surface will be rendered using this material.
==  surface_get_material  ==
  * [Material](class_material) [[#surface_get_material|surface_get_material]]**(** [int](class_int) surf_idx **)** const
\\
Return a [[material|Material]] in a given surface. Surface is rendered using this material.