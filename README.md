# Assembly

## XMIG Install
Install XMING in windows

## Machine Id Setup
sudo systemd-machine-id-setup
sudo dbus-uuidgen — ensure
cat /etc/machine-id

## Basic Font Install
sudo apt -y install x11-apps xfonts-base xfonts-100dpi xfonts-75dpi xfonts-cyrillic

## Display setup for ddd application
  DISPAY=:0 ddd <program_to_debug> 

## Assembler YASM install
sudo apt install yasm

## YASM Design
 - [yasm flow understanding](https://www.tortall.net/projects/yasm/reference/design/design.pdf)

## DDD debugger install
sudo apt install ddd

## Assembling and linking
1. write asm program
   vi exit.asm 
   
2. assembly source code 
 
    yasm -f elf64 -g dwarf2 -l exit.lst exit.asm 
   
    -f elf64 : selects a 64 bit output format
    -g dwarf2 : selects the dwarf2 debugging format
    -l exit.lst : a listing file which shows the generated code in hexadecimal
 
    output file: exit.o
    

3. linking 
    
   3.1 a program with the _start function 
    ld -o exit exit.o 

   3.2 a program with the _main function
    gcc -o exit exit.o 
 
   3.3 if -fPIC error occurs, add -no-pie options
    gcc -o add add.o -no-pie  

   
## x86 register purpose
 - ax - accumulator for numeric operations
 - bx - base register (array access)
 - cx - counter register (string operations)
 - dx - data register
 - si - source index
 - di - destination index 
 - bp - base pointer (for function frames)
 - sp - stack pointer

## Lecture 
 - [서울대 Computer Architecture 2018](http://csl.snu.ac.kr/courses/4190.308/2018-2/)
   
  
 
