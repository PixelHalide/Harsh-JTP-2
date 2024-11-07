# Bit-O-Asm 1

We are given an assembly file this time:

```
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x4],edi
<+11>:    mov    QWORD PTR [rbp-0x10],rsi
<+15>:    mov    eax,0x30
<+20>:    pop    rbp
<+21>:    ret
```

We are told to find what is inside the eax register.

I don't know assembly, So I have to first know what an eax register is. It's apparently used for arithmetic, So it probably contains a number.

I also try to see what the words in the middle (push,mov,pop,ret) do.

push moves data into a data stack, and mov moves data from one place to another, pop deletes data from the stack, and ret returns.

Looking at the code, i see 0x30 being "moved" into eax. i assume that this is the number that we are looking for.

i convert 0x30 to decimal, which is 48 and write it into the flag. This is the correct answer.