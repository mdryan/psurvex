When I first came to China we had no laptops for processing survey data in the field, relying instead on a Psion palmtop. Our early program required us to enter the data in the body of the code, and we also had to do a lot of work manually putting the stations in the correct order for processing. Apart from not being especially user friendly, this meant that it took nearly as long to convert it to the Survex file format when we got back to base as it had done to enter the data in the first place. My task therefore was to write a new program which could read the data from an external file, ideally one which resembled a .svx file as much as possible.

This program is the result, it supports only a subset of the .svx file format but the same file should process in Survex without any problems. You need to write a .svx file and save it somewhere on your machine. This program will then process the file and create a second file containing a list of points for plotting on graph paper and some statistics about your survey.
Limitations

The major lack of support in dealing with .svx files is for redefining characters (**set) and for different data styles (**data). It was written in the field without reference to the Survex sources (or even manual) so there might well be a couple of inconsistencies - check that **calibrate and**flags affect all the bits of survey that you were expecting them to and nothing else.

The program does not distribue loop closure errors around the loop as Survex does, and the output files are in a different format to those produced by Survex.

## Testing and Hardware Support ##
Although we don't use the program ourselves any more, it was given quite a bit of hammer in it's time and processed tens of kilometers of data without too much trouble. In particular it supports fairly large surveys by way of manually managing memory.

Because of the different memory architectures of the Series 3 and 5 it will only run on the later machines - but someone who knows what they are doing ought to be able to convert it fairly quickly.

I've also had a report that it will run on a Revo once the screen co-ordinates are modified.

## Future Development ##
As a result of hmg adopting laptop for data processing and all our Psions now either broken or stolen we no longer use the program, nor do we even have the means to test it these days. If anyone else wants to modify it or has any questions about how it works (or how to use it for that matter) feel free to get in touch.

## License ##
In the absense of any better ideas, this program is released under the GNU General Public License - the same as Survex itself. The program is free of charge, and you can modify it as you wish - but if you give or sell a copy to anyone else, modified or otherwise, then you must make sure they have access to the source code and that they are free to modify it and redistribute it as well. Pointing them at this webpage would probably be a good idea too.

## Download ##
The source code is available here. You will need both the implementation file and the header file. Things you might need to change to get the program to run properly appear near the top of the header file. If you have never used Survex before then you will need to become familiar with the .svx file format as well. You will probably find a plain text editor useful if you don't already have one, otherwise some of the Psion apps can also export to plain text.

## Links ##
[The Survex Project](http://www.survex.com)
[Hong Meigui CES](http://www.hongmeigui.net)
[Matt Ryan](http://www.mdryan.net)

Matt Ryan, April 3rd 2004