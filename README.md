Conversion of a 32 bit colored ICO image to 8 bit grayscale BMP image
====================================================================

COMPILATION:
-------------

- Put the 32bit ICO in the folder
- Open the folder in the terminal
- Use make command to compile the code and run ./output
- Converted image will appear in the same folder as the source file

Note:
---------

- Make sure to change the source image name in the program before compilation.
- If the filename specified in the folder does not match the the specified in the program, the program ouputs Image not found and ends.
- Some other conditions like if the image is not 32 bit will also shut down the program.(These can be found in the code but I've hardly found any 32bit ICO images online that break the said conditions).
- There is no single thing in an ICO image that confirms whether it is ICO or not so the program might behave erratically if the source file is bmp(an example) instead of shutting down. Though I've put some conditions to check the format, they might not always work.
