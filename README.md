# 1.Running and compiling in Ada

## 1.a. Compiling

Let us consider main_mine.adb as our program. Then
```bash
gnatmake main_mine.adb
```
By default, the executable output of "main_mine.adb" is "main_mine".
Precising the paths,

```shell
gnatmake main_mine.adb -D path_to_the_prog -o dir_for_executable/my_executable_file_with_the_name_i_want
```
## 1.b. Running
```Bash
./of_course
```



# 2. Anatomy of an Ada program

## 2.a. The program

The name of the program, cf. [ARM](link_here)



```Ada
with Ada.Text_IO;   use Ada.Text_IO;   -- the "with / use" clauses part


procedure anatomy_program is           -- Procedure, function, package's name must be the file's one
  val1 : float  := 11;                 -- Variables declaration
begin
  -- Some instructions                 -- the program's instructions
end anatomy_program
  ```


### Nota Bene
• On the 'main' procedure/program
In Ada, the main procedure does not need to be called 'main', any name can be given.

• To get the full picture, Ada is a high integrity programming language. Hence, along with the ```*.adb```, Ada Body package, ```anatomy_program.adb```, comes a second file, the ```Ada Specification package```, ```*.ads```, named
```Ada
anatonmy-program.ads
```
However, this does not prevent you to create single procedure or function files if needed, depending on your needs.


## 2.b. About *with, use, renames*

- A ```with``` clause makes the content of a package visible by selection,
```Ada
        with Ada.Text_IO;
        ..
            Ada.Text_IO.Put_Line("Hello, World");
 ```
            
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
For a better maintenance, improved readability, one is always suggested to use:
- ```use``` for the most 'obvious' packages (define obvious);
- ```renames``` for all other packages.


# 3. The *Hello World* program

```Ada
with Ada.Text_IO;
...
```


# 4. Help and References
-- Here!
