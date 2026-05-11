[中文](README.md)

# DNA# Online Interpreter

An online interpreter for the DNA# esoteric programming language, strictly following the [esolangs.org/wiki/DNA-Sharp](https://esolangs.org/wiki/DNA-Sharp) specification.

## Usage

Open [index.html](index.html) in a browser — no server needed.

1. Select source form (Symbol / Line / Helix)
2. Enter DNA# code
3. Press `Ctrl+Enter` or click Run

## 16 Instructions

| DNA  | Symbol | Description |
|------|--------|-------------|
| `ATAT` | `>`  | Move pointer right |
| `ATGC` | `<`  | Move pointer left |
| `ATTA` | `+`  | Increment current byte |
| `ATCG` | `-`  | Decrement current byte |
| `GCAT` | `.`  | Output ASCII |
| `GCGC` | `,`  | Input ASCII |
| `GCTA` | `[`  | Loop start |
| `GCCG` | `]`  | Loop end |
| `TAAT` | `:=` | \*p = \*newp |
| `TAGC` | `+=` | \*p += \*newp |
| `TATA` | `-=` | \*p -= \*newp |
| `TACG` | `*=` | \*p \*= \*newp |
| `CGAT` | `/=` | \*p /= \*newp |
| `CGGC` | `~`  | Output integer |
| `CGTA` | `?`  | Input integer |
| `CGCG` | `X`  | NOP / Quine |

## Three Source Forms

- **Symbol** — raw symbols: `+++>+<[->+<]>.`
- **Line** — pure ATGC: `ATTAATTAATTAATATGCATTA...`
- **Helix** — double helix structure with `-` connectors

## Built-in Examples

- Hello World
- Fibonacci Numbers
- Quine

## Project Structure

```
├── index.html   # page
├── style.css    # styles
└── app.js       # parser + interpreter + UI
```

## Specification

- [DNA# — Esolang Wiki](https://esolangs.org/wiki/DNA-Sharp)

## License

MIT
