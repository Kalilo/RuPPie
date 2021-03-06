# RuPPie
A templating engine for C++ classes powered by Ruby.

## Basic Usage
* git clone this repository to the working directory of your C++ project.
* Register your class files according to the example given in "classes/classfiles.xml"
* Define your classes in the style defined by "classes/example.xml" 
* run 'ruby ClassGenerator.rb'

## Notes
This generator was coded using ruby version 2.0.0. 

The TC.cpp and TC.hpp are template files which the script uses to discern the layout of the file. Modify this to change the layout of the resultant cpp and hpp files. 

The script determines where to place the necessary code by way for looking for xml like tags such as '\<classname\>'. Some tags like '\<classname\>' and '\<args\>' only replace the tag while leaving the other text on the line, while tags such as '\<methods\>' will remove the line it was matched on and replace it with the methods stipulated during the prompts.

## To Do
* Templates
* Interfaces
* Adaptors
* Use yml instead of XML for class definition.
* Automatically detect class files.
* Custom constructor definitions
* Better code to handle absolute pathing so that the class generator can be run from anywhere, including makefiles
