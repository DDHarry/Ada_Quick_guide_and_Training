# Title

## Ada cheat sheet

• Ada is a case insensitive language

• Names for variables, functions, procedures or packages are free to choose, letters, " _ " or numbers. Should start with a letter

• " := " denotes assignment


### Attributes, apostrophes, tick

• Integer'First : to get the minimum value of the type integer. Here, the apostrophe, tick, single quote symbol denotes an attribute

• Natural'Image(Natural'Last) : thee 'Image attribute turns an input natural into a string



### Ada types
• Integer, Positive, Natural, Long_Integer, Long_Long_Integer ...

• For portability choice, the Positive and Natural range are not related to the underlying computer architecture

• Float'Image : convert the float into a string :
'''Ada
Ada_Text_IO.Put_Line("The min range of a float: " & Float'Image(Float'First)");
'''
 
• Ada_Text_IO.Put(Total
