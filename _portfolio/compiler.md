---
title: "test"
created: March 2020
collections: portfolio
order: 1030
---

I created an x86-64 compiler for a Pascal-like language, which has static types. The language itself is not feature rich, but it supports mathematical expressions, reading user
input, writing to the console/terminal, arrays, and record types, which are user-defined container types like structs. 

The compiler also performs some optimizations including:
- Constant folding
- Constant propagation
- Register allocation with spills and restores
- Usage of %rsp register instead of %rbp for accessing or writing to variables stored on the stack
- Modulus using AND for powers of two
- Intermediate representation specific optimizations

The compiler uses a single-static assignment (SSA) intermediate representation. After the SSA is generated, it goes through the instruction selection phase, which selects 
suitable x86-64 instructions for the SSA instructions. Next, the x86-64 instructions go through register allocation, which allocates machine registers for the operands, and after that,
the x86-64 assembly is completed.

Here is an example program:
`PROGRAM program :
  VAR x : INTEGER;
BEGIN
  READ x;
  WRITE x;
END.
`
The program above reads an integer from user input and writes it to the terminal/console. The program can be compiled using `./compiler -o program.txt` and the result is:
`.section .rodata
 s_readint_fmt : .string "%ld"
 s_writeint_fmt : .string "%ld\n"
 .section .text
 .global main
main:
        push %rbp
        subq $8, %rsp               
        leaq 0(%rsp), %rsi          
        movq $s_readint_fmt, %rdi   
        subq $8, %rsp
        call scanf
        addq $8, %rsp
        movq 0(%rsp), %rsi          
        movq $s_writeint_fmt, %rdi  
        subq $8, %rsp
        call printf
        addq $8, %rsp
        addq $8, %rsp               
        pop %rbp
        movq $0, %rax
        ret`
        
Note that the variable is being stored on the stack. It currently takes 16 instructions although some of them are boiler plate instructions. In the future, local value numbering
could be used to cut down on the code size.
