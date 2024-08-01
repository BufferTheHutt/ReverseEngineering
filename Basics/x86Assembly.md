# x86 (32-bit) Crash Course

## OpCodes

ode in binary format: Der Programmcode wird auf der Festplatte und vom CPU als Folge von 1en und 0en verstanden.
Hexadezimaldarstellung: Um dies verständlicher zu machen, werden 8-Bit-Sequenzen (1 Byte) in eine Hexadezimalzahl umgewandelt.
Opcodes: Das sind Zahlen, die den Anweisungen des CPUs entsprechen.
Disassembler: Ein Tool, das Opcodes in menschenlesbare Assemblerbefehle umwandelt.
Beispiel für Disassembler-Ausgabe:
<br>
- mov eax, 0x5f wird als b8 5f 00 00 00 im Disassembler angezeigt. <br>
- b8 ist der Opcode, und 5f 00 00 00 ist der Operand.
<br>
Endianness: Die Reihenfolge der Bytes kann in Little-Endian-Darstellung vorliegen, d.h. umgekehrt.
<br>
Arten von Operanden:
<br>
- Immediate Operands: Feste Werte, z.B. 0x5f. <br>
- Register: Speicherorte im Prozessor, z.B. eax. <br>
- Memory Operands: Speicherorte im RAM, z.B. [eax], wobei der Wert von eax die Adresse ist.


# Einführung in Assembler-Instruktionen

Diese README bietet einen Überblick über einige grundlegende Assembler-Instruktionen, die oft beim Reverse Engineering von Malware verwendet werden.

## Inhaltsverzeichnis

- [Instruktionen](#instruktionen)
- [MOV-Anweisung](#mov-anweisung)
- [LEA-Anweisung](#lea-anweisung)
- [NOP-Anweisung](#nop-anweisung)
- [Shift-Anweisungen](#shift-anweisungen)
- [Rotate-Anweisungen](#rotate-anweisungen)

## Instruktionen

Instruktionen sagen der CPU, welche Operationen ausgeführt werden sollen. Dabei werden oft Operanden aus Registern, Speicher oder direkte Werte verwendet.

## MOV-Anweisung

Die `mov`-Anweisung verschiebt Daten von einer Quelle zu einem Ziel. Hier einige Beispiele:

- `mov eax, 0x5f`: Verschiebt den festen Wert `0x5f` in das Register `eax`.
- `mov ebx, eax`: Verschiebt den Inhalt von `eax` nach `ebx`.
- `mov eax, [0x5fc53e]`: Verschiebt den Wert an der Speicheradresse `0x5fc53e` nach `eax`.
- `mov eax, [ebp+4]`: Addiert 4 zu `ebp` und verschiebt den Wert der resultierenden Adresse nach `eax`.

## LEA-Anweisung

Die `lea`-Anweisung (`Load Effective Address`) speichert die Speicheradresse (nicht den Wert) in einem Register.

- `lea eax, [ebp+4]`: Speichert die Adresse `ebp+4` in `eax`.

## NOP-Anweisung

Die `nop`-Anweisung (`No Operation`) führt keine Operation aus und wird oft verwendet, um CPU-Zyklen zu verbrauchen oder als Platzhalter für Shellcode (`nop sled`).

## Shift-Anweisungen

Shift-Anweisungen verschieben Bits in einem Register nach links oder rechts:

- `shr` (shift right) und `shl` (shift left).
- Beispiel: `shl eax, 1` verschiebt die Bits in `eax` nach links, was einer Multiplikation mit 2 entspricht.

## Rotate-Anweisungen

Die Rotate-Anweisungen sind ähnlich wie die Shift-Anweisungen, aber die Bits werden wieder an das andere Ende des Registers gedreht:

- `ror` (rotate right) und `rol` (rotate left).
- Beispiel: `ror al, 1` dreht die Bits in `al` nach rechts, sodass das letzte Bit wieder an den Anfang gelangt.
