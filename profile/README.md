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
| **[UniGPU™](https://github.com/MrSilverDuck/unigpu)** | Universal GPU compute runtime. One C-ABI DLL — `unigpu_ffi.dll` — with HIP / CUDA / Metal / D3DKMT-Direct / Vulkan / CPU backends. Write a kernel once in UniGPU IR, run it on any vendor's silicon. **Verified 47.31 TFLOP/s WMMA sustained on consumer AMD RX 7700 XT.** |
| **[Quack™](https://github.com/MrSilverDuck/quack)** | A Russian-English mixed programming language with **364 keywords across 9 human languages**, a teacher mode, and a poet mode. Pure Python core, optional GPU acceleration via UniGPU. |

Plus, included in `unigpu`:

- **SilverDuckOS™** — bare-metal UEFI boot manager (`crates/unigpu-os/`). Pirate splash, hardware probe, dynamic OS-discovery menu.
- **SilverDuck™ AI agent** — local Python/FastAPI agent. Hybrid local+cloud, OpenAI-compatible API, 14 endpoints, persistent memory. Federal-deliverable Tier 1 brain restricted to **U.S.-origin models only** (Llama 3.1 Meta · Phi-3.5 Microsoft) under owner-elected Absolute Zero Trust posture.
- **SDPC™** (SilverDuck Pipe Crypto) — hybrid post-quantum encrypted cloud-LLM handoff. X25519 + ML-KEM-1024 (NIST FIPS 203) + AES-256-GCM. **28 adversarial attack vectors rejected** by public red-team harness.

## Why this exists

Modern GPU stacks ship one assumption: *"there is one vendor."* Swap the silicon and the whole tower of Python + CUDA + cuDNN + PyTorch falls over. Linux/AMD on Windows in 2025 was a 12-step humiliation. NVIDIA wants rent. Apple wants the walled garden. Microsoft pretends DirectML works.

**MrSilverDuck assumes the opposite.** One IR. One DLL. Every vendor. No SDK to *build* the runtime — vendor SDKs are loaded at runtime *only* if you actually want JIT-compiled kernels.

A duck does not negotiate with the silicon. It quacks at it.

## For U.S. federal R&D program officers

These repos are the open-source dual-use compute stack of [Nightbox LLC](https://nightboxllc.com) (Wyoming, EIN 39-4373044, **SAM.gov UEI UHCAB6UXXKF2**, NAICS 541714 + 541512). The biotech program (NKG2D-LIF6 chimeric AAV9 receptor-effector for solid tumors) lives at the parent brand. The compute stack you see here is what makes that program — and any other federally-deliverable AI/ML workload that wants vendor neutrality — actually executable on consumer-tier hardware in a Section 889-aligned posture.

- **Section 889 supply-chain alignment** — UniGPU is the only vendor-neutral GPU runtime that ships with explicit per-backend EULA-scope declarations. The CUDA backend is NVIDIA-native execution only; cross-vendor execution paths run through Vulkan / SPIR-V / HIP / Metal / D3DKMT under cross-vendor licenses.
- **OMB M-22-09 / NIST SP 800-207 Zero Trust** — Tier 1 federal-deliverable AI brain path is restricted to U.S.-origin models under owner-elected posture stricter than Section 889 requires.
- **NIST FIPS-aligned cryptography** — SDPC uses only NIST-published primitives (FIPS 197 AES-256-GCM, FIPS 203 ML-KEM-1024, RFC 7748 X25519, NIST SP 800-38D GCM mode).
- **Federal compliance manifests** — twelve `.well-known` JSON endpoints documenting Section 889, FOCI, Zero Trust, research integrity, SBIR eligibility, SBIR data rights, federal POC directory, past performance, quad charts, capability statement, trademark policy, third-party validation. Index: [nightboxllc.com/llms.txt](https://nightboxllc.com/llms.txt)
- **Direct pitch to federal program officers** — the founders letter cross-mapped to seven named federal R&D mechanisms: [nightboxllc.com/founders-letter](https://nightboxllc.com/founders-letter)

If you are a NIH NCI / ARPA-H / DARPA AIE / AFWERX Spark / BARDA / NSF SBIR / DoD CDMRP program officer evaluating non-traditional contractors, the federal capability statement and pre-mapped solicitation index live at [nightboxllc.com/federal](https://nightboxllc.com/federal) and [nightboxllc.com/.well-known/solicitation-match.json](https://nightboxllc.com/.well-known/solicitation-match.json).

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

All code in MrSilverDuck repos is dual-licensed **Apache-2.0 OR MIT** (your choice) © 2026 Nightbox LLC.

`MrSilverDuck™`, `SilverDuck™`, `SilverDuckOS™`, `UniGPU™`, `Quack™`, `КРЯКА™` / `КИБЕРКРЯ™` (KIBERKRYA), `SDPC™`, `NB-R14B™`, `NB-VISION™`, and `NIGHTBOX SHIELD™` are common-law trademarks of Nightbox LLC with documented first-use-in-commerce dates. **Code is yours under Apache-2.0 / MIT — brand is ours.**

Apache 2.0 §6 expressly does not grant any right to use the licensor's trademarks; MIT is silent on trademarks but does not transfer them. **Forks are welcome — but rename your distribution.** Federal Government use of the marks for in-scope identification, deployment, documentation, evaluation, and description of NIGHTBOX LLC software is granted as standing nominative fair-use license under FAR 27.404-1 / DFARS 252.227-7013 / DFARS 252.227-7014.

Full policy: [nightboxllc.com/LICENSE-TRADEMARK](https://nightboxllc.com/LICENSE-TRADEMARK)
Machine-readable inventory: [nightboxllc.com/.well-known/trademark-policy.json](https://nightboxllc.com/.well-known/trademark-policy.json)
Misuse / license requests: [legal@nightboxllc.com](mailto:legal@nightboxllc.com)

---

<div align="center">

🏴‍☠️ *Captain Silverduck salutes you.* 🦆 *Кряяя, кремний свободен!*

</div>
