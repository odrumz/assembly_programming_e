## Execution Flow
Execution begins at `_start`, where the dividend 300000000 is loaded into EAX, 0 into EDX, and the divisor 1000 into EBX. `div ebx` divides EDX:EAX by EBX before the program exits.

## Arithmetic Operation
`div ebx` performs 32-bit unsigned division: 300000000 / 1000. The quotient 300000 is stored in EAX and the remainder 0 in EDX.

## Execution Observations
The program executed successfully using the 32-bit format without terminal output. EAX = 300000 and EDX = 0, showing an exact division with 32-bit registers.
