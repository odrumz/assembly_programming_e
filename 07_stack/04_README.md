### Output


(no terminal output)

The program executes successfully without displaying anything on the terminal.

Explanation:
The program demonstrates 32-bit stack frame management. It calls a function named work, saves the previous base pointer and reserves 8 bytes of stack memory for two local variables (100 and 200). These values are retrieved into EAX and EBX respectively. The stack frame is then cleaned up and the function returns to the main program.

The program terminates successfully using the 32-bit Linux system call `int 0x80` with exit status 0.