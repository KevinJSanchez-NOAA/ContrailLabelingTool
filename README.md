# contrail_labeling_tool
## Description
A point-and-click tool to label contrails on satellite images using click, key and scroll events.
The repository includes 5 example granules (data from 5 satellite images). The mask begins labeled by a dated detection method instead of starting from scratch.

### Click events
Mouse left click:
    A mouse left click on the plotted image (mask or satellite image) will add a point to a list of points that 
    are used to form a polygon. The point will appear on the image and lines will be drawn between each point in order. 
    Note: mouse clicks must be performed in order (i.e. in a clockwise or counter-clock wise order).
    
Mouse right click:
    Holding left click and moving the mose will drag the image until the click is released.

### Scroll events
Mouse scroll:
    Scrolling the mouse will zoom in and out.

### Key events
! (shift+1): 
    Remove the last point added with a click event.
    
a:
    Add positive labeled points with the polygon (i.e. label points in polygon as contrail on the mask)
    
d:
    Delete positive labeled points with the polygon (i.e. label points in polygon as not a contrail on the mask)
    
u:
    Undo the last label action (the 'a' or 'd' key events). Points from the click event, for the polygon, are reploted.
    
`:
    Toggle between the satellite image and the mask. The polygon from click events will remain.
    starting from the top right corner.
    
C (shift+c):
    Close the figure, save the updated mask (as a png and '.contrail-mask' data file) and end the program execution. 
    When rerunning the code, if an updated mask already exists, a text prompt will ask if you wish to overwrite or 
    load the existing updated mask.
