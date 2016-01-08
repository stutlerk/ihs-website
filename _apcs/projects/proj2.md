---
layout: project
course: apcs

number: 2
title: PicEdit
due: 2016-01-21
turnin: #
forum: #

rubric:
  total: 30
  behavior:
    criteria:
      - criterion: grayscale() works correctly
        value: 3
      - criterion: invertColors() works correctly
        value: 3
      - criterion: changeContrastAndBrightness() works correctly
        value: 4
      - criterion: outline() works correctly
        value: 4
      - criterion: mirror() works correctly
        value: 4
      - criterion: pixelate() works correctly
        value: 5
    total: 23
  implementation:
    criteria:
      - criterion: methods return a new Picture; parameter is unaltered
        value: 2
      - criterion: methods are well-structured and helper methods are used to limit redundancy
        value: 2
      - criterion: Program is well-documented and uses good style
        value: 3
    total: 7
---
### Overview
Over the last decade or so, storage capacities available in computers (and on the Internet) has grown incredibly rapidly, driven primarily by the need to store digital media—music, images, and videos.  Even these days, when most other document files are only a few hundred kilobytes of data or less, images and music files are often several megabytes, and videos can reach into the gigabyte range.  (A gigabyte is 1024 megabytes and a megabyte is 1024 kilobytes.)  

Estimates indicate that there were over 100 billion photos on Facebook as far back as the summer of 2011, according to [http://mashable.com/2011/02/14/facebook-photo-infographic/](http://mashable.com/2011/02/14/facebook-photo-infographic/).  Due to the increased emphasis on digital media, programs that can manipulate that media in interesting ways have become very prominent.  In this project, we will implement a very simplified version of Photoshop, a popular image-editing application.

### Running the Program
For this project, you will not be implementing the main method to run the program.  Instead, you will implement a few utility methods that are called by a provided driver program.  (For reference, this is a very common way to work in the real world.  The people who write the code that runs the program are often different from the people who write the code to do the bulk of the work.)

To run the program, you will execute the main method of the PicEditMain class.  This program will first open a dialog box from which you can choose an image file to load.  It will then open the image and provide a number of controls to manipulate the image.  You can run the program before you have written any code to see the available options.  All of the buttons/sliders except for "Reset," "Open," and "Save" will utilize your code.

### Provided Code
You will be provided with _three_ code files for this part of the project, all of which are in [PicEdit.zip]({{site.baseurl}}\apcs\PicEdit.zip).  Of the three, **you should only edit PicEdit.java**— leave the other files untouched.  The provided files are:

| File Name | Description |
|---|---|
| PicEdit.java | The skeleton for a utility class which contains methods to manipulate images.  **This is the file in which you should implement the required methods.** |
| PicEditMain.java | The driver class for PicEdit, containing the client program. Run this class to test your code. |
| Picture.java | The Picture class, which provides an easy way to access images in several formats pixel by pixel. |

You should not have any need to modify or work with PicEditMain.java, other than to execute the program.  You should not modify Picture.java, but you will need to use some methods from this class in your program.  The methods you may need are:

| Method | Description |
|---|---|
| public Picture(int w, int h) | Constructor.  Creates a new empty Picture with width w and height h. |
| public Picture(java.awt.Color[][] colors) | Constructor.  Creates a new Picture with pixels as specified by the array. | 
| public Picture(Picture pic) | Constructor.  Creates a new Picture that is a copy of pic. |
| public java.awt.Color[][] getPixels() | Gets the array of pixels that make up this Picture. |
| public void setPixels(java.awt.Color[][] colors) | Sets the full set of pixels for this Picture. |
| public int height() | Returns the height of this Picture in pixels. |
| public int width() | Returns the width of this Picture in pixels. |

### Required Methods
For this project, you will implement six static methods to manipulate a Picture. For our purposes, an image is simply represented as a two-dimensional array of pixels, where each pixel has a color.  Pixels are represented using the java.awt.Color class— look this up in the Java API to see how it can be used.  Each pixel contains levels of the colors red, green, and blue which can be mixed to create all possible colors.  Each of the red, green, and blue levels is represented by an integer between 0 and 255 (inclusive).

You will implement your methods in a class called PicEdit, a skeleton for which has been provided to you.  The methods you must implement are:

| Method | Description |
|---|---|
| public static Picture grayscale(Picture p) | Returns a new Picture in which all pixels have been converted to shades of gray by setting the red, green, and blue levels to be the average of the previous levels.  For example, the color (128, 0, 55) would become (61, 61, 61) when converted to gray. |
| public static Picture invertColors(Picture p) | Returns a new Picture which contains exactly the same pixels as p but with each color inverted.  Two colors are considered inverses when their respective red, green, and blue values all add up to 255.  For example, the colors (128, 0, 55) and (127, 255, 200) are inverses. |
| public static Picture changeContrastAndBrightness(Picture p, double contrAmt, double brightAmt) | Returns a new picture in which the contrast and brightness have been altered according to the given parameters. Contrast and brightness are set using the formula c * (x - 128) + 128 + b, where x is the original color component, a is the contrast modifier, and b is the brightness modifier. The resulting values must be in the range [0, 255]. |
| public static Picture outline(Picture p, double threshold) | Runs "edge detection" on the argument to produce an outlined image.  All pixels in the returned Picture will be either black (if the "color distance" between the pixel and any neighbor is greater than the given threshold) or white (if the "color distance" between the pixel and all neighbors is less than or equal to the given threshold).  The "color distance" between to colors c1 and c2 is defined as the square root of:   (c1.red - c2.red)^2 + (c1.green - c2.green)^2 + (c1.blue - c2.blue)^2 |
| public static Picture mirror(Picture p, char dir) | Returns a new Picture which contains the same pixels as p but mirrored across either the vertical or horizontal axis.  The dir parameter indicates in which direction p should be reflected ('h' for horizontal, 'v' for vertical; case sensitive). |
| public static Picture pixelate(Picture p, int radius) | Returns a new Picture that is a pixelated version of p. Blocks of pixels with the given "box radius" should all be set to the average of all original pixels in the block. If the width or height of p is not a multiple of radius, use truncated boxes to cover the remainder. | 

### Testing
A compiled version of the project, with all extra credit features implemented, is available for download: [PicEdit.jar]({{site.baseurl}}\apcs\PicEdit.jar).  You may use this program to test your functionality by comparing the results.

You will be provided with a suite of unit tests to run against your program. Note that these tests are not exhaustive, so passing all the tests does not guarantee any particular grade.

### Extra Credit
You may earn extra credit by implementing additional features beyond those that are required.  Point values for extra credit features will be solely at my discretion and will be determined based on creativity and difficulty of implementation.  **No extra credit will be awarded for features that break required functionality, and points will still be lost for failing to meet requirements.**  It is HIGHLY recommended that you not attempt extra credit work until your project is fully complete.  Extra credit will be capped at 20% of the total project value.

Note that your extra credit work must not cause any of your unit tests to fail or otherwise cause the program functionality to change.  In other words, your extra credit features must not require the user to change their behavior to use the program properly-- you must simply add additional, optional features.

Additional method stubs are included in PicEdit.java as suggestions for extra credit. These methods are already connected to the driver GUI. See the header comments for each method for a description of what they are intended to do. If you would like to implement an extra credit feature other than those suggested, speak to Mr. Wortzman to add it to the GUI.  (Currently, the contrast/brightness sliders and the color scaling sliders do not work well together. You do not need to worry about making these work together if you choose to implement color scaling.)



  