Documentation Author: Niko Procopi 2019

This tutorial was designed for Visual Studio 2017 / 2019
If the solution does not compile, retarget the solution
to a different version of the Windows SDK. If you do not
have any version of the Windows SDK, it can be installed
from the Visual Studio Installer Tool

Welcome to the Basic Animation Tutorial!
Prerequesites: Set FPS Tutorial

In this tutorial, we create a new uniform to send the 
total elapsed time to the Fragment shader. In the 
fragment shader, we move the light and the cube around
the scene.

Every time the fragment shader begins, the light and 
cube are automatically moved back to their original positions,
because changes in the arrays (lights and triangles) are
not saved in any way. Then, every time a pixel is
processed, the new position of the light and the new
position of every vertex of every triangle of the cube 
need to be calculated. These calculations are in void main()
of the fragment shader.

In the future, we will use a compute shader to calculate the
positions (and rotations, and scales) one time per frame, and
then the fragment shader will get an array of triangles from
the compute shader, then the fragment shader will use that array
of triangles (and lights).

That way, the calculations are done once per frame, rather than
thousands of times per frame (once per pixel).