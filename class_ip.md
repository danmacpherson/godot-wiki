##  IP  
**Inherits:** [[object|Object]]\\
**Category:** Core\\
##  Brief Description  
IP Protocol support functions.
##  Member Functions 
  * [String](class_string) [[#resolve_hostname|resolve_hostname]]**(** [String](class_string) host **)**
  * [int](class_int) [[#resolve_hostname_queue_item|resolve_hostname_queue_item]]**(** [String](class_string) host **)**
  * [int](class_int) [[#get_resolve_item_status|get_resolve_item_status]]**(** [int](class_int) id **)** const
  * [String](class_string) [[#get_resolve_item_address|get_resolve_item_address]]**(** [int](class_int) id **)** const
  * void [[#erase_resolve_item|erase_resolve_item]]**(** [int](class_int) id **)**
##  Numeric Constants  
  * **RESOLVER_STATUS_NONE** = **0**
  * **RESOLVER_STATUS_WAITING** = **1**
  * **RESOLVER_STATUS_DONE** = **2**
  * **RESOLVER_STATUS_ERROR** = **3**
  * **RESOLVER_MAX_QUERIES** = **32**
  * **RESOLVER_INVALID_ID** = **-1**
##  Description  
IP contains some support functions for the IPv4 protocol. TCP/IP support is in different classes (see [TCP_Client], [[tcp_server|TCP_Server]]). IP provides hostname resolution support, both blocking and threaded.
##  Member Function Description  
==  resolve_hostname  ==
  * [String](class_string) [[#resolve_hostname|resolve_hostname]]**(** [String](class_string) host **)**
\\
Resolve a given hostname, blocking. Resolved hostname is returned as an IP.
==  resolve_hostname_queue_item  ==
  * [int](class_int) [[#resolve_hostname_queue_item|resolve_hostname_queue_item]]**(** [String](class_string) host **)**
\\
Create a queue item for resolving a given hostname. The queue ID is returned, or RESOLVER_INVALID_ID on error.
==  get_resolve_item_status  ==
  * [int](class_int) [[#get_resolve_item_status|get_resolve_item_status]]**(** [int](class_int) id **)** const
\\
Return the status of hostname queued for resolving, given it"apos;s queue ID. Returned status can be any of the RESOLVER_STATUS_* enumeration.
==  get_resolve_item_address  ==
  * [String](class_string) [[#get_resolve_item_address|get_resolve_item_address]]**(** [int](class_int) id **)** const
\\
Return a resolved item address, or an empty string if an error happened or resolution didn"apos;t happen yet (see [[#get_resolve_item_status|get_resolve_item_status]]).
==  erase_resolve_item  ==
  * void [[#erase_resolve_item|erase_resolve_item]]**(** [int](class_int) id **)**
\\
Erase a queue ID, removing it from the queue if needed. This should be used after a queue is completed to free it and enable more queries to happen.