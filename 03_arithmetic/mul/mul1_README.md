## Execution Flow
Execution begins at `_start`, where `num1` (25) is loaded into AL. `mul byte [num2]` multiplies AL by 10, and AX is stored in `result` before the program exits.

## Arithmetic Operation
`mul` performs 8-bit unsigned multiplication: 25 × 10 = 250 (`0xFA`). The product is stored in AX. Since AH is 0, the Carry and Overflow Flags are cleared.

## Execution Observations
The program executed successfully using the 32-bit format without terminal output. AX and `result` hold `0xFA`. An 8-bit multiply produces a 16-bit result.
