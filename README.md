# gba2bmp
A tool to construct BMP files from a GBA tileset. The tool can reads a user specified file containing indexes to arbitrarily construct any order of tiles with any image size. In addition, the tool conserves the index based color of the original tileset.

# Usage
This is a command line utility soooooo

-b : bitmap file
-B : bytes, interpret gba data as 8bit indexes
-h : help, displays this message
-m : map file
-r : reverse, convert from bmp to gba data
-t : gba tileset data file

example 1
---------
gba2bmp -t tileset.dat -m map.txt -b out.bmp

This will construct a bitmap image using indexed colors. Using a \"map\" file,
which are indexes to the tiles within the gba data file, will place those tiles
in any arbitrary order. This is useful when the tiles are scattered throughout

example 2
---------
gba2bmp -r -b in.bmp -m map.txt -t tileset.dat

After editing the bmp file, we can update the tileset by running the conversion
in reverse.

# Building
Grab the source and you can build the tool using Pelles C for windows. just open the gba2bmp.ppj file within and build gba2bmp.exe :)

All credit to Stickteo for making this. I am just finishing a fan translation and found his tool but found it had no build or instructions.
