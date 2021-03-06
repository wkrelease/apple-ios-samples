GLTextureAtlas

================================================================================
DESCRIPTION:

This sample demonstrates how to use a texture atlas to draw multiple objects with different textures simultaneously using OpenGL ES.

It shows how to:
	* create PVR textures in an Xcode project build phase using texturetool;
	* load a PVR texture and display it using OpenGL ES;
	* create interleaved (tightly packed) vertex array;
	* join triangle strips together by adding in degenerated triangles;
	* compute 3D transformations using matrices and homogeneous coordinates (x,y,z,1).
 
This sample also uses some unrelated techniques, including random number generators, and depth-sorted blended particle system.

================================================================================
BUILD REQUIREMENTS:

iOS 5.0 SDK

================================================================================
RUNTIME REQUIREMENTS:

iOS 5.0 or later

================================================================================
PACKAGING LIST:

PVRTexture.h
PVRTexture.m
The PVRTexture class is responsible for loading .pvr files generated by texturetool.

GLTextureAtlasViewController.h
GLTextureAtlasViewController.m
The GLTextureAtlasViewController class is a GLKViewController subclass that renders OpenGL scene. It demonstrates how to bind a texture atlas once, and draw multiple objects with different textures using one draw call.

GLTextureAtlasAppDelegate.h
GLTextureAtlasAppDelegate.m
The GLTextureAtlasAppDelegate class is the app delegate that ties everything together.

butterfly_2.pvr
butterfly_4.pvr
These are the pvr files generated from the butterfly.png image by the "Run Script" build phase.

================================================================================
CHANGES FROM PREVIOUS VERSIONS:

Version 1.6
Updated with GLKViewController and GLKMatrix. Updated for 64 bit.

Version 1.5
Changed deployment target back to iPhone OS 3.2 and added CFBundleIconFiles in Info.plist.

Version 1.4
Upgraded project to build with the iOS 4 SDK.

Version 1.3
Fixed a bug when running in the simulator.

Version 1.2
Modified the script so that it works regardless where texturetool is installed.

Version 1.1
Updated for iPhone OS 3.1. Use CADisplayLink as the preferred method for controlling animation timing, and fall back to NSTimer when running on a pre 3.1 device where CADisplayLink is not available.

================================================================================
Copyright (C) 2009-2014 Apple Inc. All rights reserved.