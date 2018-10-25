# TWFCS-Shape-GUI-Generator
## Introduction ##
  My name is Kyle Langley and this is code and a README file uploaded for my Technical Writing for Computer Science class. This code originally is created for my Computer Programming II class. This code was created in four different versions. While the final build is uploaded, the other builds/versions are discussed to document how the whole program was created step by step.

### Examples ###
When the final build of this project is run, the code should produce a new window with completely randomly generated shapes drawn onto it. The Java executable is provided with this repository as well as the code. Here is one example of what the final product when ran looks like.

![project final examples 1](https://user-images.githubusercontent.com/44346659/47449427-35076000-d788-11e8-8b49-f068403d06a8.PNG)


### Compiler? ###

This project was made in netbeans. Since the files are included in text documents however, you should be able to copy the included files into any java compiler/IDE and it should run appropriately. 

If you would like to use netbeans and don't have it downloaded, here is a link to the download page:

https://netbeans.org/downloads/index.html

Netbeans EE download should suffice just fine.

To run this, you will also need to download Java if you don't already. Just download appropriate jdk file for your system, netbeans will need this upon loading up.

https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html


## Project Summary ##
This project was created for a midterm-like assignment in my Computer Programming II class. This project was created in the “Netbeans” IDE, although this should not be necessary to run the project. The java executable should run the program just fine. The ultimate goal of this project is to create a GUI which creates 30 (or more) random shapes and draw them on a 2D plane layered by a 3rd point representing a 3D plane. To create this, four different implementation and versions were made in order to ensure that the program ran smoothly and effectively.

#### First Iteration ####
  The first version of this project created was exclusively made to iterate the shapes used in the project and create a toString method so that they would print effectively. The three shapes created in this project are rectangles, circles, and triangles. Rectangle takes two variables; a length and a width value so that an area method can be added to multiply the two to effectively create a rectangle. The circle class takes one variable which is the radius of the circle. Using this, the first version creates an area class and a circumference (taken out before 2nd version is made). The triangle class takes two variables like the rectangle but these two are the base and the height. This class also creates an area for the triangles (L*W/2).
  
#### Second Iteration ####
  The 2nd version of this project creates a Point class and adds an X-coordinate and a Y-coordinate to the constructors of each shape. This point class is created and initialized by a center variable located in each shape’s class so that the x and y coordinates can be used to create a center for each shape on a two dimensional plane. The point class takes these two coordinates and checks them both to ensure that they are above the value of zero and below the value of five-hundred. These two are checked now so that when the final version is made, the shapes generated are ensured to fit inside the designated GUI size and don't go out of bounds. In the final version, when a GUI is made, calculations must be made so that the shapes actually do center on the defined point, because the GUI window creates the shapes coming from the center point, not around it.
  
#### Third Iteration ####
  The 3rd version of this adds in a third point to the constructors of these shapes. This point is used in the final version to layer the shapes on the two-dimensional plane so that they build up from bottom to top. This version also introduced the abstract shape class which joins all of the classes together. This also introduces an arraylist that can be used to store shapes later on.
  
#### Final Iteration ####
  The 4th and final version of this program introduces the GUI so that the the shapes can actually be printed to the screen. This GUI work and introduction is created in the main. Also created in the Lab5D class, a random shape generator is created so that thirty different shapes can be created and added to the arraylist. This class also introduces the ability to take each shape out of the arraylist and layer them depending on their z-coordinate. After determining what shapes are lowest to highest, the shape taken out of the arraylist is determined to be a circle, a rectangle, or a triangle and does calculations to determine where the shape should actually be held on the GUI. These calculations are done to shift the shapes to where the center is actually in the center of the GUI. After these calculations are done, the shapes are colored and printed to the GUI one at a time randomly. Along with the shapes, the areas of each shape are also printed to the screen (the numbers used for these calculations are also randomized by a random number generator).
