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