<h1 align="center">Code &amp; Crypto 💻💳</h1>

<p align="center">
  <em>Developer tools that tell you the truth about what they did.</em>
</p>

<p align="center">
  <a href="https://medium.com/@code-and-crypto"><img alt="Medium" src="https://img.shields.io/badge/Medium-000000?style=flat&logo=medium&logoColor=white"></a>
  <a href="https://www.reddit.com/user/codeandcrypto_"><img alt="Reddit" src="https://img.shields.io/badge/Reddit-FF4500?style=flat&logo=reddit&logoColor=white"></a>
  <a href="https://www.youtube.com/@code.and.crypto"><img alt="YouTube" src="https://img.shields.io/badge/YouTube-FF0000?style=flat&logo=youtube&logoColor=white"></a>
  <a href="mailto:code.and.crypto@proton.me"><img alt="Email" src="https://img.shields.io/badge/Proton%20Mail-6D4AFF?style=flat&logo=protonmail&logoColor=white"></a>
</p>

---

## What I work on

I build small, sharp tools and then write up what I found while building them.

The thing I care about most is **verification**. A lot of software reports success
because a process exited `0`, not because the work actually happened. Most of what I
publish comes out of chasing that gap in something and finding it was real.

- 🧰 **Developer tooling** — MCP servers, automation, things that drive other programs
- 🔍 **Reverse engineering** — reading source and binaries to find out what really runs
- 🐍 **Python**, ☕ **Java**, ⚙️ **C++ / Qt**, 🌐 **web**

---

## Featured

### [`inkscape-mcp-server`](https://github.com/code-and-crypto/inkscape-mcp-server)

A dependency-free MCP server that drives Inkscape — 23 tools, standard library only,
no `pip install`.

It exists because **Inkscape exits `0` when an action does not exist**, so any wrapper
trusting the exit code reports work that never happened. While building it I verified
ten separate traps against the real binary, including:

| Finding | Why it matters |
|---|---|
| `vacuum-defs` is a **silent no-op** headlessly | The obvious way to optimise an SVG does nothing at all |
| `fit-canvas-to-drawing` is in the source registry, **not in the binary** | A registry entry that lies |
| `--batch-process` silently discards `--export-filename` | Exits `0`, writes nothing |

Every one is written up with a reproduction in
[`docs/inkscape-findings.md`](https://github.com/code-and-crypto/inkscape-mcp-server/blob/main/docs/inkscape-findings.md).

---

## Where I write

- **Medium** — [@code-and-crypto](https://medium.com/@code-and-crypto) · long-form write-ups
- **Reddit** — [u/codeandcrypto\_](https://www.reddit.com/user/codeandcrypto_) · findings and discussion
- **YouTube** — [@code.and.crypto](https://www.youtube.com/@code.and.crypto) · walkthroughs

---

## Support

Everything here is MIT and free. If something saved you time, you can send a tip —
it goes straight into building the next one.

| | |
|---|---|
| **Bitcoin** | `YOUR-BTC-ADDRESS` |
| **Ethereum / Base** | `YOUR-ETH-ADDRESS` |
| **USDC** | `YOUR-USDC-ADDRESS` |

<sub>Prefer a card? I use <a href="https://ether.fi">ether.fi</a> — referral <code>90cfb343</code>.</sub>

---

<p align="center"><sub>Reach me at <a href="mailto:code.and.crypto@proton.me">code.and.crypto@proton.me</a></sub></p>
