## Execution Flow
Execution begins at `_start`, where the dividend 50000 is loaded into AX, 0 into DX, and the divisor 300 into BX. `div bx` divides DX:AX by BX before the program exits.

## Arithmetic Operation
`div bx` performs 16-bit unsigned division: 50000 / 300. The quotient 166 is stored in AX and the remainder 200 in DX.

## Execution Observations
The program executed successfully using the 32-bit format without terminal output. AX = 166 and DX = 200. DX must be cleared before division since it forms the high part of the dividend.
