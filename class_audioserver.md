##  AudioServer  
**Inherits:** [[object|Object]]\\
**Category:** Core\\
##  Brief Description  
Server interface for low level audio access.
##  Member Functions 
  * [RID](class_rid) [[#sample_create|sample_create]]**(** [int](class_int) format, [bool](class_bool) stereo, [int](class_int) length **)**
  * void [[#sample_set_description|sample_set_description]]**(** [RID](class_rid) sample, [String](class_string) description **)**
  * [String](class_string) [[#sample_get_description|sample_get_description]]**(** [RID](class_rid) sample, [String](class_string) arg1 **)** const
  * [int](class_int) [[#sample_get_format|sample_get_format]]**(** [RID](class_rid) sample **)** const
  * [bool](class_bool) [[#sample_is_stereo|sample_is_stereo]]**(** [RID](class_rid) sample **)** const
  * [int](class_int) [[#sample_get_length|sample_get_length]]**(** [RID](class_rid) sample **)** const
  * void [[#sample_set_signed_data|sample_set_signed_data]]**(** [RID](class_rid) sample, [RealArray](class_realarray) data **)**
  * void [[#sample_set_data|sample_set_data]]**(** [RID](class_rid) sample, [RawArray](class_rawarray) arg1 **)**
  * [RawArray](class_rawarray) [[#sample_get_data|sample_get_data]]**(** [RID](class_rid) sample **)** const
  * void [[#sample_set_mix_rate|sample_set_mix_rate]]**(** [RID](class_rid) sample, [int](class_int) mix_rate **)**
  * [int](class_int) [[#sample_get_mix_rate|sample_get_mix_rate]]**(** [RID](class_rid) sample **)** const
  * void [[#sample_set_loop_format|sample_set_loop_format]]**(** [RID](class_rid) sample, [int](class_int) loop_format **)**
  * [int](class_int) [[#sample_get_loop_format|sample_get_loop_format]]**(** [RID](class_rid) sample **)** const
  * void [[#sample_set_loop_begin|sample_set_loop_begin]]**(** [RID](class_rid) sample, [int](class_int) pos **)**
  * [int](class_int) [[#sample_get_loop_begin|sample_get_loop_begin]]**(** [RID](class_rid) sample **)** const
  * void [[#sample_set_loop_end|sample_set_loop_end]]**(** [RID](class_rid) sample, [int](class_int) pos **)**
  * [int](class_int) [[#sample_get_loop_end|sample_get_loop_end]]**(** [RID](class_rid) sample **)** const
  * [RID](class_rid) [[#voice_create|voice_create]]**(****)**
  * void [[#voice_play|voice_play]]**(** [RID](class_rid) voice, [RID](class_rid) sample **)**
  * void [[#voice_set_volume|voice_set_volume]]**(** [RID](class_rid) voice, [real](class_real) volume **)**
  * void [[#voice_set_pan|voice_set_pan]]**(** [RID](class_rid) voice, [real](class_real) pan, [real](class_real) depth=0, [real](class_real) height=0 **)**
  * void [[#voice_set_filter|voice_set_filter]]**(** [RID](class_rid) voice, [int](class_int) type, [real](class_real) cutoff, [real](class_real) resonance, [real](class_real) gain=0 **)**
  * void [[#voice_set_chorus|voice_set_chorus]]**(** [RID](class_rid) voice, [real](class_real) chorus **)**
  * void [[#voice_set_reverb|voice_set_reverb]]**(** [RID](class_rid) voice, [int](class_int) room, [real](class_real) reverb **)**
  * void [[#voice_set_mix_rate|voice_set_mix_rate]]**(** [RID](class_rid) voice, [int](class_int) rate **)**
  * void [[#voice_set_positional|voice_set_positional]]**(** [RID](class_rid) voice, [bool](class_bool) enabled **)**
  * [real](class_real) [[#voice_get_volume|voice_get_volume]]**(** [RID](class_rid) voice **)** const
  * [real](class_real) [[#voice_get_pan|voice_get_pan]]**(** [RID](class_rid) voice **)** const
  * [real](class_real) [[#voice_get_pan_height|voice_get_pan_height]]**(** [RID](class_rid) voice **)** const
  * [real](class_real) [[#voice_get_pan_depth|voice_get_pan_depth]]**(** [RID](class_rid) voice **)** const
  * [int](class_int) [[#voice_get_filter_type|voice_get_filter_type]]**(** [RID](class_rid) voice **)** const
  * [real](class_real) [[#voice_get_filter_cutoff|voice_get_filter_cutoff]]**(** [RID](class_rid) voice **)** const
  * [real](class_real) [[#voice_get_filter_resonance|voice_get_filter_resonance]]**(** [RID](class_rid) voice **)** const
  * [real](class_real) [[#voice_get_chorus|voice_get_chorus]]**(** [RID](class_rid) voice **)** const
  * [int](class_int) [[#voice_get_reverb_type|voice_get_reverb_type]]**(** [RID](class_rid) voice **)** const
  * [real](class_real) [[#voice_get_reverb|voice_get_reverb]]**(** [RID](class_rid) voice **)** const
  * [int](class_int) [[#voice_get_mix_rate|voice_get_mix_rate]]**(** [RID](class_rid) voice **)** const
  * [bool](class_bool) [[#voice_is_positional|voice_is_positional]]**(** [RID](class_rid) voice **)** const
  * void [[#voice_stop|voice_stop]]**(** [RID](class_rid) voice **)**
  * void [[#free|free]]**(** [RID](class_rid) rid **)**
  * void [[#set_stream_global_volume_scale|set_stream_global_volume_scale]]**(** [real](class_real) scale **)**
  * [real](class_real) [[#get_stream_global_volume_scale|get_stream_global_volume_scale]]**(****)** const
  * void [[#set_fx_global_volume_scale|set_fx_global_volume_scale]]**(** [real](class_real) scale **)**
  * [real](class_real) [[#get_fx_global_volume_scale|get_fx_global_volume_scale]]**(****)** const
  * void [[#set_event_voice_global_volume_scale|set_event_voice_global_volume_scale]]**(** [real](class_real) scale **)**
  * [real](class_real) [[#get_event_voice_global_volume_scale|get_event_voice_global_volume_scale]]**(****)** const
##  Numeric Constants  
  * **SAMPLE_FORMAT_PCM8** = **0** - Sample format is 8 bits, signed.
  * **SAMPLE_FORMAT_PCM16** = **1** - Sample format is 16 bits, signed.
  * **SAMPLE_FORMAT_IMA_ADPCM** = **2** - Sample format is IMA-ADPCM compressed.
  * **SAMPLE_LOOP_NONE** = **0** - Sample does not loop.
  * **SAMPLE_LOOP_FORWARD** = **1** - Sample loops in forward mode.
  * **SAMPLE_LOOP_PING_PONG** = **2** - Sample loops in a bidirectional way.
  * **FILTER_NONE** = **0** - Filter is disable.
  * **FILTER_LOWPASS** = **1** - Filter is a resonant lowpass.
  * **FILTER_BANDPASS** = **2** - Filter is a resonant bandpass.
  * **FILTER_HIPASS** = **3** - Filter is a resonant highpass.
  * **FILTER_NOTCH** = **4** - Filter is a notch.
  * **FILTER_BANDLIMIT** = **6** - Filter is a bandlimit (resonance used as highpass).
  * **REVERB_SMALL** = **0** - Small reverb room (closet, bathroom, etc).
  * **REVERB_MEDIUM** = **1** - Medium reverb room (living room)
  * **REVERB_LARGE** = **2** - Large reverb room (warehouse).
  * **REVERB_HALL** = **3** - Large reverb room with long decay.
##  Description  
AudioServer is a low level server interface for audio access. It is"#10;"#9;in charge of creating sample data (playable audio) as well as it's"#10;"#9;playback via a voice interface.
##  Member Function Description  
==  sample_create  ==
  * [RID](class_rid) [[#sample_create|sample_create]]**(** [int](class_int) format, [bool](class_bool) stereo, [int](class_int) length **)**
\\
Create an audio sample, return a [[rid|RID]] referencing"#10;"#9;"#9;"#9;it. The sample will be created with a given format"#10;"#9;"#9;"#9;(from the SAMPLE_FORMAT_* enum), a total length (in"#10;"#9;"#9;"#9;frames, not samples or bytes), in either stereo or"#10;"#9;"#9;"#9;mono.
==  sample_set_description  ==
  * void [[#sample_set_description|sample_set_description]]**(** [RID](class_rid) sample, [String](class_string) description **)**
\\
Set the description of an audio sample. Mainly used"#10;"#9;"#9;"#9;for organization.
==  sample_get_description  ==
  * [String](class_string) [[#sample_get_description|sample_get_description]]**(** [RID](class_rid) sample, [String](class_string) arg1 **)** const
\\
Return the description of an audio sample. Mainly"#10;"#9;"#9;"#9;used for organization.
==  sample_get_format  ==
  * [int](class_int) [[#sample_get_format|sample_get_format]]**(** [RID](class_rid) sample **)** const
\\
Return the format of the audio sample, in the form"#10;"#9;"#9;"#9;of the SAMPLE_FORMAT_* enum.
==  sample_is_stereo  ==
  * [bool](class_bool) [[#sample_is_stereo|sample_is_stereo]]**(** [RID](class_rid) sample **)** const
\\
Return wether the sample is stereo (2 channels)
==  sample_get_length  ==
  * [int](class_int) [[#sample_get_length|sample_get_length]]**(** [RID](class_rid) sample **)** const
\\
Return the length in frames of the audio sample (not"#10;"#9;"#9;"#9;samples or bytes).
==  sample_set_signed_data  ==
  * void [[#sample_set_signed_data|sample_set_signed_data]]**(** [RID](class_rid) sample, [RealArray](class_realarray) data **)**
\\
Set the sample data for a given sample as an array"#10;"#9;"#9;"#9;of floats. The length must be equal to the sample"#10;"#9;"#9;"#9;lenght or an error will be produced.
==  sample_set_data  ==
  * void [[#sample_set_data|sample_set_data]]**(** [RID](class_rid) sample, [RawArray](class_rawarray) arg1 **)**
\\
Set the sample data for a given sample as an array"#10;"#9;"#9;"#9;of bytes. The length must be equal to the sample"#10;"#9;"#9;"#9;lenght expected in bytes or an error will be produced.
==  sample_get_data  ==
  * [RawArray](class_rawarray) [[#sample_get_data|sample_get_data]]**(** [RID](class_rid) sample **)** const
\\
Return the sample data as an array of bytes. The"#10;"#9;"#9;"#9;length will be the expected length in bytes.
==  sample_set_mix_rate  ==
  * void [[#sample_set_mix_rate|sample_set_mix_rate]]**(** [RID](class_rid) sample, [int](class_int) mix_rate **)**
\\
Change the default mix rate of a given sample.
==  sample_get_mix_rate  ==
  * [int](class_int) [[#sample_get_mix_rate|sample_get_mix_rate]]**(** [RID](class_rid) sample **)** const
\\
Return the mix rate of the given sample.
==  sample_set_loop_format  ==
  * void [[#sample_set_loop_format|sample_set_loop_format]]**(** [RID](class_rid) sample, [int](class_int) loop_format **)**
\\
Set the loop format for a sample from the"#10;"#9;"#9;"#9;SAMPLE_LOOP_* enum. As a warning, Ping Pong loops"#10;"#9;"#9;"#9;may not be available on some hardware-mixing"#10;"#9;"#9;"#9;platforms.
==  sample_get_loop_format  ==
  * [int](class_int) [[#sample_get_loop_format|sample_get_loop_format]]**(** [RID](class_rid) sample **)** const
\\
Return the loop format for a sample, as a value from"#10;"#9;"#9;"#9;the SAMPLE_LOOP_* enum.
==  sample_set_loop_begin  ==
  * void [[#sample_set_loop_begin|sample_set_loop_begin]]**(** [RID](class_rid) sample, [int](class_int) pos **)**
\\
Set the initial loop point of a sample. Only has"#10;"#9;"#9;"#9;effect if sample loop is enabled. See [[#sample_set_loop_format|sample_set_loop_format]].
==  sample_get_loop_begin  ==
  * [int](class_int) [[#sample_get_loop_begin|sample_get_loop_begin]]**(** [RID](class_rid) sample **)** const
\\
Return the initial loop point of a sample. Only has"#10;"#9;"#9;"#9;effect if sample loop is enabled. See [[#sample_set_loop_format|sample_set_loop_format]].
==  sample_set_loop_end  ==
  * void [[#sample_set_loop_end|sample_set_loop_end]]**(** [RID](class_rid) sample, [int](class_int) pos **)**
\\
Set the final loop point of a sample. Only has"#10;"#9;"#9;"#9;effect if sample loop is enabled. See [[#sample_set_loop_format|sample_set_loop_format]].
==  sample_get_loop_end  ==
  * [int](class_int) [[#sample_get_loop_end|sample_get_loop_end]]**(** [RID](class_rid) sample **)** const
\\
Return the final loop point of a sample. Only has"#10;"#9;"#9;"#9;effect if sample loop is enabled. See [[#sample_set_loop_format|sample_set_loop_format]].
==  voice_create  ==
  * [RID](class_rid) [[#voice_create|voice_create]]**(****)**
\\
Allocate a voice for playback. Voices are"#10;"#9;"#9;"#9;persistent. A voice can play a single sample at the"#10;"#9;"#9;"#9;same time. See [[#sample_create|sample_create]].
==  voice_play  ==
  * void [[#voice_play|voice_play]]**(** [RID](class_rid) voice, [RID](class_rid) sample **)**
\\
Start playback of a given voice using a given"#10;"#9;"#9;"#9;sample. If the voice was already playing it will be"#10;"#9;"#9;"#9;restarted.
==  voice_set_volume  ==
  * void [[#voice_set_volume|voice_set_volume]]**(** [RID](class_rid) voice, [real](class_real) volume **)**
\\
Change the volume of a currently playing voice."#10;"#9;"#9;"#9;Volume is expressed as linear gain where 0.0 is mute"#10;"#9;"#9;"#9;and 1.0 is default.
==  voice_set_pan  ==
  * void [[#voice_set_pan|voice_set_pan]]**(** [RID](class_rid) voice, [real](class_real) pan, [real](class_real) depth=0, [real](class_real) height=0 **)**
\\
Change the pan of a currently playing voice and,"#10;"#9;"#9;"#9;optionally, the depth and height for a positional/3D"#10;"#9;"#9;"#9;sound. Panning values are expressed within the -1 to"#10;"#9;"#9;"#9;+1 range.
==  voice_set_filter  ==
  * void [[#voice_set_filter|voice_set_filter]]**(** [RID](class_rid) voice, [int](class_int) type, [real](class_real) cutoff, [real](class_real) resonance, [real](class_real) gain=0 **)**
\\
Set a resonant filter post processing for the voice."#10;"#9;"#9;"#9;Filter type is a value from the FILTER_* enum.
==  voice_set_chorus  ==
  * void [[#voice_set_chorus|voice_set_chorus]]**(** [RID](class_rid) voice, [real](class_real) chorus **)**
\\
Set chorus send post processing for the voice (from"#10;"#9;"#9;"#9;0 to 1).
==  voice_set_reverb  ==
  * void [[#voice_set_reverb|voice_set_reverb]]**(** [RID](class_rid) voice, [int](class_int) room, [real](class_real) reverb **)**
\\
Set the reverb send post processing for the voice (from"#10;"#9;"#9;"#9;0 to 1) and the reverb type, from the REVERB_* enum.
==  voice_set_mix_rate  ==
  * void [[#voice_set_mix_rate|voice_set_mix_rate]]**(** [RID](class_rid) voice, [int](class_int) rate **)**
\\
Set a different playback mix rate for the given"#10;"#9;"#9;"#9;voice.
==  voice_set_positional  ==
  * void [[#voice_set_positional|voice_set_positional]]**(** [RID](class_rid) voice, [bool](class_bool) enabled **)**
\\
Set wether a given voice is positional. This is only"#10;"#9;"#9;"#9;interpreted as a hint and used for backends that may"#10;"#9;"#9;"#9;support binaural encoding.
==  voice_get_volume  ==
  * [real](class_real) [[#voice_get_volume|voice_get_volume]]**(** [RID](class_rid) voice **)** const
\\
Return the current volume for a given voice.
==  voice_get_pan  ==
  * [real](class_real) [[#voice_get_pan|voice_get_pan]]**(** [RID](class_rid) voice **)** const
\\
Return the current pan for a given voice (-1 to +1"#10;"#9;"#9;"#9;range).
==  voice_get_pan_height  ==
  * [real](class_real) [[#voice_get_pan_height|voice_get_pan_height]]**(** [RID](class_rid) voice **)** const
\\
Return the current pan height for a given voice (-1 to +1"#10;"#9;"#9;"#9;range).
==  voice_get_pan_depth  ==
  * [real](class_real) [[#voice_get_pan_depth|voice_get_pan_depth]]**(** [RID](class_rid) voice **)** const
\\
Return the current pan depth for a given voice (-1 to +1"#10;"#9;"#9;"#9;range).
==  voice_get_filter_type  ==
  * [int](class_int) [[#voice_get_filter_type|voice_get_filter_type]]**(** [RID](class_rid) voice **)** const
\\
Return the current selected filter type for a given"#10;"#9;"#9;"#9;voice, from the FILTER_* enum.
==  voice_get_filter_cutoff  ==
  * [real](class_real) [[#voice_get_filter_cutoff|voice_get_filter_cutoff]]**(** [RID](class_rid) voice **)** const
\\
Return the current filter cutoff (in hz) for a given"#10;"#9;"#9;"#9;voice.
==  voice_get_filter_resonance  ==
  * [real](class_real) [[#voice_get_filter_resonance|voice_get_filter_resonance]]**(** [RID](class_rid) voice **)** const
\\
Return the current filter resonance for a given"#10;"#9;"#9;"#9;voice.
==  voice_get_chorus  ==
  * [real](class_real) [[#voice_get_chorus|voice_get_chorus]]**(** [RID](class_rid) voice **)** const
\\
Return the current chorus send for a given"#10;"#9;"#9;"#9;voice (0 to 1).
==  voice_get_reverb_type  ==
  * [int](class_int) [[#voice_get_reverb_type|voice_get_reverb_type]]**(** [RID](class_rid) voice **)** const
\\
Return the current reverb type for a given voice"#10;"#9;"#9;"#9;from the REVERB_* enum.
==  voice_get_reverb  ==
  * [real](class_real) [[#voice_get_reverb|voice_get_reverb]]**(** [RID](class_rid) voice **)** const
\\
Return the current reverb send for a given voice"#10;"#9;"#9;"#9;(0 to 1).
==  voice_get_mix_rate  ==
  * [int](class_int) [[#voice_get_mix_rate|voice_get_mix_rate]]**(** [RID](class_rid) voice **)** const
\\
Return the current mix rate for a given voice.
==  voice_is_positional  ==
  * [bool](class_bool) [[#voice_is_positional|voice_is_positional]]**(** [RID](class_rid) voice **)** const
\\
Return wether the current voice is positional. See"#10;"#9;"#9;"#9;[[#voice_set_positional|voice_set_positional]].
==  voice_stop  ==
  * void [[#voice_stop|voice_stop]]**(** [RID](class_rid) voice **)**
\\
Stop a given voice.
==  free  ==
  * void [[#free|free]]**(** [RID](class_rid) rid **)**
\\
Free a [[rid|RID]] resource.
==  set_stream_global_volume_scale  ==
  * void [[#set_stream_global_volume_scale|set_stream_global_volume_scale]]**(** [real](class_real) scale **)**
\\
Set global scale for stream playback. Default is 1.0.
==  get_stream_global_volume_scale  ==
  * [real](class_real) [[#get_stream_global_volume_scale|get_stream_global_volume_scale]]**(****)** const
\\
Return the global scale for stream playback.