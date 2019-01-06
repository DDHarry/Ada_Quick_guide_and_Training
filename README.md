# Running and compiling in Ada

Let us consider main_mine.adb as our program. Then
```ada
gnatmake main_mine.adb
```
By default, the executable output of "main_mine.adb" is "main_mine".
Precising the paths,

```Ada
gnatmake main_mine.adb -D path_to_the_prog -o dir_for_executable/my_executable_file_with_the_name_i_want
```


### More about compilation

The path of compilation is
```Ada
gcc -c main_mine.adb
gcc -c greetings.adb
```
to bind them
```Ada
gnatbind main_mine
gnatlink main_mine
```
  
If you wish to check the specs
```ada  
gcc -c -gnatc greetings.ads
```

```Ada
with Ada.Text_IO;
use Ada.Text_IO;
begin
  int A = 2;
  end
  ```
  

    
  ### Much simpler
  
    > gnatmake main_mine.adb
      

    

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
