## Execution Flow
Execution begins at `_start`, where `num1` (0) is loaded into AX. `sub ax, [num2]` subtracts 1, then `sbb ax, 0` subtracts the borrow, and the result is stored in `result` before the program exits.

## Arithmetic Operation
`sub` computes 0 − 1 = `0xFFFF` and sets the Carry Flag. `sbb ax, 0` then computes AX − 0 − CF = `0xFFFF` − 1 = `0xFFFE`.

## Execution Observations
The program executed successfully using the 32-bit format without terminal output. AX and `result` hold `0xFFFE`. SBB uses the Carry Flag from the previous subtraction as a borrow.
