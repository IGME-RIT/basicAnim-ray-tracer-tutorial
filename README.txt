Documentation Author: Niko Procopi 2019

This tutorial was designed for Visual Studio 2017 / 2019
If the solution does not compile, retarget the solution
to a different version of the Windows SDK. If you do not
have any version of the Windows SDK, it can be installed
from the Visual Studio Installer Tool

Welcome to the Render Tutorial!
Prerequesites: AVI Movie

This tutorial does not depend on the previous tutorial with compute shaders.
Here, we set the Frame Rate and the duration (in seconds) of the final video,
rather than setting a number of frames that are locked at 60 FPS. All changes
are in Main.cpp

Near the top of the page, we add the variables videoFPS and videoSeconds,
these are the FPS and duration of the final video, while the variables called
"fps" and "totalTime" are related to the time of the program's duration, and
the number of frames that are rendered per second. Don't get confused by those

Maximum number of frames will be equal to videoFPS x videoSeconds

Near the end of the tutorial (last few lines in main.cpp), we use sprintf to 
modify the command that we use to generate the AVI video from PNG 
images. The only variable we modify is the frame rate of the video, but
plenty more can be modified if someody ever wanted to