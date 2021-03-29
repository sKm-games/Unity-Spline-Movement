# Unity-Spline-Movement
Unity package for creating splines and move objects along them, made with Unity 2019. Supports 2D and 3D.

System to allow an object to follow a preset spline or splines in order. Made using Unity 2019.4.0f1, but should work fine for other versions
Contains two scripts

## SplineController:
* Calculates and shows the spline using gizmos
* Spline Points - Should hold all four of the "Point" child objects, in the correct order. if these are missing and error will show
* Spline Point Icons - Holds ref to the icons used to show spline points order, for more clear editing
* Ref Color - Hold the color this spline should use, makes it easier to see the difference with multiple splines	
* Show Spline Point - Determine if the "Point" object should show during gameplay, can be changed during runtime, 
but only updates if Gizmos are turned on.
		

## SplineMovement:

Moves the actual object along given splines.

* Spline Infos Class
** Spline Path - Hold ref to the spline controller that holds the spline path
** Return - If you want the object to move back to the start along the spline
** Loops - How many times you want the object to follow this path
* Loop Splines - How many times you want the object to go through all the Splines, -1 = infinite
* Destroy When Done - If you want the object to get removed when done moving if Loop Spline is infinite this open does nothing
* RotateToward - If you want the object to rotate toward the spline
* Speed Modifier - How fast the object should move along the path

## Placeholder art:
* The number used to show spline points more clearly
* A square used for the test movement object

## Sample scene:
*Showing the system in use, with two spines and a move object setup with different looping and spline setups.

## Usage:
To create the spline move the Point object under the Spline object, if you have Gizmos turned on you should now see a series of circles showing you the spline path.
The system is made mainly for 2D but should work fine with 3D, but the RotateToward function might not work as well, depending on angles.

This system is heavily based on a Youtube tutorial by Alexander Zotov (https://www.youtube.com/watch?v=11ofnLOE8pw), but aspects have been modified and added to allow looping controls and color-coded splines


