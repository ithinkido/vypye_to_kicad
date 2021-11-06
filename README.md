# vypye_to_kicad
Misusing vpype gcode to generate kicad_mod files  
This is a dirty hack, but i works ( with lots of caveats )  
1. you ***must*** use `splittall` when reading the file 
2. you will have to manualy edit the config.toml to fix the line width of the generated file. 
3. No chance of filled shaped here, just plain old lines  
4. orientaion is a bit wonky, but still usable

eg:

    vpype read '/cu_pour/merged.svg' splitall gwrite -p mod /cu_pour/merged_vpype.kicad_mod  

  
  
![image](https://user-images.githubusercontent.com/52834821/140616097-857c9ee6-5c70-42f9-9454-5c4733d0c9be.png)
