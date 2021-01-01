v1.0.6
- Add LV2 format support (#70)
- Add new example PdStalFx (a plugin that loads patches dynamically)  
- Add camomile plugin generation script for Apple and Linux
- Fix MIDI channels correlation between Pd (0-15) and Juce (1-16)
- Fix buses with no-channels (for Debug mode only)
- Improve console for concurrent access
- Remove LibWebKit on Linux plugin for better Ardour and Carla Support (#116)
- Add support for naming buses (#114)
- Fix number boxes and symbol box ellipsis
- Add support for bypass parameter and manual bypass in the patch (#108)
- Fix param.get abstraction for the first value
- Improve IEM/atom GUIS label rendering (#118)
- Fix invisible comments in subpatches and abstractions (#120)
- Improve Font size rendering
- Add Fuzzy tests using pluginval
- Fix main patch margins

v1.0.5
- Fix warnings when audio buses are not well configured
- Fix MIDI out issue when block size is superior to 64 samples (#107)
- Improve multibus support for multichannel & side-chain - experimental with iolayout (#110)
- Add support for autoprogram to disable parameters recording within programs
- Add program updated method to notify the host that internal state has changed
- Fix plugin format recognition VST/VST3/AU
- Improve online documentation & remove locale documentation
- Add plugin's state management for dynamic reloading
- Improve background image resizing and positioning

v1.0.4
- Add label support for GUI objects (#95)
- Add graphical array support for GUI array objects (graph)  (#93)
- Add window array support for array define objects (#93)
- Add steady/jump mode for IEM's GUI slider
- Add log scale for IEM's GUI slider (#96)
- Add instructions for contributions
- Add the facultative flag "-s" to openpanel/savepanel methods to suspend processing
- Add warning if no audio bus is defined
- Fix the width of the comment
- Fix the incrementation of the number box and the atom number
- Add support to change dynamically the graphical interface (#99)
- Add support to change dynamically the latency (#62)
- Fix variable block size support (#100)
- Improve MIDI In/Out time precision
- Add support for manually and automatic dynamic reload of the patch (#101)
- Add support for abstractions/sub-patches GraphOnParent (#102)
- Fix midi pitch bend offset due to +8192 from libpd (#104)
- Remove libpd.dll dependency to the Windows versions (#94)

v1.0.3
- Fix DSP support for multiple audio buses
- Fix the number of channels in the messages sent to the patch
- Remove the name of the channels configuration in the messages sent to the patch (not coherent)
- Add buses information in the messages sent to the patch
- Add warning when the plugin code or the plugin type is not defined
- Fix the position of the popup menu for console level (#90)
- Add support when plugin is muted or not playing (#78)
- Fix missing library on Linux (#89)
- Add support for extra data to save and reload with the plugin's state (#91)

v1.0.2
- Fix DSP off message to Pd
- Prepare the DSP before opening the patch (#83)
- Initialize parameters and programs before opening the patch (#82)
- Use libpd_process_raw in the DSP perform method for optimization
- Add support for MIDI In SysEx, SysRealTime & Byte
- Add support for MIDI Out Byte
- Add full support for keys objects [key], [keyup] (#80)
- Add partial support for key objects[keyname] (perhaps some names are still missing names are missing)
- Improve the console (resizable)
- Improve prints for lists (remove line breaks)
- Floating Window always on top
- Floating Window with tabs (Console/Patch/Camomile)
- Display patch description
- Add support for compatibility versions (plugin's version of the patch <= plugin's version used)
- Add support for block size inferior to 64 samples (implies delay)
- Add support for non-real time processing
- Improve name of the UI Window
- Fix the FFT objects for multithreading support

v1.0.1
- Fix thread concurrency issue that occurred when selecting a program (#77).
- Fix stack overflow issue due to concurrent access to the Pd's stack counter (#69).
- Update documentation for VST2/VST3/AU generation on MacOS to display the name of the plugins in Ableton (#75).
- Improve the whole documentation (#72) and start "How to Create Patches" (#73).
- Add more warning when there are extra arguments in parameters' methods.
- Add support for "openpanel" and "savepanel" methods.
- Update examples Bulgroz, AlmondOrgan, Castafiore, MiniMock.
- Start/Add support for patch description in the text file (#74).
- Start/Add support for patch credits in the text file (#74).

v1.0.0
Only main changes are presented. Most of the changes will be presented during the JIM 2018 and perhaps the LAC 2018.
- Use libpd instead of my personal wrapper.
- Use TLS approach of Pd to manage thread concurrency issues.
- Use a text file to define the properties of the plugins.
- Generate plugins with the patches included.
- Separate the GUI and the parameters' definitions.

There is no ChangeLog for previous versions, sorry.
