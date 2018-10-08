# Ada
Some Ada exercices and snippets

## Compiling
The path of compilation is

    > gcc -c main_mine.adb
    > gcc -c greetings.adb

    > gnatbind main_mine
    > gnatlink main_mine
  
  If you wish to check the specs
  
    > gcc -c -gnatc greetings.ads
    
    
  ### *Much simpler
  
    > gnatmake main_mine.adb
      
 or
 
    > gnatmake my_file.adb -D directory_path -o exe_dir/my_file_with_the_name_i_want_executable
    
By default, the executable output of "main_mine.adb" is "main" ,
    
    > ./main
    

### *Notes on the 'main' procedure/program
In Ada, the main procedure does not need to be called 'main', any name can be given.



## with, use, renames

- A with clause makes the content of a package visible by selection,

        with Ada.Text_IO;
        ..
            Ada.Text_IO.Put_Line("Heelo World");
            
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
            
e
e
e
