# A# - CPU in Logicsim.
Central Processing Unit created in logicsim, using only basic logic gates and integrated circuits (Created by me).

This CPU is extremally optimised for using a low quantity of clocks circles per operation, Mostly using 1 clock per operation. 

Making possible running interessing programs at 4.1 KMz.


![Screenshot](https://i.postimg.cc/bNXQj4TP/Captura-de-Tela-2017-10-12-as-21-26-43.png)

Inner view.

![Screenshot](https://i.postimg.cc/nrmSh7gh/Captura-de-Tela-2017-10-12-as-21-22-34.png)

Circuits and CPU created in 2015. (I just passed it to github for public domain).

# Documentation CPU instructions
All instructions are created by myself.
Here is the list (not complete).
| Operation| Binary | HEX |
| :---: | :---: | :---: |
| INIT AX| 00000000 | 00 |
| IN AX| 00110001 | 31 |
| OUT AX| 00110010 | 32 |
| MOV AX, BX| 00000001 | 01 |
| MOV AX, CX| 00000010 | 02 |
| MOV BX, AX| 00000101 | 05 |
| MOV CX, AX| 00000110 | 06 |
| MOV AX, {RAM}| 00000100 | 04 |
| ADD AX, BX| 00001101 | 0D |
| ADD AX, CX| 00001110 | 0E |
| SUB AX, BX| 00010001 | 11 |
| SUB AX, CX| 00010010 | 12 |
| JNO| 01001010 | 4A |
| PUSH AX| 10000000 | 80 |
| PUSH BX| 1000001 | 81 |
| PUSH CX| 10000010 | 82 |
| POP AX| 10010000 | 90 |
| POP BX| 10010001 | 91 |
| POP CX| 10010010 | 92 |
| OR AX,BX | 00011001 | 19 |
| OR AX,CX | 00011110 | 1E |
| NOT AX | 00010100 | 14 |
| INC AX | 00001100 | 0C |
| DEC AX | 00010000 | 10 |

Is possible to make CALLS and MOV {RAM}, AX, Conditional or incoditional JUMPS etc... 

But i dont remember instructions anymore (I will analise later.)

# Sinus Wave Code Demonstration
Hexadecimal program loaded.
```
00 00 00 05 01 00 04 ff
00 00 00 05 11 00 04 ff
05 11 00 04 ff 05 21 00
04 ff 05 21 00 04 ff 05
41 00 04 ff 05 41 00 04
ff 05 21 00 04 ff 00 05
21 00 04 ff 05 11 00 04
ff 05 11 00 04 ff 00 00
00 27 08
```
Video demonstration 
[Watch the video](https://www.youtube.com/watch?v=P-vK3BA1kco&feature=youtu.be)

# Interessing ideas for new CPUs.
I could implement alot of things to make this have a even better clock performance.
1. Having a SPECIAL register thats defines block of memory for actuation, decreasing the amount of information for JMP instruction.
2. Duplicate BUS, to enter two instructions at a time with two loaded ROM units and create a unit that defines whether two instructions can be executed simultaneously,
like (PUSH CX, INC AX) or even (MOV AX, CX and MOV AX, BX) having 2x better performance and 2 intructions per 1 clock.  
