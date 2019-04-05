FreeImageDraw README

There are a few elements included in the project:


Steps to get the drawing working:
1. Create a .png image in your favorite image editor (I simply used MS Paint)
2. Drop the new image into your project (preferably in the Assets/Resources folder)
3. select the image in the Assets folder and apply the following settings:
* Set "Texture Type" to "Sprite (2D and UI)"
* Set the "Pivot" to "BottomLeft"
* Check the box for "Read/Write Enable" 
* Set the "Compression" dropdown to "None"
* Hit "Apply"
3. Create an image in the scene (right click in scene heirarchy>UI>Image)
4. Set the Image's "Source Image" to be the image you just created (you can drop and drop from the assets folder)
5. Attach the "DrawViewController" script to the newly created Image
6. Hit play, and left click to draw
7. To undo/redo in the editor use "shift+z/shift+y" respectively. If you are testing this in a built version use "control+z/control+shift+Z"

# Troubleshooting:
## Image settings:
* check that the image you are using has "Texture Type" set to "Sprite (2D and UI)", and make sure you hit "Apply"
* check that the image you are using has the "Pivot" dropdown set to "BottomLeft", and make sure you hit "Apply"
* check that the image you are using has "Read/Write Enable" checked, and make sure you hit "Apply"
* check that the image you are using has the "Compression" dropdown set to "None", and make sure you hit "Apply"

## Runtime issues:
* if you change the image at runtime, make sure you call the Initialize() method
* make sure the RectTransform the image is attached to has a pivot of (0,0)
