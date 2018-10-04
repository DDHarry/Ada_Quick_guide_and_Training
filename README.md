# Ada
Some Ada exercices and snippets

## Compiling
The path of compilation is
    gcc -c main.adb
    gcc -c greetings.adb
    > gnatbind main
    > gnatlink main
  
  If you wish to check the specs
    gcc -c -gnatc greetings.ads
    
  Much more simply
  
      gnatmake main.adb
      
 or
 
    gnatmake my_file.adb -D directory_path -o exe_file
    
By default, the executable output is "main" ,
    
    ./main
    
