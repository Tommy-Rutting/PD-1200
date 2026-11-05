
PD 1200 is an emulation of the E-mu SP-1200 Audio Engine, not it's sequencer, you need a DAW or other MIDI device for that. This is my very first Pure Data project, so you may encounter unconventional or remarkable solutions for certain problems when looking at how the patch works. This is a short manual. Installation is very straightforward: install Plugdata, copy the files to the Plugdata folder, and load it as a standalone or as a plug-in in your DAW (see below). You will also find some explanation here on how it works.

Installation

1.	It is built in Plugdata. You might be wondering: what is Plugdata? Plugdata is a modern, open-source visual programming environment designed to bring the power of Pure Data (Pd) directly to your DAW as an audio plug-in. Think of it as a modular sandbox—similar to Max for Live or Reaktor—built on a highly responsive, JUCE-powered user interface. Thanks to seamless DAW integration, it runs natively as a VST3, AU, or LV2 plug-in inside every major host (such as Ableton Live, Logic Pro, Bitwig, Reaper, and FL Studio). Install Plugdata version 0.9.3 or newer. This automatically installs the VST3, AU, and CLAP plug-ins for your DAW so you can load the patch in your DAW: plugdata.org.
2.   First, copy the extracted contents of the Plugdata folder from this download to /Users/[yourname]/Documents/Plugdata on macOS, to C:\Users\[YourUsername]\Documents\plugdata on Windows, or to /home/[yourusername]/Documents/plugdata on Linux.
3.	Load the Plugdata plug-in in your DAW, open the Plugdata plug-in, click on the three lines in the top left, click Open Patch…, and open file beginning with PD 1200(some version).pd .
6.	Press the performance button at the top center (or use the shortcut Cmd + E on macOS or the Windows/Linux equivalent) to switch to presentation or run mode. If you stay in edit mode, you run the risk of shifting the faceplate or altering the programming of the patch. So be careful! Should this happen anyway, press Cmd + Z (undo) on macOS or the Windows/Linux equivalent.
7.	You will likely want to zoom out a bit; the faceplate is 1920 x 1522 pixels, so it is quite large. You can zoom back in later when needed to set the start and end points very accurately.	

Features & Workflow

•	Presets: The Setup button loads a standard default preset included in the Plugdata folder. You can save your own default preset by sampling into the 8 voices and pressing the Save button. Note: this does not load project-specifically in your DAW. For that, use the save buttons of the voices themselves (see the chapter on Saving Samples in this short manual).

•	Sampling: To sample into a specific voice (1 through 8), press the small red button for that voice in the Performance section. Next, you can press Monitor to hear your input signal and listen to how it sounds when you overdrive the input. Adjust the recording level in the top right corner and press the red Record button to record the input. It always records for exactly 5 seconds. I may build a threshold trigger function in the future.

•	Loading Samples: The small blue button in the Performance section loads a sample into the selected voice. The PD 1200 loads a specific file sampled at 26.040 kHz / 12-bit. Therefore, you must first save a sample or load the demo samples included with the patch. You need to save all 8 voices to a location in order for them to load correctly in the DAW project you are working on. It is best to create a folder with the same name as your DAW project to save the 8 voices/samples into; the patch will then automatically load those samples when you close and reopen that session.	

•	Sample Rates & Authenticity: Set your DAW's audio settings (or Plugdata's own settings when used standalone) to at least 88.2 kHz or 96 kHz for an authentic E-mu SP-1200 sound. This prevents unwanted extra aliasing during recording and playback. You can use 44.1 kHz or 48 kHz if you prefer a slightly more aliased sound and want better CPU performance.

•	Saving Samples: You must first sample in the PD 1200 before using the small white Save button in the Performance section, or to save the demo samples already present after loading them. Samples saved this way are retained between different DAW projects; the patch will automatically reload the samples saved within that project. Tip: It is strongly recommended to create a dedicated project folder to save your 8-voice sample sets, as explained above.	

•	Choke Groups: Just like on the original hardware, voices can cut off (choke) their own audio playback by sharing the same output channel. Activate this feature by pressing the CHOKE button in the bottom left corner. You can select which voices are part of the choke group by pressing the small white buttons next to the trigger pads. I may make an additional, separate choke group for the hi-hat in the future.	

•	Filter Toggle: There is also a filter button you can toggle on/off. This acts like the half-pulled jack trick on the rear output of the original SP-1200, bypassing the internal filters and giving the voices the full frequency range.

•	Decay: Above the start and end sliders there is a rotary knob that goes from 0 to 31 0 is a very short decay to 30 which is the max decay and 31 is no decay like the original SP 1200.

Final Notes
I am going to try to turn it into a full-fledged VST, AU, CLAP, and LV2 plug-in if I have more time. This emulation is built to have the variable pitch-sample rate of 26.041 kHz, 12-bit sound, without compromising down to 44100+ Hz or 16+ bit. It is a true 12-bit 26.040 kHz EMU SP-1200 sampler inside a modern 44100+ Hz / 16+ bit DAW environment. That is also why the patch does not load standard WAV formats. Although it does not contain the original menu structure, it comes very, very close to the original in terms of sound! A lot of work has gone into it. ;-)
Make fat tracks with the PD 1200!
Tommy




