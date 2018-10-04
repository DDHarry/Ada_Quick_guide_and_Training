# Ada
Some Ada exercices and snippets

## Compiling
The path of compilation is

    > gcc -c main_mine.adb
    > gcc -c greetings.adb

and

    > gnatbind main_mine
    > gnatlink main_mine
  
  If you wish to check the specs
  
    > gcc -c -gnatc greetings.ads
    
    
  Much more simply
  
    > gnatmake main_mine.adb
      
 or
 
    > gnatmake my_file.adb -D directory_path -o exe_dir/my_file_executable
    
By default, the executable output of "main_mine.adb" is "main" ,
    
    > ./main
    
