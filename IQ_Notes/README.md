# IQ_Notes — Interview Question Notes

Concept notes for interview prep. Each file explains one topic using comparison
tables, a real example from this repo, and a short spoken answer.

---

## Index

| Note | Topic | Covers |
|---|---|---|
| [source_codeBytecode_Binary_IQ.md](source_codeBytecode_Binary_IQ.md) | Source Code vs Bytecode vs Binary Code | V8 pipeline, Ignition, TurboFan, `.class` / `.pyc` / `.exe` |

_Add a row here whenever a new note is created._

---

## How to create a note

Use the `/iq` slash command from the repo root:

```
/iq <topic>
```

Examples:

```
/iq closures vs scope in JavaScript
/iq var vs let vs const
/iq JDK vs JRE vs JVM
/iq synchronous vs asynchronous
/iq == vs === in JavaScript
```

The command is defined in [`.claude/commands/iq.md`](../.claude/commands/iq.md).
Output lands here as `IQ_Notes/<Topic>_IQ.md`.

---

## Naming convention

| Rule | Example |
|---|---|
| Suffix every note with `_IQ.md` | `source_codeBytecode_Binary_IQ.md` |
| Topic name is short, no spaces | `var_let_const_IQ.md` |
| One topic per file | do not merge unrelated concepts |

---

## Note structure

Every note follows the same eight sections so they are scannable under time
pressure:

| # | Section | Purpose |
|---|---|---|
| 1 | Title | `# <Topic>` |
| 2 | Example | Real file path from this repo + code snippet |
| 3 | Comparison table | The core — rows are aspects, columns are the things compared |
| 4 | Diagram | ASCII flow/pipeline, only if the topic has stages |
| 5 | Detail per item | Short `###` section each, 3-5 bullets, plus a runnable command |
| 6 | Quick analogy table | Plain-English analogy per item |
| 7 | Language / tool comparison | How other languages handle the same idea |
| 8 | Interview answer | 3-4 sentences to say out loud |

---

## Writing rules

- Tables beat prose. Use a table wherever one fits.
- Be technically exact — name the real engines, compilers, and specs.
- Short bullets, no filler paragraphs.
- GitHub-flavored markdown only.
- Pull examples from actual repo files when one fits; otherwise write a minimal
  example and say that it is synthetic.

---

## Repo layout

```
LEARNPLAYWRIGHT3X/
├── .claude/
│   └── commands/
│       └── iq.md                 <-- /iq slash command definition
├── 01_chapter_javascript/        <-- JS practice files (examples come from here)
│   ├── 01_HelloWord.js
│   └── 02_let_concept.js
├── 02_CHAPTER_JAVA_CONCEPT/      <-- Java practice files
└── IQ_Notes/                     <-- you are here
    ├── README.md
    └── source_codeBytecode_Binary_IQ.md
```

---

## Suggested topic backlog

| Area | Topics |
|---|---|
| JavaScript core | `var` vs `let` vs `const`, hoisting, closures, scope chain, `this` binding, `==` vs `===` |
| Async | callbacks vs promises vs async/await, event loop, microtask vs macrotask |
| Objects | prototype chain, `class` vs constructor function, shallow vs deep copy |
| Node | CommonJS vs ES modules, `require` vs `import`, event emitters |
| Playwright | locators vs selectors, auto-waiting, fixtures, Page Object Model, `test.describe` vs `test.step` |
| Testing | unit vs integration vs E2E, flaky test causes, retries vs waits |
| Java | JDK vs JRE vs JVM, `==` vs `.equals()`, checked vs unchecked exceptions |
