#  Range  
####**Inherits:** [Control](class_control)
####**Category:** Core

###  Brief Description  
Abstract base class for range-based controls.

###  Member Functions 
  * [real](class_real)  **[get&#95;val](#get_val)**  **(** **)** const
  * [real](class_real)  **[get&#95;value](#get_value)**  **(** **)** const
  * [real](class_real)  **[get&#95;min](#get_min)**  **(** **)** const
  * [real](class_real)  **[get&#95;max](#get_max)**  **(** **)** const
  * [real](class_real)  **[get&#95;step](#get_step)**  **(** **)** const
  * [real](class_real)  **[get&#95;page](#get_page)**  **(** **)** const
  * [real](class_real)  **[get&#95;unit&#95;value](#get_unit_value)**  **(** **)** const
  * [bool](class_bool)  **[get&#95;rounded&#95;values](#get_rounded_values)**  **(** **)** const
  * void  **[set&#95;val](#set_val)**  **(** [real](class_real) value  **)**
  * void  **[set&#95;value](#set_value)**  **(** [real](class_real) value  **)**
  * void  **[set&#95;min](#set_min)**  **(** [real](class_real) minimum  **)**
  * void  **[set&#95;max](#set_max)**  **(** [real](class_real) maximum  **)**
  * void  **[set&#95;step](#set_step)**  **(** [real](class_real) step  **)**
  * void  **[set&#95;page](#set_page)**  **(** [real](class_real) pagesize  **)**
  * void  **[set&#95;unit&#95;value](#set_unit_value)**  **(** [real](class_real) value  **)**
  * void  **[set&#95;rounded&#95;values](#set_rounded_values)**  **(** [bool](class_bool) arg0  **)**
  * void  **[set&#95;exp&#95;unit&#95;value](#set_exp_unit_value)**  **(** [bool](class_bool) enabled  **)**
  * [bool](class_bool)  **[is&#95;unit&#95;value&#95;exp](#is_unit_value_exp)**  **(** **)** const
  * void  **[share](#share)**  **(** [Object](class_object) with  **)**
  * void  **[unshare](#unshare)**  **(** **)**

###  Signals  
  *  **value&#95;changed**  **(** [real](class_real) value  **)**
  *  **changed**  **(** **)**

###  Description  
Range is a base class for [Control](class_control) nodes that change a floating point _value_ between a need a _minimum_, _maximum_, using _step_ and _page_, for example a [ScrollBar](class_scrollbar).

###  Member Function Description  

#### <a name="get_val">get_val</a>
  * [real](class_real)  **get&#95;val**  **(** **)** const

Return the current value.

#### <a name="get_min">get_min</a>
  * [real](class_real)  **get&#95;min**  **(** **)** const

Return the minimum value.

#### <a name="get_max">get_max</a>
  * [real](class_real)  **get&#95;max**  **(** **)** const

Return the maximum value.

#### <a name="get_step">get_step</a>
  * [real](class_real)  **get&#95;step**  **(** **)** const

Return the stepping, if step is 0, stepping is disabled.

#### <a name="get_page">get_page</a>
  * [real](class_real)  **get&#95;page**  **(** **)** const

Return the page size, if page is 0, paging is disabled.

#### <a name="get_unit_value">get_unit_value</a>
  * [real](class_real)  **get&#95;unit&#95;value**  **(** **)** const

Return value mapped to 0 to 1 (unit) range.

#### <a name="set_min">set_min</a>
  * void  **set&#95;min**  **(** [real](class_real) minimum  **)**

Set minimum value, clamped range value to it if it"apos;s less.

#### <a name="set_step">set_step</a>
  * void  **set&#95;step**  **(** [real](class_real) step  **)**

Set step value. If step is 0, stepping will be disabled.

#### <a name="set_page">set_page</a>
  * void  **set&#95;page**  **(** [real](class_real) pagesize  **)**

Set page size. Page is mainly used for scrollbars or anything that controls text scrolling.

#### <a name="set_unit_value">set_unit_value</a>
  * void  **set&#95;unit&#95;value**  **(** [real](class_real) value  **)**

Set value mapped to 0 to 1 (unit) range, it will then be converted to the actual value within min and max.
