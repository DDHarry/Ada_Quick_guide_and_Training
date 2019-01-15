

## 1.c. More about compilation

The path of compilation is
```shell
gcc -c main_mine.adb
gcc -c greetings.adb
```
to bind them
```shell
gnatbind main_mine
gnatlink main_mine
```
  
If you wish to check the specs
```shell
gcc -c -gnatc greetings.ads
```
