
This code is just a upgrade port of Ryan great work .. all credit to him ... original code located here..

http://www.arcgis.com/home/item.html?id=794b0a10e3b3413e9f3b7870acb9953f#

there are some issues with this code ... will accept pull request to sort out :p


Cheers
Coomsie


Description by Ryan of widget

=============================

This Drawing and Measurement widget provides users with the ability to annotate maps made in the ArcGIS Viewer for Flex (v2.4) with graphics and text.  It is a complete rewrite of the previous release (from the ground up) and at this stage should be considered BETA as not all planned functionality has been implimented at this stage. 

It contains functionality that extends that available in the standard Drawing widget that comes as part of the Viewer framework.  This widget allows users to interactively add graphic features to the map, including points, lines, polygons and text.  They can then manipulate the properties of the graphics (symbology colour and style, font size, transparency, etc.).  It utilises a template picker component similar to that used in the editor widget to allow the user to select the type of graphic they wish to produce. 

The widget features a graphic inspection list that provides the user with summaries of each drawn graphic (including area and length measurements, graphic text, etc).  When moving over the features in the list, the graphic is highlighted with animated halo effects (making it easy to distinguish it from other graphics in the list).  Individual graphics can be selected and removed from the inspection list.

This release of the widget has the following user functionality:

�      Users can interactively create a point, polyline, freehand line, polygon, freehand polygon, circle, ellipse or rectangle shapes with symbology and settings based on graphic templates. 

�      Drawn graphics are stored on the map in a self-contained graphics layer tied to the widget.  The user simply selects the template they wish create a graphic based on from the template picker, then start drawing on the map.

�      Users can change the current drawing tool being utilised by selecting a tool from the tool dropdown (if more than one drawing tool is available for the particular geometry type being created e.g. the circle, ellipse, rectangle, polygon, and freehand polygon tools are available when drawing a polygon graphic).

�      Users can interactively create and place text labels on the map, again based on graphic templates.

�      Users may add attributes to individual drawn graphics, including a title, some user defined text, and a hyperlink to a web location.  These details are displayed in a popup when the user clicks the graphic (similar to the search results in the standard ESRI search widget).  If the hyperlink path links to an image (a jpeg, png, or gif), this image will be displayed in the popup.

�      Users can define their own graphic templates, setting the default symbology including transparency used for graphic features, as well as defining the default tool used to create that feature (e.g. the freehand polyline tool)..

�      Users can modify the default graphic templates available for use with the Graphic Template editor.

�      The user�s graphic template settings are stored in a local storage object and are available to the user each time they start the widget (i.e. users preferences are available each time they use the widget on a specific machine).  These settings are updated each time the user makes a change to their template settings.  Users can reset these template settings to the configured default settings at any time.  

�      When constructing line and polygon graphics with the draw tools, interactive segment and total line length measurements are displayed as a mouse tip (these measurements are approximate only).

�      Users can snap a node to a node of another feature while drawing or modifying a feature by pressing down the Control key.  

�      Users can interactively move, scale, and rotate an existing graphic with the mouse by clicking and dragging it.

�      Users can edit the geometry of polyline and polygon graphics using interactive tools that become available when the graphics is clicked with the mouse.

�      Users can change the symbology properties of an existing graphic by double clicking on it with the mouse or right-clicking it and choosing the properties option from the popup menu.  The properties are changed in a popup dialog with properties appropriate for that graphic i.e. a point graphic will show a point symbology dialog.

�      Users can reshape line and polygon graphic boundaries using the reshape tool.  This tool functions by allowing the user to draw a line that defines the new section of the boundary.  This functionality utilises the Reshape Task of the geometry service (ArcGIS Server version 10).

�      Users can cut line and polygon graphics into multiple individual pieces utilising the cut tool.  This tool functions by allowing the user to draw a line that defines the line the will divide feature.  Each of the pieces retains the original graphic�s symbology and attribute settings.  This functionality utilises the Cut Task of the geometry service (ArcGIS Server version 10).

�      Users can merge two or more polygon graphics into a single graphic, the geometry merged into a single shape (or a multipart polygon) using the union task of the geometry service (ArcGIS Server version 10).  The new graphic retains the symbology and attribute settings of the first graphic selected. 

�      Users can select and highlight existing graphics.  They can do so automatically when clicking a graphic with the mouse (the clicked graphic is highlighted with glow sing the focus colour setting from the viewer configuration).  Multiple graphics can be selected if the user holds down the Control button while clicking individual features.  Clicking an existing selected feature while holding the Control key will remove that feature from the selection.  Clicking an open space on the map will clear the selected graphics (unless the Control key is held).

�      Users can change the default graphic selection mode by picking a selection method from the selection method dropdown.  The available selection methods are: New Selection (when unless the Control key is clicked, existing selections are replaced each time a new graphic is selected); Add To Selection (when the user no longer has to hold the Control key down to select additional graphics � clicking another graphic will append it to the existing selection); and Remove From Selection (when the user no longer has to hold the Control Key down to remove a graphic from the current selection � clicking a non-selected graphic in this mode will not add it to the current selection).

�      Users can review a list of the selected graphics and a list of all the graphics currently on the map.  The list contains summary details about the type and geometry properties of the graphic (length/perimeter/area/XY position/label text).  When the mouse pointer hovers over an item in the list, the associated graphic on the map is highlighted.  Users can remove a graphic by clicking the Delete icon on the item in the list for that graphic. 

�      Users can delete an existing graphic by right clicking on it (or right�clicking on the item in the graphics list) and choosing delete graphic from the popup menu, or by selecting it with the select tool and pushing the delete key.

�      Users can delete all graphics by clicking on the clear graphics button in the widget, or by right clicking a graphic and choosing the Delete All Graphics option.

�      Users can copy and paste an existing graphic by right clicking on it and choose copy graphic and then paste graphic from the popup menu, or by selecting it with the select tool and pushing the Control+C keys, then the Control+V keys.

�      Users can toggle functionality to display the measurements for a graphic (i.e. line length polygon area, point coordinates) when it is created.  These measurements are displayed as text graphics which position themselves based on the features geometry.  These labels will move if the base graphic is moves, and the contents will automatically update if the geometry is modified (i.e. the geometry is moved or reshaped).

�      Users can generate measurement labels for existing graphics by right clicking on the graphic and choosing the Show Measurements option.

�      The measurement units utilised can be set by the user from a list of pre-configured choices.

�      Users can toggle functionality to create multiple buffer regions around graphics as they are created.  The number of buffer regions, and the buffer distance can be set by the user prior the graphic being created.  The buffer distance can be chosen from a list of pre-configured buffer distances, or can be set to a custom distance determined by the user.

�      Users can save the graphics including font and symbology settings to a file for later reuse.  This includes any attribute settings, such as the title, content, hyperlink and whether the measurement label is displayed.

�      Users can import previously saved graphics files back into a map.The code attachment includes both the compiled version of the widget and the source code, as well as a configuration/deployment guide. 

The code attachment includes both the compiled version of the widget and the source code.  A configuration/deployment guide is currently being compiled and will be made available as soon as it is completed
