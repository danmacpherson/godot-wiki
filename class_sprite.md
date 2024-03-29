#  Sprite  
####**Inherits:** [Node2D](class_node2d)
####**Category:** Core

###  Brief Description  
General purpose Sprite node.

###  Member Functions 
  * void  **[set&#95;texture](#set_texture)**  **(** [Texture](class_texture) texture  **)**
  * [Texture](class_texture)  **[get&#95;texture](#get_texture)**  **(** **)** const
  * void  **[set&#95;centered](#set_centered)**  **(** [bool](class_bool) centered  **)**
  * [bool](class_bool)  **[is&#95;centered](#is_centered)**  **(** **)** const
  * void  **[set&#95;offset](#set_offset)**  **(** [Vector2](class_vector2) offset  **)**
  * [Vector2](class_vector2)  **[get&#95;offset](#get_offset)**  **(** **)** const
  * void  **[set&#95;flip&#95;h](#set_flip_h)**  **(** [bool](class_bool) flip_h  **)**
  * [bool](class_bool)  **[is&#95;flipped&#95;h](#is_flipped_h)**  **(** **)** const
  * void  **[set&#95;flip&#95;v](#set_flip_v)**  **(** [bool](class_bool) flip_v  **)**
  * [bool](class_bool)  **[is&#95;flipped&#95;v](#is_flipped_v)**  **(** **)** const
  * void  **[set&#95;region](#set_region)**  **(** [bool](class_bool) enabled  **)**
  * [bool](class_bool)  **[is&#95;region](#is_region)**  **(** **)** const
  * void  **[set&#95;region&#95;rect](#set_region_rect)**  **(** [Rect2](class_rect2) rect  **)**
  * [Rect2](class_rect2)  **[get&#95;region&#95;rect](#get_region_rect)**  **(** **)** const
  * void  **[set&#95;frame](#set_frame)**  **(** [int](class_int) frame  **)**
  * [int](class_int)  **[get&#95;frame](#get_frame)**  **(** **)** const
  * void  **[set&#95;vframes](#set_vframes)**  **(** [int](class_int) vframes  **)**
  * [int](class_int)  **[get&#95;vframes](#get_vframes)**  **(** **)** const
  * void  **[set&#95;hframes](#set_hframes)**  **(** [int](class_int) hframes  **)**
  * [int](class_int)  **[get&#95;hframes](#get_hframes)**  **(** **)** const
  * void  **[set&#95;modulate](#set_modulate)**  **(** [Color](class_color) modulate  **)**
  * [Color](class_color)  **[get&#95;modulate](#get_modulate)**  **(** **)** const

###  Description  
General purpose Sprite node. This Sprite node can show any texture as a sprite. The texture can be used as a spritesheet for animation, or only a region from a bigger texture can referenced, like an atlas.

###  Member Function Description  

#### <a name="set_texture">set_texture</a>
  * void  **set&#95;texture**  **(** [Texture](class_texture) texture  **)**

Set the base texture for the sprite.

#### <a name="get_texture">get_texture</a>
  * [Texture](class_texture)  **get&#95;texture**  **(** **)** const

Return the base texture for the sprite.

#### <a name="set_centered">set_centered</a>
  * void  **set&#95;centered**  **(** [bool](class_bool) centered  **)**

Set whether the sprite should be centered on the origin.

#### <a name="is_centered">is_centered</a>
  * [bool](class_bool)  **is&#95;centered**  **(** **)** const

Return if the sprite is centered at the local origin.

#### <a name="set_offset">set_offset</a>
  * void  **set&#95;offset**  **(** [Vector2](class_vector2) offset  **)**

Set the sprite draw offset, useful for setting rotation pivots.

#### <a name="get_offset">get_offset</a>
  * [Vector2](class_vector2)  **get&#95;offset**  **(** **)** const

Return sprite draw offst.

#### <a name="set_flip_h">set_flip_h</a>
  * void  **set&#95;flip&#95;h**  **(** [bool](class_bool) flip_h  **)**

Set true to flip the sprite horizontaly.

#### <a name="is_flipped_h">is_flipped_h</a>
  * [bool](class_bool)  **is&#95;flipped&#95;h**  **(** **)** const

Return true if the sprite is flipped horizontally.

#### <a name="set_flip_v">set_flip_v</a>
  * void  **set&#95;flip&#95;v**  **(** [bool](class_bool) flip_v  **)**

Set true to flip the sprite vertically.

#### <a name="is_flipped_v">is_flipped_v</a>
  * [bool](class_bool)  **is&#95;flipped&#95;v**  **(** **)** const

Return true if the sprite is flipped vertically.

#### <a name="set_region">set_region</a>
  * void  **set&#95;region**  **(** [bool](class_bool) enabled  **)**

Set the sprite as a sub-region of a bigger texture. Useful for texture-atlases.

#### <a name="is_region">is_region</a>
  * [bool](class_bool)  **is&#95;region**  **(** **)** const

Return if the sprite reads from a region.

#### <a name="set_region_rect">set_region_rect</a>
  * void  **set&#95;region&#95;rect**  **(** [Rect2](class_rect2) rect  **)**

Set the region rect to read from.

#### <a name="get_region_rect">get_region_rect</a>
  * [Rect2](class_rect2)  **get&#95;region&#95;rect**  **(** **)** const

Return the region rect to read from.

#### <a name="set_frame">set_frame</a>
  * void  **set&#95;frame**  **(** [int](class_int) frame  **)**

Set the texture frame for a sprite-sheet, works when vframes or hframes are greater than 1.

#### <a name="get_frame">get_frame</a>
  * [int](class_int)  **get&#95;frame**  **(** **)** const

Return the texture frame for a sprite-sheet, works when vframes or hframes are greater than 1.

#### <a name="set_vframes">set_vframes</a>
  * void  **set&#95;vframes**  **(** [int](class_int) vframes  **)**

Set the amount of vertical frames and converts the sprite into a sprite-sheet. This is useful for animation.

#### <a name="get_vframes">get_vframes</a>
  * [int](class_int)  **get&#95;vframes**  **(** **)** const

Return the amount of vertical frames. See [set_vframes].

#### <a name="set_hframes">set_hframes</a>
  * void  **set&#95;hframes**  **(** [int](class_int) hframes  **)**

Set the amount of horizontal frames and converts the sprite into a sprite-sheet. This is useful for animation.

#### <a name="get_hframes">get_hframes</a>
  * [int](class_int)  **get&#95;hframes**  **(** **)** const

Return the amount of horizontal frames. See [set_hframes].

#### <a name="set_modulate">set_modulate</a>
  * void  **set&#95;modulate**  **(** [Color](class_color) modulate  **)**

Set color modulation for the sprite. All sprite pixels are multiplied by this color.

#### <a name="get_modulate">get_modulate</a>
  * [Color](class_color)  **get&#95;modulate**  **(** **)** const

Return color modulation for the sprite. All sprite pixels are multiplied by this color.
