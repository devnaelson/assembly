```
General registers
EAX EBX ECX EDX

Segment registers
CS DS ES FS GS SS

Index and pointers
ESI EDI EBP EIP ESP

Indicator
EFLAGS
```

General registers
As the title says, general register are the one we use most of the time Most of the instructions perform on these registers. They all can be broken down into 16 and 8 bit registers.<br>

```
32 bits :  EAX EBX ECX EDX
16 bits : AX BX CX DX
 8 bits : AH AL BH BL CH CL DH DL
```

##### EAX,AX,AH,AL : Called the Accumulator register
- It is used for I/O port access, arithmetic, interrupt calls,
##### EBX,BX,BH,BL : Called the Base register
- It is used as a base pointer for memory access Gets some interrupt return values,
##### ECX,CX,CH,CL : Called the Counter register
- It is used as a loop counter and for shifts Gets some interrupt values.
##### EDX,DX,DH,DL : Called the Data register
- It is used for I/O port access, arithmetic, some interrupt calls.


###### segment registers or Memory Segmentation in 8086 Microprocessor

```
Segmentation is the process in which the main memory of the computer is logically divided into different segments and each segment has its own base address. It is basically used to enhance the speed of execution of the computer system, so that the processor is able to fetch and execute the data from the memory easily and fast.
```

##### Code segment register (CS): 
- is used for addressing memory location in the code segment of the memory, where the executable program is stored.
##### Data segment register (DS): 
- points to the data segment of the memory where the data is stored.
##### Extra Segment Register (ES): 
- also refers to a segment in the memory which is another data segment in the memory.
##### Stack Segment Register (SS): 
- is used for addressing stack segment of the memory. The stack segment is that segment of memory which is used to store stack data.

![MySQL](https://qph.fs.quoracdn.net/main-qimg-8d059228ebba03bd803df7fa9b420be3)
![MySQL](https://qph.fs.quoracdn.net/main-qimg-393f9b74e7266dab96e3a6be84284dac-pjlq)


##### Indexes and pointers

```
Indexes and pointer and the offset part of and address. They have various uses but each register has a specific function. They some time used with a segment register to point to far address (in a 1Mb range). The register with an "E" prefix can only be used in protected mode.

ES:EDI EDI DI : Destination index register
                Used for string, memory array copying and setting and
                for far pointer addressing with ES

DS:ESI EDI SI : Source index register
                Used for string and memory array copying

SS:EBP EBP BP : Stack Base pointer register
                Holds the base address of the stack
                
SS:ESP ESP SP : Stack pointer register
                Holds the top address of the stack

CS:EIP EIP IP : Index Pointer
                Holds the offset of the next instruction
                It can only be read 

```