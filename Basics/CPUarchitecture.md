# CPU Register in x86 und x64

<div style="display: flex;">

<div style="flex: 1;">
<a> 
Instruction Pointer (Befehlspointer)

    x86: EIP (Extended Instruction Pointer)
        32-bit Register.
        Zeigt auf die nächste auszuführende Anweisung.
    x64: RIP (Register Instruction Pointer)
        64-bit Register.
        Erweitert für 64-bit Adressierung.

General-Purpose Registers (Allgemeine Register)
EAX / RAX (Accumulator)

    x86: EAX
        32-bit Register.
        Speichert Ergebnisse von arithmetischen Operationen.
        Zugriffsmodi: 16-bit (AX), 8-bit (AH/AL).
    x64: RAX
        64-bit Register.
        Entspricht EAX, aber mit erweiterter Größe.

EBX / RBX (Base Register)

    x86: EBX
        32-bit Register.
        Häufig für Basisadressen verwendet.
        Zugriffsmodi: 16-bit (BX), 8-bit (BH/BL).
    x64: RBX
        64-bit Register.
        Entspricht EBX, aber mit erweiterter Größe.

ECX / RCX (Counter Register)

    x86: ECX
        32-bit Register.
        Wird oft für Schleifenzähler verwendet.
        Zugriffsmodi: 16-bit (CX), 8-bit (CH/CL).
    x64: RCX
        64-bit Register.
        Entspricht ECX, aber mit erweiterter Größe.

EDX / RDX (Data Register)

    x86: EDX
        32-bit Register.
        Häufig in Multiplikations- und Divisionsoperationen verwendet.
        Zugriffsmodi: 16-bit (DX), 8-bit (DH/DL).
    x64: RDX
        64-bit Register.
        Entspricht EDX, aber mit erweiterter Größe.

ESP / RSP (Stack Pointer)

    x86: ESP
        32-bit Register.
        Zeigt auf den obersten Wert des Stacks.
    x64: RSP
        64-bit Register.
        Entspricht ESP, aber für 64-bit Adressierung.

EBP / RBP (Base Pointer)

    x86: EBP
        32-bit Register.
        Wird oft verwendet, um auf Funktionsparameter zuzugreifen.
    x64: RBP
        64-bit Register.
        Entspricht EBP, aber mit erweiterter Größe.

ESI / RSI (Source Index)

    x86: ESI
        32-bit Register.
        Für String-Operationen und als Offset verwendet.
    x64: RSI
        64-bit Register.
        Entspricht ESI, aber mit erweiterter Größe.

EDI / RDI (Destination Index)

    x86: EDI
        32-bit Register.
        Wird für Zieladressen bei String-Operationen verwendet.
    x64: RDI
        64-bit Register.
        Entspricht EDI, aber mit erweiterter Größe.

R8-R15 (Zusätzliche Register in x64)

    Nur in x64:
        64-bit Register, nicht vorhanden in 32-bit Systemen.
        Zugriffsmodi: 32-bit (R8D-R15D), 16-bit (R8W-R15W), 8-bit (R8B-R15B).

Status Flag Registers (Statusregister)

    Enthalten verschiedene Flags, die den Zustand des Prozessors nach Operationen anzeigen, wie z.B. Zero Flag (ZF), Carry Flag (CF).

Segment Registers (Segmentregister)

    Verwendet, um Speichersegmente zu adressieren.
    Beispiele: CS (Code Segment), DS (Data Segment), SS (Stack Segment).

</a>

</div>
<div style="flex: 1;">
<a href="">
    <img src="img/b3d7e425dae623de1ce2d57b25e4e809.png" alt="Packaging status" align="right">
</a>
</div>

<div style="flex: 1;">
    <strong>Status-Flag-Register</strong>
    <ul>
        <li><strong>EFLAGS/RFLAGS</strong>: 32-Bit-Register in 32-Bit-Systemen, 64-Bit-Register in 64-Bit-Systemen.</li>
        <li><strong>Zero Flag (ZF)</strong>: Zeigt an, wenn das Ergebnis der letzten Instruktion Null war. (ZF = 1 bei Ergebnis 0)</li>
        <li><strong>Carry Flag (CF)</strong>: Zeigt an, wenn die letzte Instruktion zu einem Überlauf oder Unterlauf geführt hat. (CF = 1 bei Überlauf)</li>
        <li><strong>Sign Flag (SF)</strong>: Zeigt an, ob das Ergebnis negativ ist oder das höchstwertige Bit gesetzt ist. (SF = 1 bei negativem Ergebnis)</li>
        <li><strong>Trap Flag (TF)</strong>: Aktiviert den Debugging-Modus, bei dem die CPU eine Instruktion nach der anderen ausführt. (Nützlich zum Debuggen)</li>
    </ul>

    <a href="">
        <img src="img/trapFlag.png" alt="Trap Flag" align="right">
    </a>

    <strong>Segment-Register</strong>
    <ul>
        <li><strong>Code Segment (CS)</strong>: Zeigt auf den Code-Bereich im Speicher.</li>
        <li><strong>Data Segment (DS)</strong>: Zeigt auf den Datenbereich des Programms im Speicher.</li>
        <li><strong>Stack Segment (SS)</strong>: Zeigt auf den Stack des Programms im Speicher.</li>
        <li><strong>Extra Segments (ES, FS, GS)</strong>: Zeigen auf zusätzliche Datenbereiche und teilen den Speicher des Programms in vier verschiedene Datenabschnitte ein.</li>
    </ul>

</div>

</div>
