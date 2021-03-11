# QuickFigures User Guide
# By Gregory Mazo
## Section 1: Install 
### Full Install instructions
### Fiji Install: 
#### Step 1: update Fiji (if not already up to date)
a.	Go the Help menu and select “Update…”
b.	Apply changes to make sure your Fiji is up to date
c.	Restart Fiji
#### Step 2: Install QuickFigures
d.	Go the Help->Update… menu item again
e.	After a moment, Fiji will tell you that you are up to date
f.	In the next dialog window click “Manage Update Sites”
g.	QuickFigures will appear in the update site list
h.	Check QuickFigures and close that window.
i.	Click Apply changes to download QuickFigures
j.	Restart ImageJ
### Ordinary ImageJ Install. 
#### Step 1: Install an up to date version of ImageJ. 
You can either download a fresh copy of ImageJ (recommended especially if you have an old install) or go to Help menu and choose ‘Update ImageJ…’
#### Step 2: 
a.	Download QuickFigures
https://github.com/grishkam/QuickFigures/raw/master/QuickFigures_.jar
	copy the file into the plugins folder of ImageJ
#### Step 3: Download optional dependencies for extra features
a.	If you will be opening microscopy file formats, download “loci_tools.jar” file and copy it into the plugins folder
https://downloads.openmicroscopy.org/bio-formats/4.4.12/
After installation of loci tools, one should be able to import microscopy files into ImageJ using Bio-formats (File->Import->Bio-Formats). One should set the Bio-Formats import Options to import the files as a ‘Hyperstack’ (in the stack viewing section), the import Color Mode should be set to ‘Composite’ preferably with the ‘Autoscale’ Checkbox set. All other part of the Bio-Formats import options can be left unchecked. Once those options are set, one should try a windowless Bio-formats import (also in the import menu).
b.	If you intend to export as SVG, PDF, or EPS you will need to download apache batik
https://xmlgraphics.apache.org/batik/download.html
As of this moment, Batik 1.13 or higher is required. Unzip the downloaded file and place that folder into the plugins folder of ImageJ
c.	If you intend to export as PowerPoint or use the plot package for QuickFigures you will need Apache POI.
https://poi.apache.org/download.html
As of this moment, QuickFigures is being updated to work with the latest version of apache POI (4.1.2). Those who downloaded QuickFigures before the update can download/use POI 3.12.
Copy the Apache POI folder into the plugins folder of ImageJ. Any .jar files that are in subfolders of the poi folder may need to be moved into the main POI folder
d.	Certain features of the Plot Package within QuickFigures also require Apache Commons-Math3 package. Math3 should be included in downloads of apache poi. If it is absent, 
https://commons.apache.org/proper/commons-math/
4	Go to the QuickFigures menu and select ‘Show Main Toolbar’. 

## Section 2: Getting Started 
### Creating Figures from images
1.	QuickFigures’ toolbars and windows have their own menu bars (not the same as the ImageJ Menu bar). If using a MacOS, the menu bar will appear at the top of the screen after you select one of the toolbars.
2.	You can create a new Figure using the options in the New menu (File->New) to creates figures Each of these options will create a new worksheet. The types of options are summarized below.
a.	Empty Worksheet creates a worksheet without objects. Figures can be added to any worksheet by drag and drop of image files. Dragging an image file onto an existing figure, adds another image to the figure. 
b.	Figure With Split Channels always creates a figure with split channels in a new worksheet. If an image is open in ImageJ, that image will be used to create a figure, otherwise the user will be asked to choose a file. 
c.	Figure With Merge Panels Only always creates a figure with all channels merged in a new worksheet. If an image is open in ImageJ, that image will be used to create a figure, otherwise the user will be asked to choose a file.
Note: For each of these options. The new figures created will be based on the default template (see “Setting default template”). A use can customize the default template based on their own needs.
3.	Alternatively, a user can click the “Quick Figure” button on the toolbar which works like the options in the “New” menu.
4.	You can export anything you create into other file formats using the Export menu (File->Export). Some export menu items will only appear if the required packages are installed. 
### The basics of Using QuickFigures
The ‘Object Tools’ toolbar is the main toolbar for QuickFigures. It contains all the critical tools for selecting and drawing objects. Like the ImageJ toolbar, double clicking on a tool icon displays an options dialog relevant to that tool. Similarly to the ImageJ toolbar, control clicking/right clicking on many of the tool icons allows the user to access additional tools. The most important tool families are summarized below.
The Object Selector Tool is used to click on, select and move objects within the figures. Clicking on any object selects it and deselects all others. A user can select multiple objects by holding shift while clicking on one object after another. If a user starts a mouse drag in a location without an object and drags over an area, all objects in the area will be selected after the mouse is released. When an object is selected, its handles will appear. A user can edit an object simply by dragging the handles. A user can right click on an object or handle to display a popup menu specific to the clicked object. If the user double clicks on an object or a handle, a dialog window with options specific to that object or handle may appear. If the user double clicks a text item, that item switches to “text edit mode” in which a user can edit its text via the keyboard. Clicking on another item, switches off text edit mode. For most objects, a set of icons composing a ‘mini toolbar’ will also appear below the clicked item. By clicking the icons in the mini toolbars one can perform nearly every type of edit. Most edits done with the mini toolbars apply to all selected objects. 
The Layout Selector Tool is a version of the object selector that selects only layouts (even if a layout is behind another object).
The basic shape tools can be used to draw a variety of shapes. A user can switch back to the Object Selector Tool by pressing the spacebar or enter. Right clicking on the tool icons shows the variety of alternate shapes. One may draw rectangles, circles, arrows, polygons, lines, curves, stars, gears, triangles, blobs, and other shapes. 
Add Text Tool is used to draw a fragment of text. A user can right click on this tool for access to specialized versions of it. The tool may also be used to edit text.
The Quick Figure Tool creates a new figure from a multidimensional image. If an image is open in ImageJ, that image will be used to create a figure, otherwise the user will be asked to choose a file. New figures may either be split channel or contain only the merged image depending on what the user has set as the default template.
See other sections for details of specialized tools.
