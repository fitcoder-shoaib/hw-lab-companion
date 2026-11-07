# Contributing to HW Lab Companion

Thanks for helping the next batch! You don't need to be a web developer to contribute. Most fixes are a few words in an HTML file.

## Ways to help

| You want to… | Do this |
|---|---|
| Report a wrong pin, equation or truth table | [Open a **Content error** issue](../../issues/new/choose). Say which experiment and what your manual says. |
| Share a viva question you were asked | [Open a **Viva question** issue](../../issues/new/choose). |
| Report something broken (a button, layout on your phone) | [Open a **Bug report**](../../issues/new/choose). |
| Fix it yourself | Follow the steps below and open a pull request. |

## Editing the files

Every tool is a single self-contained HTML file. No build step, no npm, no frameworks.

1. **Fork** the repo and clone your fork.
2. Open the file in any text editor (VS Code is great):
   - `guides/exam-guide.html`: experiment content lives in the `HW.EXPS = [ ... ]` array near the bottom. Digital basics are in `HW.BASICS`.
   - `guides/theory-bench.html`: experiments are in `const EXPS = [ ... ]`, flashcards in `const VIVA = [ ... ]`.
   - `simulators/ram-4x3.html`: holds two models (`src-vlab` and `src-simple`) embedded in one file so it works offline.
3. **Test it:** double-click the file to open it in your browser. Check the experiment you changed, and check it on a narrow window (phone width) too.
4. Commit with a clear message, e.g. `Fix 7476 GND pin in Exp 06`.
5. Open a pull request and fill in the checklist.

## Content rules

- **Be correct first.** Check pin numbers against a datasheet (TI or similar). If you're unsure, say so in the PR.
- **Plain words.** Write for a student seeing this for the first time. Short sentences beat long ones.
- **Your own words only.** Don't paste text or figures from the department lab manual, textbooks or other sites. Write it yourself.
- **Don't add record answers to copy.** This repo is for understanding, not for copying records.
- **Keep files self-contained.** No new external scripts or CDNs. The tools must keep working offline.

## Adding a new tool

Ideas are on the [roadmap](README.md#-roadmap). For a new simulator:

- Put it in `simulators/` as one `.html` file.
- Support light and dark mode and phone-width screens.
- Add a card for it on `index.html` and a row in the README.
- Add a screenshot to `docs/images/`.

Open an issue first if it's a big idea, so nobody duplicates work.

## Be kind

Everyone here was a confused first-year once. Be patient and respectful in issues and reviews.
