# Source Code vs Bytecode vs Binary Code

Example file: `LEARNPLAYWRIGHT3X/01_chapter_javascript/01_HelloWord.js`

```js
console.log("Hello, world!");
```

---

## Comparison Table

| Aspect | Source Code | Bytecode | Binary Code (Machine Code) |
|---|---|---|---|
| **What it is** | Human-written text following language rules | Intermediate, low-level instruction set for a virtual machine | Raw CPU instructions as 0s and 1s |
| **Audience** | Humans | Virtual Machine (V8, JVM, CLR) | CPU / hardware |
| **In our example** | `console.log("Hello, world!");` in `01_HelloWord.js` | V8 Ignition bytecode generated when Node runs the file | x86-64 / ARM64 instructions the laptop CPU actually executes |
| **Who produces it** | You (the developer) | Compiler/interpreter front-end (V8 parser + Ignition) | JIT compiler (V8 TurboFan) or AOT compiler (gcc, rustc) |
| **File form** | `.js`, `.java`, `.py`, `.c` | `.class` (Java), `.pyc` (Python); JS bytecode stays in memory (unless cached via `v8.serialize`/code cache) | `.exe`, `.dll`, `.o`, `.so`, ELF/PE |
| **Readable?** | Yes, plain text | Semi-readable via a disassembler | No, only hex/disassembly |
| **Portable?** | Yes, runs anywhere the runtime exists | Yes, portable across OS/CPU **if** VM present | No, tied to one CPU architecture + OS |
| **Speed** | Slowest (must be parsed) | Medium (VM interprets it) | Fastest (direct execution) |
| **Needs a VM?** | Yes (via runtime) | Yes | No |
| **Editable by hand** | Easy | Hard | Practically never |
| **Example snippet** | `console.log("Hello, world!");` | `LdaGlobal [0]<br>LdaNamedProperty <br>CallProperty1<br>Return` | `48 8B 05 3A 00 00 00`<br>`E8 12 00 00 00` |

---

## The Pipeline for `01_HelloWord.js`

```
01_HelloWord.js                 <-- SOURCE CODE (you write this)
        |
        |  node 01_HelloWord.js
        v
   V8 Parser  -->  AST (Abstract Syntax Tree)
        |
        v
   Ignition Interpreter          <-- BYTECODE (V8 internal)
        |
        |  hot code path detected
        v
   TurboFan JIT Compiler
        |
        v
   x86-64 / ARM64 instructions   <-- BINARY / MACHINE CODE
        |
        v
      CPU executes  -->  prints "Hello, world!"
```

---

## Detail per Stage

### 1. Source Code
- The literal text in `01_HelloWord.js`.
- Written in JavaScript syntax, governed by the ECMAScript spec.
- Portable: same file runs on Windows, macOS, Linux — as long as Node.js is installed.
- Version-controlled in git; this is what code review sees.

### 2. Bytecode
- JavaScript is **not** shipped as bytecode files; V8 generates bytecode at runtime, in memory.
- V8's interpreter is called **Ignition**; its bytecode is a compact register-based instruction set.
- Purpose: faster to execute than re-parsing source, but still platform-independent.
- Compare: Java produces `.class` files and Python produces `.pyc` files, which are bytecode you can see on disk.

Inspect V8 bytecode for the example file:

```bash
node --print-bytecode 01_HelloWord.js
```

### 3. Binary Code
- Only hot (frequently executed) functions get compiled to machine code by **TurboFan**.
- Architecture-specific: an x86-64 build will not run on ARM64.
- This is what the CPU decodes and executes directly — no further translation.
- Languages like C/C++/Rust/Go skip the bytecode stage and compile straight to a binary (`.exe`).

---

## Quick Analogy

| Stage | Analogy |
|---|---|
| Source Code | A recipe written in English |
| Bytecode | The recipe translated into a standard chef's shorthand any kitchen understands |
| Binary Code | The actual hand movements of the chef in one specific kitchen |

---

## Language Comparison

| Language | Source | Bytecode | Binary | Notes |
|---|---|---|---|---|
| JavaScript (Node/V8) | `.js` | in-memory Ignition bytecode | JIT-generated at runtime | Bytecode not usually saved to disk |
| Java | `.java` | `.class` | JIT via HotSpot | Bytecode is a distributable artifact |
| Python | `.py` | `.pyc` in `__pycache__` | none (CPython interprets) | No JIT in standard CPython |
| C / C++ | `.c` / `.cpp` | none | `.exe` / `.o` | Compiled ahead of time |
| C# | `.cs` | CIL / MSIL in `.dll` | JIT via CLR | Similar model to Java |
