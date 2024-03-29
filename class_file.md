#  File  
####**Inherits:** [Reference](class_reference)
####**Category:** Core

###  Brief Description  


###  Member Functions 
  * [int](class_int)  **[open](#open)**  **(** [String](class_string) path, [int](class_int) flags  **)**
  * void  **[close](#close)**  **(** **)**
  * [bool](class_bool)  **[is&#95;open](#is_open)**  **(** **)** const
  * void  **[seek](#seek)**  **(** [int](class_int) pos  **)**
  * void  **[seek&#95;end](#seek_end)**  **(** [int](class_int) pos=0  **)**
  * [int](class_int)  **[get&#95;pos](#get_pos)**  **(** **)** const
  * [int](class_int)  **[get&#95;len](#get_len)**  **(** **)** const
  * [bool](class_bool)  **[eof&#95;reached](#eof_reached)**  **(** **)** const
  * [int](class_int)  **[get&#95;8](#get_8)**  **(** **)** const
  * [int](class_int)  **[get&#95;16](#get_16)**  **(** **)** const
  * [int](class_int)  **[get&#95;32](#get_32)**  **(** **)** const
  * [int](class_int)  **[get&#95;64](#get_64)**  **(** **)** const
  * [real](class_real)  **[get&#95;float](#get_float)**  **(** **)** const
  * [real](class_real)  **[get&#95;double](#get_double)**  **(** **)** const
  * [real](class_real)  **[get&#95;real](#get_real)**  **(** **)** const
  * [RawArray](class_rawarray)  **[get&#95;buffer](#get_buffer)**  **(** [int](class_int) len  **)** const
  * [String](class_string)  **[get&#95;line](#get_line)**  **(** **)** const
  * [String](class_string)  **[get&#95;as&#95;text](#get_as_text)**  **(** **)** const
  * [bool](class_bool)  **[get&#95;endian&#95;swap](#get_endian_swap)**  **(** **)**
  * void  **[set&#95;endian&#95;swap](#set_endian_swap)**  **(** [bool](class_bool) enable  **)**
  * [int](class_int)  **[get&#95;error](#get_error)**  **(** **)** const
  * void  **[get&#95;var](#get_var)**  **(** **)** const
  * [StringArray](class_stringarray)  **[get&#95;csv&#95;line](#get_csv_line)**  **(** **)** const
  * void  **[store&#95;8](#store_8)**  **(** [int](class_int) value  **)**
  * void  **[store&#95;16](#store_16)**  **(** [int](class_int) value  **)**
  * void  **[store&#95;32](#store_32)**  **(** [int](class_int) value  **)**
  * void  **[store&#95;64](#store_64)**  **(** [int](class_int) value  **)**
  * void  **[store&#95;float](#store_float)**  **(** [real](class_real) value  **)**
  * void  **[store&#95;double](#store_double)**  **(** [real](class_real) value  **)**
  * void  **[store&#95;real](#store_real)**  **(** [real](class_real) value  **)**
  * void  **[store&#95;buffer](#store_buffer)**  **(** [RawArray](class_rawarray) buffer  **)**
  * void  **[store&#95;line](#store_line)**  **(** [String](class_string) line  **)**
  * void  **[store&#95;string](#store_string)**  **(** [String](class_string) string  **)**
  * void  **[store&#95;var](#store_var)**  **(** var value  **)**
  * [bool](class_bool)  **[file&#95;exists](#file_exists)**  **(** [String](class_string) path  **)** const

###  Numeric Constants  
  * **READ** = **1**
  * **WRITE** = **2**
  * **READ_WRITE** = **3**

###  Member Function Description  
