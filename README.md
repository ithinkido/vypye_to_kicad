# vypye_to_kicad
Misusing vpype gcode to generate kicad_mod files  
This is a dirty hack, but works ( with lots of caveats )  
1. you ***must*** use `splittall` when reading the file 
2. Seperate line widths into different layers. 
3. No chance of filled shapes here, just plain old lines  
4. Make sure ALL layers have line width defined in **mm**

eg:

    vpype read input.svg forlayer translate -l %_lid% "%lprop.pen_width_mm = lprop.vp_pen_width/mm; 0%" 0 end splitall gwrite -p mod test.kicad_mod  

 The prop substitution is used to fix the line width that is ALAWYA saved as px value when you actualy need a mm value 
  
![image](https://user-images.githubusercontent.com/52834821/140616097-857c9ee6-5c70-42f9-9454-5c4733d0c9be.png)
