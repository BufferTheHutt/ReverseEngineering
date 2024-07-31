# CPU Register in x86 und x64

<div style="display: flex;">

<div style="display: flex; flex-direction: column; gap: 10px;">
    <div>
        <strong>Instruction Pointer (Befehlspointer)</strong>
        <div>
            <strong>x86: EIP (Extended Instruction Pointer)</strong>
            <p>32-bit Register</p>
            <p>Zeigt auf die nächste auszuführende Anweisung</p>
        </div>
        <div>
            <strong>x64: RIP (Register Instruction Pointer)</strong>
            <p>64-bit Register</p>
            <p>Erweitert für 64-bit Adressierung</p>
        </div>
    </div>

<div>
        <strong>General-Purpose Registers (Allgemeine Register)</strong>
        <div>
            <strong>EAX / RAX (Accumulator)</strong>
            <div>
                <strong>x86: EAX</strong>
                <p>32-bit Register</p>
                <p>Speichert Ergebnisse von arithmetischen Operationen</p>
                <p>Zugriffsmodi: 16-bit (AX), 8-bit (AH/AL)</p>
            </div>
            <div>
                <strong>x64: RAX</strong>
                <p>64-bit Register</p>
                <p>Entspricht EAX, aber mit erweiterter Größe</p>
            </div>
        </div>
        <div>
            <strong>EBX / RBX (Base Register)</strong>
            <div>
                <strong>x86: EBX</strong>
                <p>32-bit Register</p>
                <p>Häufig für Basisadressen verwendet</p>
                <p>Zugriffsmodi: 16-bit (BX), 8-bit (BH/BL)</p>
            </div>
            <div>
                <strong>x64: RBX</strong>
                <p>64-bit Register</p>
                <p>Entspricht EBX, aber mit erweiterter Größe</p>
            </div>
        </div>
        <div>
            <strong>ECX / RCX (Counter Register)</strong>
            <div>
                <strong>x86: ECX</strong>
                <p>32-bit Register</p>
                <p>Wird oft für Schleifenzähler verwendet</p>
                <p>Zugriffsmodi: 16-bit (CX), 8-bit (CH/CL)</p>
            </div>
            <div>
                <strong>x64: RCX</strong>
                <p>64-bit Register</p>
                <p>Entspricht ECX, aber mit erweiterter Größe</p>
            </div>
        </div>
        <div>
            <strong>EDX / RDX (Data Register)</strong>
            <div>
                <strong>x86: EDX</strong>
                <p>32-bit Register</p>
                <p>Häufig in Multiplikations- und Divisionsoperationen verwendet</p>
                <p>Zugriffsmodi: 16-bit (DX), 8-bit (DH/DL)</p>
            </div>
            <div>
                <strong>x64: RDX</strong>
                <p>64-bit Register</p>
                <p>Entspricht EDX, aber mit erweiterter Größe</p>
            </div>
        </div>
        <div>
            <strong>ESP / RSP (Stack Pointer)</strong>
            <div>
                <strong>x86: ESP</strong>
                <p>32-bit Register</p>
                <p>Zeigt auf den obersten Wert des Stacks</p>
            </div>
            <div>
                <strong>x64: RSP</strong>
                <p>64-bit Register</p>
                <p>Entspricht ESP, aber für 64-bit Adressierung</p>
            </div>
        </div>
        <div>
            <strong>EBP / RBP (Base Pointer)</strong>
            <div>
                <strong>x86: EBP</strong>
                <p>32-bit Register</p>
                <p>Wird oft verwendet, um auf Funktionsparameter zuzugreifen</p>
            </div>
            <div>
                <strong>x64: RBP</strong>
                <p>64-bit Register</p>
                <p>Entspricht EBP, aber mit erweiterter Größe</p>
            </div>
        </div>
        <div>
            <strong>ESI / RSI (Source Index)</strong>
            <div>
                <strong>x86: ESI</strong>
                <p>32-bit Register</p>
                <p>Für String-Operationen und als Offset verwendet</p>
            </div>
            <div>
                <strong>x64: RSI</strong>
                <p>64-bit Register</p>
                <p>Entspricht ESI, aber mit erweiterter Größe</p>
            </div>
        </div>
        <div>
            <strong>EDI / RDI (Destination Index)</strong>
            <div>
                <strong>x86: EDI</strong>
                <p>32-bit Register</p>
                <p>Wird für Zieladressen bei String-Operationen verwendet</p>
            </div>
            <div>
                <strong>x64: RDI</strong>
                <p>64-bit Register</p>
                <p>Entspricht EDI, aber mit erweiterter Größe</p>
            </div>
        </div>
        <div>
            <strong>R8-R15 (Zusätzliche Register in x64)</strong>
            <p>Nur in x64:</p>
            <p>64-bit Register, nicht vorhanden in 32-bit Systemen</p>
            <p>Zugriffsmodi: 32-bit (R8D-R15D), 16-bit (R8W-R15W), 8-bit (R8B-R15B)</p>
        </div>
    </div>

<div>
        <strong>Status Flag Registers (Statusregister)</strong>
        <p>Enthalten verschiedene Flags, die den Zustand des Prozessors nach Operationen anzeigen, wie z.B. Zero Flag (ZF), Carry Flag (CF).</p>
    </div>

 <div>
        <strong>Segment Registers (Segmentregister)</strong>
        <p>Verwendet, um Speichersegmente zu adressieren.</p>
        <p>Beispiele: CS (Code Segment), DS (Data Segment), SS (Stack Segment).</p>
</div>
</div>




<div style="flex: 1;">
<a href="">
    <img src="img/b3d7e425dae623de1ce2d57b25e4e809.png" alt="Packaging status" align="right" width="275px">
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
    <div>
    <a href="">
        <img src="img/trapFlag.png" alt="Trap Flag" align="right">
    </a>
    </div>
    <div>
    <strong>Segment-Register</strong>
    <ul>
        <li><strong>Code Segment (CS)</strong>: Zeigt auf den Code-Bereich im Speicher.</li>
        <li><strong>Data Segment (DS)</strong>: Zeigt auf den Datenbereich des Programms im Speicher.</li>
        <li><strong>Stack Segment (SS)</strong>: Zeigt auf den Stack des Programms im Speicher.</li>
        <li><strong>Extra Segments (ES, FS, GS)</strong>: Zeigen auf zusätzliche Datenbereiche und teilen den Speicher des Programms in vier verschiedene Datenabschnitte ein.</li>
    </ul>
    </div>
</div>

</div>
