## Execution Flow
Execution begins at `_start`, where `num1` (3000) is loaded into AX. `mul word [num2]` multiplies AX by 200. AX is stored in the low half of `result` and DX in the high half before the program exits.

## Arithmetic Operation
`mul` performs 16-bit unsigned multiplication: 3000 × 200 = 600000 (`0x927C0`). The product is split across DX:AX, with DX = `0x0009` and AX = `0x27C0`. Since DX is non-zero, the Carry and Overflow Flags are set.

## Execution Observations
The program executed successfully using the 32-bit format without terminal output. `result` holds `0x000927C0`. A 16-bit multiply produces a 32-bit result in DX:AX.
