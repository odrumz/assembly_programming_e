## Execution Flow
Execution begins at `_start`, where 100 and 200 are loaded into RAX and RBX. `push rax` and `push rbx` place these values onto the stack. The program then uses `pop rcx` and `pop rdx` to retrieve them in reverse order. Finally, the program exits using the 64-bit Linux system call.

## Stack Operations
`push rax` stores 100 and decreases RSP by 8 bytes. `push rbx` stores 200 and decreases RSP by another 8 bytes. `pop rcx` retrieves 200, increasing RSP by 8 bytes, while `pop rdx` retrieves 100 and increases RSP by another 8 bytes. RSP returns to its original position, demonstrating the LIFO principle.

## Execution Observations
The program executed successfully without terminal output. The values were retrieved in reverse order, confirming correct stack operation.