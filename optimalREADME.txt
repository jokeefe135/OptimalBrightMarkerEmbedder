# Optimal BrightMarker Embedder (OBE)

OBE is a Blender add-on that embeds codes in 3D models, and determines optimal embed locations on said models. Developed with Blender 3.4 Python API.

## Setup

1. **Install OBE.**
  
To install OBE, navigate to Edit -> Preferences -> Add-ons and click "Install...". Select obe.py in your files, and the add-on will be installed. Make sure it's enabled by checking the box to the left of its name.  
  
 2. **Enable LoopTools.**
  
OBE uses a Blender add-on called LoopTools. Navigate to Edit -> Preferences -> Add-ons, search "Mesh: LoopTools" (make sure that "Enabled Add-ons Only" is not checked or LoopTools won't show up), and check the box next to its name to enable it.
  
3. **Disable Auto Perspective.**
  
Navigate to Edit -> Preferences -> Navigation and make sure that Auto -> Perspective is not checked.

## Usage

Import your model (any 3D file type) and code (.svg) into Blender. Note that the code will import as a collection of curves. Ensure that Blender is in Object Mode, and select the model you would like to embed in. 
![image info](https://i.ibb.co/brKTGB7/Untitled.png)

Navigate to Object -> Optimal BrightMarker Embedder.

**Modes**  
OBE has three modes to choose from, each of which can be activated by checking/un-checking the "Enabled" box. Note that only one mode can be used at a time.

1. **Determine Optimal Locations**

This mode determines and displays the best tag locations on the model. "Max Faces" and "Accuracy" will impact parts of the algorithm, and are best left at their default values. Increasing "Sharpness" allows for more curved surfaces to be included as possible locations (again, the default is recommended). Min / Max side length set the range of values for the side length of a square code, or locations in this case. "Number of Tags" is the number of locations that will be displayed. "Ignore Bottom" means that no locations on the bottom of the model (within 15 degrees of the negative z axis) will be displayed.

2. **Embed Optimal Locations**

Parameters present in this mode that aren't explained serve the same purpose as they do in other modes. "File Name" is the name of your imported SVG. "Code Offset" determines how deeply the code will be embedded in the model from its surface. "Code Thickness" determines how thick the embedded code will be. "Align Local Z Rotation" sets the local Z rotation of all embedded codes (the +x axis is 0 degrees, the +y axis is 90 degrees).

3. **Embed Manual Locations**

Enter Edit Mode, and select a face. This face will serve as a point location where the code will be embedded. You can select multiple faces, and a code will be embedded at each location. After selecting your faces, make sure to return to Object Mode to run OBE.