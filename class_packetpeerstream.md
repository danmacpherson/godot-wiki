##  PacketPeerStream  
**Inherits:** [[packetpeer|PacketPeer]]\\
**Category:** Core\\
##  Brief Description  
Wrapper to use a PacketPeer over a StreamPeer.
##  Member Functions 
  * void [[#set_stream_peer|set_stream_peer]]**(** [StreamPeer](class_streampeer) peer **)**
##  Description  
PacketStreamPeer provides a wrapper for working using packets over a stream. This allows for using packet based code with StreamPeers. PacketPeerStream implements a custom protocol over the StreamPeer, so the user should not read or write to the wrapped StreamPeer directly.
##  Member Function Description  
==  set_stream_peer  ==
  * void [[#set_stream_peer|set_stream_peer]]**(** [StreamPeer](class_streampeer) peer **)**
\\
Set the StreamPeer object to be wrapped