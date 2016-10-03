# Fast Temporal Median Filter for ImageJ

This ImageJ plugin was developed for the Milstein Lab at the University of Toronto,
with the help of Professor Josh Milstein during the summer of 2014, as part of the
Science Without Borders research opportunity program.

This plugin uses a variant of the Huang algorithm to quickly determine the temporal
median  of each pixel across a number of frames within an image stack. The  program
then creates a new stack with the running median subtracted.

With a Forward Window, the program selects a window from frames [i] to [i + Window Size]
to find the median. With a Radial Window, the window ranges from frames [i - Window Size]
to [i + Window Size]. If "Intensity Normalization" is activated, the program also
accounts for shifts in overall intensity by scaling all pixels according to the mean
intensity of each frame.

To install the plugin, follow these steps:
1. Download the JAVA file
2. Open ImageJ
3. Open the stack file
4. Go to "Plugins" -> "Install..."
5. Select the JAVA file and save it in the folder "Filters"

To use the plugin, open the stack file and go to "Plugins" -> "Filters" -> "Fast Temporal Median".
If "Fast Temporal Median" is not listed, go to "Help" -> "Refresh Menus" and try again.

Simply select the start frame and end frame of the stack, running window size, forward or
radial window, and if intensity normalization is to be used.

This plugin currently works only with 16-bit grayscale stacks.
