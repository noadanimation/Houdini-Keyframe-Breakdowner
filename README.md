# Houdini Keyframe Breakdowner
Python panel for Houdini to easily add inbetween poses to animations

Inspired by (but with far less features than) https://github.com/boredstiff/tweenMachine,
and ported from our similar Cinema 4D Python Plugin https://github.com/noadanimation/C4D-Keyframe-Breakdowner

## Installation
* Copy the .pypanel file to your Houdini python_panels directory (eg C:\Users\User\Documents\houdini19.0\python_panels)
* Run Houdini, set a pane to Pane Tab Type "Misc > Python Panel", and choose "Keyframe Breakdowner" from the dropdown.
  * If it doesn't appear in the dropdown, you may need to add it to the "Pane Tab Menu Entries" field in the "Pane Tab Menu" tab of the Python Panel Editor (menu "Windows > Python Panel Editor")
* Save your desktop to keep the panel there next time you run Houdini.

## Use
With your animated node selected, press the buttons in the Keyframe Breakdowner panel to create new inbetween keyframes (or alter existing keyframes) at your current project time, with values interpolated from the nearest previous and nearest next keyframes.
   * Pressing the numbered buttons (15 through 85) will create keyframes that are 15%, 33%, 50% etc from the previous keyframe to the next keyframe.
   * Or enter a custom percentage in the text field before the 'Custom %' button, then press 'Custom %'.
   * Sliding the slider underneath those buttons does the same, but with a live view of the interpolation (the interaction can be a bit flaky on this one).

### Notes
* All channels of your node that are visible and selected in the Animation Editor are altered, you can avoid editing certain channels by deselecting them in the Channel List, or setting Channel Groups to hide unwanted channels.
* Currently only works on one node at a time.
* Tested in Houdini 19.
