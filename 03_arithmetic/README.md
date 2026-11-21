# 03_arithmetic examples

Build/run (32-bit): `nasm -f elf32 file.asm -o file.o && ld -m elf_i386 file.o -o file && ./file`
No terminal output; inspect results in GDB. All programs exit with code 0.

## add
- **add1.asm** – 8-bit: `AL = 120 + 10 = 130 (0x82)`, stored in `result`. OF=1, SF=1 (signed overflow).
- **add2.asm** – 16-bit: `AX = 32000 + 500 = 32500 (0x7EF4)`, stored in `result`. No overflow.

## div
- **div2.asm** – 16-bit `div bx`: `DX:AX = 50000 / 300` → AX = 166 (quotient), DX = 200 (remainder).
- **div3.asm** – 32-bit `div ebx`: `EDX:EAX = 300000000 / 1000` → EAX = 300000, EDX = 0.

## mul
- **mul1.asm** – 8-bit `mul byte`: `AX = 25 * 10 = 250 (0xFA)`. AH = 0, so CF=OF=0.
- **mul2.asm** – 16-bit `mul word`: `DX:AX = 3000 * 200 = 600000 (0x927C0)` → DX = 0x0009, AX = 0x27C0. CF=OF=1.

## sub
- **sub2.asm** – 16-bit: `AX = 1000 - 2000 = -1000 (0xFC18)`. CF=1 (borrow), SF=1.
- **sub3.asm** – `sub` then `sbb`: `0 - 1 = 0xFFFF` (CF=1), then `sbb ax, 0` → `0xFFFF - 0 - 1 = 0xFFFE`.
