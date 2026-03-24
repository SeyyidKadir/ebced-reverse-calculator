# أبجد — Ebced Reverse Calculator

A free, open-source tool that converts any number back into all possible **Arabic letter combinations** based on the classical Abjad (Ebced) numeral system.

> *"A number has many faces. This tool reveals them all."*

![HTML](https://img.shields.io/badge/HTML-single--file-10b974?style=flat-square&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-10b974?style=flat-square&logo=javascript&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-10b974?style=flat-square)
![No dependencies](https://img.shields.io/badge/dependencies-none-10b974?style=flat-square)

---

## What is Ebced (Abjad)?

The **Abjad numeral system** is an ancient Arabic alphanumeric code where each of the 28 Arabic letters carries a specific numerical value:

| Letter | Value | Letter | Value | Letter | Value |
|--------|-------|--------|-------|--------|-------|
| أ Alif | 1 | ي Ya | 10 | ق Qaf | 100 |
| ب Ba | 2 | ك Kaf | 20 | ر Ra | 200 |
| ج Jim | 3 | ل Lam | 30 | ش Shin | 300 |
| د Dal | 4 | م Mim | 40 | ت Ta | 400 |
| ه Ha | 5 | ن Nun | 50 | ث Tha | 500 |
| و Waw | 6 | س Sin | 60 | خ Kha | 600 |
| ز Zay | 7 | ع Ayn | 70 | ذ Dhal | 700 |
| ح Ha | 8 | ف Fa | 80 | ض Dad | 800 |
| ط Ta | 9 | ص Sad | 90 | ظ Dha | 900 |
| | | | | غ Ghayn | 1000 |

Traditionally, Ebced is used to calculate the numerical value of words, names, Quranic verses, and dates. This tool does the **reverse**: given a number, it finds all possible letter combinations that produce that value.

---

## The Problem

Converting a number back to Arabic letters is not a simple reverse lookup. The number **200** for example could be:

- **ر** (Ra = 200) — direct match
- **ق + ق** (100 + 100)
- **ق + ن + ن** (100 + 50 + 50)
- **ن + ن + ن + ن** (50 + 50 + 50 + 50)
- ...and many more

There is no single correct answer — the meaning depends entirely on context and the user's interpretation. This tool presents all mathematical possibilities and lets the user decide.

---

## Features

- 🔢 **Reverse lookup** — any positive integer → all valid Arabic letter combinations
- 📄 **Lazy loading** — results generated in batches, no memory overload
- 🔁 **Checkpoint system** — continues exactly where it left off
- 🔤 **RTL Arabic display** — letters rendered right-to-left natively
- ⭐ **Direct match priority** — single-letter matches always shown first
- 🔀 **Sort modes** — fewest letters / highest value / lowest value
- 🔄 **Repeat toggle** — allow or disallow repeated letters
- 📱 **Fully responsive** — works on mobile, tablet, desktop
- 📦 **Zero dependencies** — single HTML file, works offline
- 🌙 **Black & emerald theme** — easy on the eyes

---

## Usage

Download `ebced_single.html` and open it in any browser. No installation, no server, no internet required.

```bash
git clone https://github.com/yourusername/ebced-reverse-calculator.git
# open ebced_single.html in your browser
```

---

## Algorithm

The core engine uses an **iterative stack-based generator** pattern:

- No recursion → no stack overflow risk
- Checkpoint-based → resumes from last position on "Load More"
- Sorted combination generation → guarantees no duplicate results
- `0` is rejected (zero has no form in Abjad)
- Negative numbers → absolute value
- Decimal numbers → rounded to nearest integer

---

## Files

| File | Description |
|------|-------------|
| `ebced_single.html` | Complete app — everything in one file |

---

## License

MIT — free to use, modify, and distribute.

---

## Built With

- Vanilla HTML / CSS / JavaScript
- [Amiri Font](https://fonts.google.com/specimen/Amiri) — Arabic typography
- [Cinzel Font](https://fonts.google.com/specimen/Cinzel) — Display headings
- [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) — Monospace UI

---

## 🤖 About the AI Behind This

This project was designed and built in collaboration with **[Claude](https://claude.ai)** by **[Anthropic](https://anthropic.com)** — not just code generation, but full algorithm design, edge case analysis, and architecture decisions were discussed and solved together before a single line of code was written.

If you're curious what thoughtful AI-assisted development looks like, give Claude a try → **[claude.ai](https://claude.ai)**

---

*Classical Arabic Abjad · 28 Letters · Immutable Values*
