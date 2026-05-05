<div align="center">

# 🦆 MrSilverDuck

### Universal GPU compute. Bare-metal boot. A duck programming language.

**Short link: [mrsilverduck.lif-6.com](https://mrsilverduck.lif-6.com)**

*Built by [Nightbox LLC](https://nightboxllc.com) · Wyoming, USA · MIT licensed*

[![UniGPU](https://img.shields.io/github/v/release/MrSilverDuck/unigpu?include_prereleases&label=UniGPU&color=orange)](https://mrsilverduck.lif-6.com/unigpu)
[![Quack](https://img.shields.io/github/v/release/MrSilverDuck/quack?include_prereleases&label=Quack&color=ff69b4)](https://mrsilverduck.lif-6.com/quack)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/MrSilverDuck/unigpu/blob/main/LICENSE)

</div>

---

## What we ship

| Project | What it is |
|---|---|
| **[UniGPU](https://github.com/MrSilverDuck/unigpu)** | Universal GPU compute runtime. One C-ABI DLL — `unigpu_ffi.dll` — with HIP / CUDA / Metal / D3DKMT-Direct / Vulkan / CPU backends. Write a kernel once in UniGPU IR, run it on any vendor's silicon. |
| **[Quack](https://github.com/MrSilverDuck/quack)** | A Russian-English mixed programming language with **364 keywords across 9 human languages**, a teacher mode, and a poet mode. Pure Python core, optional GPU acceleration via UniGPU. |

Plus, included in `unigpu`:

- **SilverDuckOS** — bare-metal UEFI boot manager (`crates/unigpu-os/`). Pirate splash, hardware probe, dynamic OS-discovery menu.
- **SilverDuck AI agent** — local Python/FastAPI agent. Hybrid local+cloud, OpenAI-compatible API, 14 endpoints, persistent memory.

## Why this exists

Modern GPU stacks ship one assumption: *"there is one vendor."* Swap the silicon and the whole tower of Python + CUDA + cuDNN + PyTorch falls over. Linux/AMD on Windows in 2025 was a 12-step humiliation. NVIDIA wants rent. Apple wants the walled garden. Microsoft pretends DirectML works.

**MrSilverDuck assumes the opposite.** One IR. One DLL. Every vendor. No SDK to *build* the runtime — vendor SDKs are loaded at runtime *only* if you actually want JIT-compiled kernels.

A duck does not negotiate with the silicon. It quacks at it.

## By the numbers

| | |
|---|---:|
| GPU backends in `unigpu` | **6** (HIP · CUDA · Metal · Direct · Vulkan · CPU) |
| FFI symbols exposed | **16** |
| UniGPU IR opcodes | **41** |
| `unigpu_ffi.dll` size | **1.55 MiB** |
| `unigpu-os.efi` size | **~60 KiB** |
| SAXPY launch + sync (RX 7700 XT) | **495 µs** |
| Quack keywords | **364** across 9 human languages |
| Source code | Rust **9,170** + Python **21,041** LOC |
| External SDKs needed to build | **0** |

Full numbers: [BENCHMARKS.md](https://github.com/MrSilverDuck/unigpu/blob/main/BENCHMARKS.md)

## Roadmap

- **0.1.x** — Public source drop ✅ (you are here)
- **0.2.0** — Bootable ISO via archiso + GitHub Actions; ≥ 50 GB persistent USB; no BitLocker drama
- **0.3.0** — Vulkan / oneAPI backends; WebGPU fallback
- **0.4.0** — Quack 1.0 — REPL, syntax highlighting, more language packs

## Get involved

- 🐛 [Open an issue](https://mrsilverduck.lif-6.com/issues) — bugs, requests, hardware reports
- 🦆 [Read the FAQ](https://github.com/MrSilverDuck/unigpu/blob/main/FAQ.md) — answers most questions before they're asked
- 🛠️ [HACKING.md](https://github.com/MrSilverDuck/unigpu/blob/main/docs/HACKING.md) — add a backend, write a kernel
- 📋 [GETTING_STARTED.md](https://mrsilverduck.lif-6.com/docs) — clone → build → run

## Short links

| URL | Where it goes |
|---|---|
| [`mrsilverduck.lif-6.com`](https://mrsilverduck.lif-6.com) | this org |
| [`mrsilverduck.lif-6.com/unigpu`](https://mrsilverduck.lif-6.com/unigpu) | UniGPU repo |
| [`mrsilverduck.lif-6.com/quack`](https://mrsilverduck.lif-6.com/quack) | Quack repo |
| [`mrsilverduck.lif-6.com/releases`](https://mrsilverduck.lif-6.com/releases) | latest UniGPU release (incl. ISO) |
| [`mrsilverduck.lif-6.com/iso`](https://mrsilverduck.lif-6.com/iso) | bootable ISO download |
| [`mrsilverduck.lif-6.com/install`](https://mrsilverduck.lif-6.com/install) | one-line installer |
| [`mrsilverduck.lif-6.com/issues`](https://mrsilverduck.lif-6.com/issues) | bug tracker |

(All 301 via Cloudflare on `lif-6.com`. The biotech parent brand at [nightboxllc.com](https://nightboxllc.com) is intentionally separate.)

## Licenses & trademarks

All code in MrSilverDuck repos is **MIT** © 2026 Nightbox LLC.

`MrSilverDuck`, `SilverDuck`, `SilverDuckOS`, `UniGPU`, `Quack`, `КРЯКА` are trademarks of Nightbox LLC. Code is yours under MIT — brand is ours.

---

<div align="center">

🏴‍☠️ *Captain Silverduck salutes you.* 🦆 *Кряяя, кремний свободен!*

</div>
