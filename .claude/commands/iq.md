---
description: Write an interview-question concept note into IQ_Notes/
argument-hint: <topic>
allowed-tools: Read, Write, Glob, Grep
---

Write an interview-prep concept note explaining: **$ARGUMENTS**

Save it to `IQ_Notes/<Topic>_IQ.md` in this repo, where `<Topic>` is a short
PascalCase or snake_case name derived from the topic. Create the file; do not
overwrite an existing note without saying so first.

Structure the note like this:

1. **Title** — `# <Topic>`
2. **Example** — pick a real file from this repo that demonstrates the concept.
   Show its path and the relevant code snippet in a fenced block. If no file
   fits, write a minimal example instead and say so.
3. **Comparison table** — the core of the note. Rows = aspects
   (what it is, who uses it, where it lives, portability, speed, readability,
   when to use it, common gotcha). Columns = the things being compared.
   If the topic is a single concept rather than a comparison, use
   columns of `Aspect | Detail | Why it matters`.
4. **Diagram** — an ASCII flow/pipeline block if the topic has stages, layers,
   or a lifecycle. Skip if it genuinely has none.
5. **Detail per item** — one short `###` section each, 3-5 bullets, plus any
   command the reader can run to see it themselves.
6. **Quick analogy table** — plain-English analogy per item.
7. **Language / tool comparison table** — how other languages or frameworks
   handle the same idea.
8. **Interview answer** — a 3-4 sentence version to say out loud.

Rules:
- Tables are the priority. Prefer a table over prose wherever possible.
- Be technically exact. Name the real components (engines, compilers, specs).
- Keep it scannable: short bullets, no filler paragraphs.
- Use GitHub-flavored markdown only.
