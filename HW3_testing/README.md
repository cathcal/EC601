#README:

#AWS Test Farm:
- Ran AWS Built-in Fuzz Test on package com.google.identitytoolkit.demo with a 6000 Event Count
- Test was run on 5 device emulators: Samsung Galaxy S5, LG G Pad, Samsung Galaxy Tab 4, Amazon Kindle fire HDX 7, and Samsung Galaxy S6
- After running, only the Samsung Galaxy S6 passed, since that is the emulator I used when creating the application in HW 2
- Picures of the set up steps and device test results are seen in the HW3_testing folder of this repository
- The log files are also seen in this folder as zip files, as these log files are too large to view directly on git hub. The logs were downloaded directly from the AWS Test Farm after the application testing was complete.
- A video of the Samsung Galaxy S6 during the Fuzz Test is also included, it was downloaded as an output of the Fuzz Test


#Monkey Test:
- Had to install adb and activate emulator before Monkey test could be run
- Ran Monkey Test on Samsung Galaxy S6 emulator three times, with 100, 500, and 1000 events respectively
$ adb shell monkey -p com.google.identitytoolkit.demo -v 100 > 100.txt
- The Monkey Test then performed the events and put the output into corresponding text files (seen in this folder)
- At 100, 500, and 1000 events there were 0 dropped keys, pointers, trackballs, flips, and rotations, as seen at the bottom of 100.txt, 500.txt, and 1000.txt


- Learned how an AWS Test and a Monkey Test work and how to use these tools to look through errors and find problems that need to be addressed when developing code.
- Lookng through the AWS Test Farm log file outputs was very helpful for seeing where the errors occured in the different device emulators
