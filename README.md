# Ada
Some Ada exercices and snippets

                ===> Write the Basic stuff here!

## COMPILING
The path of compilation is

    > gcc -c main_mine.adb
    > gcc -c greetings.adb

    > gnatbind main_mine
    > gnatlink main_mine
  
  If you wish to check the specs
  
    > gcc -c -gnatc greetings.ads
    
    
  ### Much simpler
  
    > gnatmake main_mine.adb
      
 or
 
    > gnatmake my_file.adb -D directory_path -o exe_dir/my_executable_file_with_the_name_i_want
    
By default, the executable output of "main_mine.adb" is "main_mine" ,
    
    > ./main_mine
    

### Notes on the 'main' procedure/program
In Ada, the main procedure does not need to be called 'main', any name can be given.



## WITH, USE, RENAMES

- A with clause makes the content of a package visible by selection,

        with Ada.Text_IO;
        ..
            Ada.Text_IO.Put_Line("Hello, World");
            
- A 'use' clause makes all the content of a package directly visible. Less typing and less readability.

        with Ada.Text_IO;
        use Ada.Text_IO;
        ..
        Put_Line("Hello_World");
    

- By renaming, we get a shorter alias to any package name

        with Ada.Text_IO;
        
        procedure ..
            package IO renames Ada.Text_IO;
        begin
            IO.Put_Line("Hello, renames");
            


### General rule
"use" for the most used packages (define them);

"renames" for all other packages.

e
e
e
