# Glyph Image Maker
This photoshop script will generate an image file for each glyph at a certain size, color, font and will name the image file according to the glyph name. For instance, the glyph A will be named A.png. The collection of glyph images can then be used in your favourite spritesheet generation tool (e.g. Texture Packer).

Forked from:
https://graphicdesign.stackexchange.com/questions/737/how-do-i-break-apart-text-in-photoshop
https://gist.github.com/davestewart/4529727

# Instructions for use with Texture Packer:
1) modify variables at top of the script to your specifications
2) open photoshop and create a new PSD file with the canvas big enough to hold all your glyphs. This script will output the glpyhs as one long single line on the canvas. The background should be set to transparent
3) in photoshop go to in menu file/scripts/browse and select this script
4) when the dialog opens up - set following settings:
- Select destination folder
- File type: PNG-24 (so it supports transparency)
- Transparency: true
- Trim Layers: true
- All other options: false
5) click ok and the glyph images will be produced and named after each glyph. For instance the letter a will be saved as a.png. NOTE that if you require upper and lower case glyphs then you need to process them in seperate batches as a.png and A.png cannot be put in the same folder in windows or MacOS.
6) Copy all glyph images into game project folder /lib/glyphs. If you have upper and lowercase copy them into /lib/glyphs/upper and /lib/glyphs/lower accordingly
7) open texture packer and drag all glyph images into root - do not use a smart folder as the name of the glyph cannot have any prepended folder names on it in the json file. For instance, the glyph for A must have an animation name A and not glyphs/A
8) The glyph images will be horizontally trimmed but not vertically. This is so a pivot point can be set for all glyphs that is consistent in Texture Packer.  Select all glyph images and adjust pivot point to be top left and then moved down close to top of the glyphs
9) publish the spritesheet/json
