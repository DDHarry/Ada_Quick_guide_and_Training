# Some tips about Ada

## Conventions

• Ada is a case insensitive language

• Names for variables, functions, procedures or packages are free to choose, letters, " _ " or numbers. Should start with a letter

• " := " denotes assignment




## Reminder

### About the 'main' procedure/program

In Ada, the main procedure does not need to be called 'main', any name can be given.



### About *with, use, renames

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
            


### A most general rule

"use" for the most used packages (define them; Ada.Text_IO could be one of them);

"renames" for all other packages.
