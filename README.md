# Digital Standard Cell Characterizer (DSCC)  

This tool generates characterization data from the layout of the cell.  
The tool currently support combinational cells.

## How to use 
You just need to load the magic file of the cell layout `thesis_aoi211.mag`, the path where Sky130 PDK was installed, the output load in picofarads [pF] and the transition times in nanoseconds [ns] to characterize the cell.

~~~
python3 dscc.py thesis_aoi211.mag --sky130-root="/home/nelson/cad" --output-loads="0.05, 0.1" --slew-rates="0.1, 0.2"
~~~

The output is the characterization data in `.lib` format. 
