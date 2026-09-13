# LEARNPLAYWRIGHT3X 🚀

[![Node.js CI](https://img.shields.io/badge/Node.js-v16%2B-green.svg)](https://nodejs.org/)
[![JavaScript](https://img.shields.io/badge/Language-JavaScript%20%2F%20TypeScript-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Playwright](https://img.shields.io/badge/Automation-Playwright-blueviolet.svg)](https://playwright.dev/)
[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](LICENSE)

> A curated collection of hands-on programs, concept explanations, edge-case exercises, and interview questions designed to master **JavaScript**, **TypeScript**, and **Playwright Automation Testing** from first principles to advanced concepts.

---

## 📌 Repository Overview

`LEARNPLAYWRIGHT3X` serves as a comprehensive, structured learning path and interview preparation workspace. It breaks down complex JavaScript language fundamentals, type systems, and automation concepts into modular, executable code examples paired with in-depth interview notes.

---

## 📂 Repository Layout

```
LEARNPLAYWRIGHT3X/
├── 01_chapter_javascript/          # JS Basics & Hello World
├── 02_chapter_Javascript_concept/  # Variable Declarations & Scope (let/var/const)
├── 03_chapter_Identifier/          # Naming Rules, Comments & Edge Cases
├── 04_chapter_Literal/             # Literals, Data Types, Null & Undefined
├── 05_chapter_Operator/            # Operators, Type Conversion & Interview Scenarios
├── 06_chapter_Statement/           # Control Flow Statements & Conditionals
├── 07_chapter_switch/              # Switch Cases, Grouping & API Testing Mocking
├── IQ_Notes/                       # Deep-Dive Interview Question Guides & Notes
├── .claude/                        # Custom Automation Commands & Helpers
├── package.json                    # Project Configuration & Dependencies
└── README.md                       # Project Documentation
```

---

## 📚 Chapter Breakdown

### 🔹 [01_chapter_javascript](./01_chapter_javascript)
- **Topics**: Getting started with JavaScript runtime environment.
- **Key Files**:
  - [`01_HelloWord.js`](./01_chapter_javascript/01_HelloWord.js): Console logging and basic setup.

### 🔹 [02_chapter_Javascript_concept](./02_chapter_Javascript_concept)
- **Topics**: Variable declarations, block scope vs function scope, reassignment rules.
- **Key Files**:
  - [`01_let_concept.js`](./02_chapter_Javascript_concept/01_let_concept.js): Demystifying `let` declaration and temporal dead zone (TDZ).
  - [`02_let_concept.js`](./02_chapter_Javascript_concept/02_let_concept.js): Hands-on scoping exercises.

### 🔹 [03_chapter_Identifier](./03_chapter_Identifier)
- **Topics**: Valid/invalid identifier naming rules, reserved keywords, single & multi-line comments.
- **Key Files**:
  - [`03_Identifer_Rules.js`](./03_chapter_Identifier/03_Identifer_Rules.js): Syntax rules for identifiers.
  - [`04_Identifer_Rues_Part2.js`](./03_chapter_Identifier/04_Identifer_Rues_Part2.js): Special character allowed sets (`$`, `_`).
  - [`05_Comments.js`](./03_chapter_Identifier/05_Comments.js): Documentation & comment standards.
  - [`06_Identifer_IQ.js`](./03_chapter_Identifier/06_Identifer_IQ.js): Common interview questions on naming conventions.

### 🔹 [04_chapter_Literal](./04_chapter_Literal)
- **Topics**: Numeric, string, boolean literals, differences between `null` and `undefined`, type coercion.
- **Key Files**:
  - [`07_Literal.js`](./04_chapter_Literal/07_Literal.js): Literal types overview.
  - [`08_null_undefined.js`](./04_chapter_Literal/08_null_undefined.js): Primitive types comparison.
  - [`09_Null_IQ.js`](./04_chapter_Literal/09_Null_IQ.js): `typeof null` legacy bug (`"object"`) and interview questions.
  - [`11_Number.js`](./04_chapter_Literal/11_Number.js) & [`12_Number_Part2.js`](./04_chapter_Literal/12_Number_Part2.js): Floating point precision & BigInt behavior.

### 🔹 [05_chapter_Operator](./05_chapter_Operator)
- **Topics**: Exhaustive exploration of JavaScript operators, tricky comparisons, type conversion, and ternary expressions.
- **Key Files**:
  - [`13_DataType.js`](./05_chapter_Operator/13_DataType.js): Dynamic typing rules.
  - [`14_Assignment_Operator.js`](./05_chapter_Operator/14_Assignment_Operator.js) – [`17_Logical_Operators.js`](./05_chapter_Operator/17_Logical_Operators.js): Fundamental operators.
  - [`18_Confusing_Comparsion.js`](./05_chapter_Operator/18_Confusing_Comparsion.js) & [`18_Confusing_Comparsion_P2.js`](./05_chapter_Operator/18_Confusing_Comparsion_P2.js): Loose (`==`) vs Strict (`===`) equality edge cases.
  - [`22_Ternary_Op.js`](./05_chapter_Operator/22_Ternary_Op.js) & [`28_Nested_Terny_Op.js`](./05_chapter_Operator/28_Nested_Terny_Op.js): Concise conditional evaluations.
  - [`32_In_De_Op.js`](./05_chapter_Operator/32_In_De_Op.js) – [`35_Decrement.js`](./05_chapter_Operator/35_Decrement.js): Prefix vs Postfix increment/decrement behavior.
  - [`36_Null_Coalescing.js`](./05_chapter_Operator/36_Null_Coalescing.js): `??` vs `||` short-circuiting logic.
  - **Interview Challenges**: [`20_Question.js`](./05_chapter_Operator/20_Question.js), [`23_IQ.js`](./05_chapter_Operator/23_IQ.js)–[`27_IQ5.js`](./05_chapter_Operator/27_IQ5.js), [`29_IQ_NT.js`](./05_chapter_Operator/29_IQ_NT.js), [`30_NT_IQ2.js`](./05_chapter_Operator/30_NT_IQ2.js).

### 🔹 [06_chapter_Statement](./06_chapter_Statement)
- **Topics**: `if-else` branches, multiple condition chains, guard clauses.
- **Key Files**:
  - [`38_Multiple_Condition.js`](./06_chapter_Statement/38_Multiple_Condition.js): Complex multi-condition evaluations.
  - [`37_IQ.js`](./06_chapter_Statement/37_IQ.js) & [`38_IQ2.js`](./06_chapter_Statement/38_IQ2.js): Control flow interview problems.

### 🔹 [07_chapter_switch](./07_chapter_switch)
- **Topics**: `switch` statements, case grouping, fallthrough behavior, and real-world API status testing code.
- **Key Files**:
  - [`39_Switch.js`](./07_chapter_switch/39_Switch.js): Basic switch structure.
  - [`42_REAL_API_Testing.js`](./07_chapter_switch/42_REAL_API_Testing.js): Practical application in handling HTTP status codes.
  - [`43_Switch_Group.js`](./07_chapter_switch/43_Switch_Group.js): Combining case conditions.
  - [`40_IQ.js`](./07_chapter_switch/40_IQ.js) – [`47_IQ4.js`](./07_chapter_switch/47_IQ4.js): Switch interview tricky questions.

---

## 🧠 Interview Question Notes (`IQ_Notes`)

The [`IQ_Notes`](./IQ_Notes) folder contains detailed conceptual breakdown documents for technical interviews. Each note includes comparison tables, code snippets, ASCII diagrams, common pitfalls, and spoken interview answers.

| Note Document | Core Focus Area |
|---|---|
| 📄 [`IQ_Notes/README.md`](./IQ_Notes/README.md) | Index of all interview topic guides & note writing guidelines |
| 📄 [`source_codeBytecode_Binary_IQ.md`](./IQ_Notes/source_codeBytecode_Binary_IQ.md) | Source Code vs Bytecode vs Binary Code (V8 Ignition, TurboFan, JVM) |

---

## 🛠️ Prerequisites & Setup Instructions

### 1. Requirements
- **Node.js**: `v16.0.0` or higher
- **npm**: `v7.0.0` or higher
- **Git**: Installed and configured

### 2. Clone & Install
```bash
# Clone repository
git clone https://github.com/Sriradha-108/LEARNPLAYWRIGHT3X.git

# Navigate to project root
cd LEARNPLAYWRIGHT3X

# Install required dependencies
npm install
```

---

## 💻 How to Run JavaScript Programs

You can execute any individual script using Node.js directly from your command line:

```bash
# Run a specific program
node 01_chapter_javascript/01_HelloWord.js

# Run operator exercises
node 05_chapter_Operator/18_Confusing_Comparsion.js

# Run API Testing simulation script
node 07_chapter_switch/42_REAL_API_Testing.js
```

---

## 🗺️ Learning Roadmap

```
[Phase 1: JS Fundamentals] ---> [Phase 2: ES6+ & Async JS] ---> [Phase 3: TypeScript Basics] ---> [Phase 4: Playwright Web & API Automation]
        (Current Focus)
```

1. 🟡 **JavaScript Foundations** *(Chapters 01–07)*: Data types, scoping, operators, equality, control flow, functions, and objects.
2. 🟠 **Advanced JS & Async**: Closures, prototypal inheritance, Promises, `async/await`, Event Loop.
3. 🔵 **TypeScript Fundamentals**: Static typing, interfaces, generics, type aliases, and TS compiler configuration.
4. 🟣 **Playwright Test Automation**: Page Object Model (POM), Locators, Actions, Assertions, Network Interception, CI/CD Integration.

---

## 📄 License

This project is licensed under the **ISC License**.

---

⭐ *If you find this repository helpful in your learning journey or interview preparation, don't forget to give it a star!*
