## Execution Flow
Execution begins at `_start`, where `num1` (1000) is loaded into AX. `sub ax, [num2]` subtracts 2000, and the result is stored in `result` before the program exits.

## Arithmetic Operation
`sub` performs a 16-bit subtraction: 1000 − 2000 = −1000, stored as `0xFC18` in two's complement. The Carry Flag (borrow) and Sign Flag are set.

## Execution Observations
The program executed successfully using the 32-bit format without terminal output. AX and `result` hold `0xFC18`, showing how negative results are represented in two's complement.
