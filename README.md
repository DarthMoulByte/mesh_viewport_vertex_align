mesh_viewport_vertex_align
==========================
An operator for Blender 2.69.

This operator aligns selected vertices in the 3D viewport to a selected fitting function.

Features:

-3D Viewport dependent alignment. It's important to understand that this works in 2D based on your viewport--this operator doesn't know about your vertices in 3d world space, only in 2d screen space.
-Orthographic vs Perspective works.
-Cosine 'omega' can be tweaked.
-Uses a 'least squares' best fit approach.
-Anchor endpoints
-Simple to add your own 'fitting' functions if you know python and the relevant math. 


Fitting functions included:

-Linear, y = a1*x + a0

-Parabolic, y = a2*x^2 + a1*x + a0

-Cubic, y = a3*x^3 + a2*x^2 + a1*x + a0

-Cosine, y = a0 + a1*cos(w*x) + a2*cos(w*x)


Usage:
-'w' key specials menu → Select function
-Toolshelf 'Vertex Alignment' panel.
-Toolshelf Operator Panel to tweak values. 



It works as you would expect-- select the vertices you want to align, line up your 3D viewport and activate the operator. You can use it to clean up lines on a mesh-- pinpoint a flow line error and straighten it up with a parabolic fit, etc.

Note: If you are using viewport splitting, use the 'w' specials key (with your mouse in the desired viewport) to reliably activate the alignment for the viewport you want.

This operator is different from 'relax' tools from other addons, this one lines up based on your 3D viewport and 'solves', so repeated use will not further affect the alignment.
