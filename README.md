# Digital Standard Cell Characterizer (DSCC)  

## [Slides](https://docs.google.com/presentation/d/e/2PACX-1vSiSyyyWhbehkQ2xNrCZK2VOh_s4KmKSZHU7BYJNZw7zeUBU8BMkgzOVHIq0tX81F9O7TQF6yfjhio4/embed?start=true&loop=true&delayms=3000")

### In these slides you could find an explanation on how the tool was developed, the algorithms to characterize the cells and to identify the logical function of them. This tool was developed to be used in the main proyect of [Open-Source Standard Cell Design Methodology](https://github.com/ledzeg/stdcell-methodology) 
<br>
<div style="text-align: center"><b>👇🏼 Click on the image to watch the slides</b></div>
<br>
<div style="text-align: center"><a href="https://docs.google.com/presentation/d/e/2PACX-1vSiSyyyWhbehkQ2xNrCZK2VOh_s4KmKSZHU7BYJNZw7zeUBU8BMkgzOVHIq0tX81F9O7TQF6yfjhio4/embed?start=true&loop=true&delayms=3000"><img src="slides_cover.png" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></a></div>

This tool generates characterization data from the layout of the cell.  
The tool currently support combinational cells.

## How to use 
You just need to load the magic file of the cell layout `thesis_aoi211.mag`, the path where Sky130 PDK was installed, the output load in picofarads [pF] and the transition times in nanoseconds [ns] to characterize the cell.

~~~
python3 dscc.py thesis_aoi211.mag --sky130-root="/home/nelson/cad" --output-loads="0.05, 0.1" --slew-rates="0.1, 0.2"
~~~

The output is the characterization data in `.lib` format. 
