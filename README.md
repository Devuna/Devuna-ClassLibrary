# About the Devuna Class Library #

----------

A public repository for some Clarion classes that you may find useful.

# ctWinPredefinedColors  #

A class that encapsulates the Windows predefined colors.  Can be used to create a color picker of WIndows predefined colors.

**ctWinPredefinedColors.def**	contains the ctWinPredefinedColorsQueueType declaration
**ctWinPredefinedColors.inc**	contains the ctWinPredefinedColors class declaration
**ctWinPredefinedColors.clw**	contains the ctWinPredefinedColors class implementation

The **Images** subfolder contains small bitmaps of the predefined colors.  These work well with a standard clarion listbox.

##Methods

GetColorName         PROCEDURE(LONG pColorValue),STRING

- **pColorValue** a Clarion color value
- **Returns** the name of the passed color value


GetColorValue        PROCEDURE(*CSTRING pColorName),LONG

- **pColorName** a Windows Predefined Color Name
- **Returns** the Clarion color value for the passed color name.

GetColorQueue        PROCEDURE(*ctWinPredefinedColorsQueueType pWinColorQueue, BYTE pFreeQueue = 0),LONG,PROC

- **pWinColorQueue** a queue of ctWinPredefinedColorsQueueType TYPE
- **pFreeQueue** frees the passed queue before adding entries if TRUE
- **Returns** the number of entries added to the queue
