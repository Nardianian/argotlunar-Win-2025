About this fork
With this fork we only wanted to update the code for use with the latest versions of Juce (8.0.10) and Visual Studio (Community Edition 2022 version 17.14.17) therefore changes were only made to limited parts of the source code (sections of Plugin.cpp and Plugin.h and on PluginEditor.cpp and PluginEditor.h) without introducing changes in the functions or in the GUI. The potential of Juce was exploited to allow compilation in VST3, VST2, LV2, AAX and standalone formats with ASIO and Jack2 support. Remember that VST2 requires the Steinberg license while the AAX plugins are unusable if they are not activated (to activate it you must follow a specific procedure established by Avid, which requires Avid and iLok accounts, as well as the use of specific tools like iLok, AAX Validator, Pro Tools Developer Bundle, PACE Eden Signing Tools, etc.). Before doing the build, check the correspondence of the directories in the global path and in the header search path of Juce with your directories (those of the VST2, ASIO, AAX and Jack2 SDKs which must be installed in your system otherwise you need to disable this option from the juce_audio_devices module), remember juce needs these preprocessor definitions: JUCE_VST3_CAN_REPLACE_VST2=0  + JUCE_MODAL_LOOPS_PERMITTED=1 and paths for Jack2 "include" folder and Asio sdk "common" folder on the Header Search Paths tab.

Original Readme:

==========
Argotlunar
==========

<img src="argotlunar.png" width="780" height="225" />

Realtime granulator VST / AudioUnit plugin. 

Uses the JUCE toolkit. This version is based on JUCE Git 2013-02-17.

Licensed under GPLv2

[http://argotlunar.info](http://argotlunar.info)


