## Execution Flow
Execution begins at `_start`, where `num1` (32000) is loaded into AX. `add ax, [num2]` adds 500, and the result is stored in `result` before the program exits.

## Arithmetic Operation
`add` performs a 16-bit addition: 32000 + 500 = 32500 (`0x7EF4`). The result fits within the signed 16-bit range, so no overflow occurs.

## Execution Observations
The program executed successfully using the 32-bit format without terminal output. AX and `result` hold `0x7EF4`. Using 16-bit registers allowed values too large for 8 bits.
