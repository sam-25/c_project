                                                                   C - PROJECT
                                                                    GROUP 12

                                      Conversion of a 32 bit colored ICO image to 8 bit grayscale BMP image


COMPILATION:

-Put the 32bit ICO in the folder
-Open the folder in the terminal
-Use make command to compile the code and run ./output
-Converted image will appear in the same folder as the source file

Note:
-Make sure to change the source image name in the program before compilation.
-If the filename specified in the folder does not match the the specified in the program, the program ouputs Image not found and ends.
-Some other conditions like if the image is not 32 bit will also shut down the program.(These can be found in the code but I've hardly found any
 32bit ICO images online that break the said conditions).
-There is no single thing in an ICO image that confirms whether it is ICO or not so the program might behave erratically if the source file is bmp(an example)
 instead of shutting down. Though I've put some conditions to check the format, they might not always work.


GROUP MEMBERS:

(a)IMT2020010 Vanshvardhan Singh: 1.Understand the source format and the destination format and then define appropriate date structures.
                                  2.Explained everyone the formats and algorithm to build the project on.

(b)IMT2020114 Puram Rahul Kumar Reddy: Read the source file and populate the data structure.

(c)IMT2020507 Asmita Zjigyasu: Code for writing the conversion between formats.

(d)IMT2020534 B Sathiya Naraayanan: Code for writing the conversion between formats.

(e)IMT2020062 Gattu Samarth: Code for writing the conversion between formats.

(f)IMT2020106 Chandra Karthik Deshineni: Use data in the destination data structure format and create destination image.


ABOUT THE CODE:

1. Read the header information of the ico file using its infoheader, its header and bmpinfoheader as defined earlier from the source image. 
2. Assign a color palette for the destination BMP image. Since it is going to have 256 different levels of color(from black to white),we assign 
   an array of size 1024, with all original terms 0. Assign the colors to the palette (0 0 0 0, 1 1 1 0, 2 2 2 0...), 0 0 0 0 = black and
   255 255 255 0 = white. 
3. Extract the values of blue, green and red from the source image from each pixel and use a formula for calculating the value of the 
   grayscale variable for the destination image using the previous color values. Assign the grayscale value to the pixels of the destination image.
4. Write the necessary information (i.e. the BMPINFOHEADER, BMPHEADER, new color palette, pixel size, padding correction etc.) to the
   destination file.

RESOURCES:

1. http://paulbourke.net/dataformats/bitmaps/
2. https://medium.com/sysf/bits-to-bitmaps-a-simple-walkthrough-of-bmp-image-format-765dc6857393
3. http://www.retroarchive.org/swag/WIN-OS2/0058.PAS.html
4. https://engineering.purdue.edu/ece264/16au/hw/HW13
5. https://www.daubnet.com/en/file-format-ico
6. Wikipedia pages for both the image formats
7. Countless Stackoverflow threads
