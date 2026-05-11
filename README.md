[English](README.en.md)

# DNA# Online Interpreter

基于 DNA 双螺旋结构的深奥编程语言在线解释器，严格遵循 [esolangs.org/wiki/DNA-Sharp](https://esolangs.org/wiki/DNA-Sharp) 规范。

## 使用

打开 [index.html](index.html) 即可使用，无需服务器。

1. 选择源码形式（Symbol / Line / Helix）
2. 输入 DNA# 代码
3. 按 `Ctrl+Enter` 或点击 Run

## 16 条指令

| DNA 编码 | 符号 | 说明 |
|----------|------|------|
| `ATAT`   | `>`  | 指针右移 |
| `ATGC`   | `<`  | 指针左移 |
| `ATTA`   | `+`  | 当前字节 +1 |
| `ATCG`   | `-`  | 当前字节 -1 |
| `GCAT`   | `.`  | 输出 ASCII |
| `GCGC`   | `,`  | 输入 ASCII |
| `GCTA`   | `[`  | 循环开始 |
| `GCCG`   | `]`  | 循环结束 |
| `TAAT`   | `:=` | \*p = \*newp |
| `TAGC`   | `+=` | \*p += \*newp |
| `TATA`   | `-=` | \*p -= \*newp |
| `TACG`   | `*=` | \*p \*= \*newp |
| `CGAT`   | `/=` | \*p /= \*newp |
| `CGGC`   | `~`  | 输出整数 |
| `CGTA`   | `?`  | 输入整数 |
| `CGCG`   | `X`  | NOP / Quine |

## 三种源码形式

- **Symbol**：直接使用符号，如 `+++>+<[->+<]>.`
- **Line**：纯 ATGC 序列，如 `ATTAATTAATTAATATGCATTA...`
- **Helix**：双螺旋结构，含 `-` 连接线

## 内置示例

- Hello World
- Fibonacci Numbers
- Quine（自打印）

## 项目结构

```
├── index.html   # 页面
├── style.css    # 样式
└── app.js       # 解析器 + 解释器 + UI
```

## 规范

- [DNA# — Esolang Wiki](https://esolangs.org/wiki/DNA-Sharp)

## 许可证

MIT
