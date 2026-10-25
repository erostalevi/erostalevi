<div align="center">

# Hola, I'm Eros 👋

**Backend & full-stack engineer** · currently building [**Napple**](https://github.com/erostalevi/Napple)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-erosneto-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/erosneto/)
[![Email](https://img.shields.io/badge/Email-talevineto%40gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:talevineto@gmail.com)
![Location](https://img.shields.io/badge/Santiago-Chile-2ea44f?style=flat&logo=googlemaps&logoColor=white)

</div>

---

<div align="center">

# 🍎 Napple

### Turn a Switch game you own into a native Apple Silicon app.

**Ahead-of-time ARM64 rewrite · Horizon HLE · NVN → Metal · no emulator, no JIT**

![Rust](https://img.shields.io/badge/core-Rust%202024-orange?style=flat&logo=rust&logoColor=white)
![C and Objective-C](https://img.shields.io/badge/runtime-C%20%2B%20Objective--C-blue?style=flat)
![SwiftUI](https://img.shields.io/badge/studio-SwiftUI-F05138?style=flat&logo=swift&logoColor=white)
![Metal](https://img.shields.io/badge/GPU-Metal-black?style=flat&logo=apple&logoColor=white)
![Status](https://img.shields.io/badge/status-early%20%2F%20experimental-yellow?style=flat)

[**View the repository →**](https://github.com/erostalevi/Napple)

</div>

### The idea

The Switch and every Apple Silicon Mac are both **ARM64**. So instead of emulating the console, Napple **runs the game's own machine code natively** and rewrites, ahead of time, only the few things macOS forbids: the reserved `x18` register, the thread-pointer register, `svc` system calls and the timer-counter registers.

Everything the game asks the console OS for is answered by a **Horizon high-level-emulation runtime**, and the GPU API (**NVN**) is translated to **Metal**. The result is a standalone, locally signed `.app` built from your own copy of the game. With no JIT involved, the door also stays open for iOS and iPadOS.

### The pipeline

```
 your files: game (XCI / NSP / NSZ) + prod.keys + firmware
   │
   ├─ 1 ingest    container parse, NCA decrypt, ExeFS / RomFS, updates + DLC (BKTR patches)
   ├─ 2 analyze   NSO load, function discovery, patch-site scan
   ├─ 3 resolve   signature lookup (known signatures → reverse-engineering fallback)
   ├─ 4 rewrite   AArch64 rewriter: x18, TPIDR, svc, counters, 4K→16K page issues
   ├─ 5 package   .app = runtime + per-game patch table
   │
   └─ run         loader · Horizon kernel + services · NVN→Metal · audio · input · saves
```

Per-game knowledge lives only in **data** (signatures, patch tables), never in per-game code branches. Napple is built to be game-agnostic.

### What it does

| | |
|---|---|
| ⚡ **Native speed** | Guest code runs directly on the CPU. No interpreter or recompiler at run time. |
| 🧠 **Horizon kernel + HLE services** | Threads, scheduling, memory, sessions and IPC, plus a broad set of system services, with offline answers for the online ones. |
| 🎮 **NVN → Metal** | A Maxwell shader-ISA translator, NVN pipeline and format support, MSAA, indirect draws, query objects and more. |
| 🔊 **Audio and input** | Audio renderer (reverb, delay, compressor, limiter, Opus) over Core Audio. GameController input with rumble, plus keyboard and mouse mapping. |
| 💾 **Saves, updates and DLC** | Base game, updates and DLC packs merge in any container, in any order. |
| 🖥️ **Napple Studio** | A SwiftUI app: drop a game on the window, watch the pipeline run, install the result. |
| 📋 **Compatibility matrix** | Every game and every pipeline stage tracked with evidence. |

### Where it stands

Early and moving fast. Two titles currently boot all the way to their title screen or early gameplay on the runtime; neither is fully playable yet.

The table estimates how much of the Switch platform surface the pipeline and runtime cover (not per-game compatibility):

| Area | Coverage |
|---|---|
| CPU: AOT A64 rewrite | 100% |
| Loader: NSO / NRO / modules / relocations | 100% |
| Kernel: svcs + scheduling | 99% |
| IPC: HLE service coverage | 97% |
| IPC: command depth (implemented vs. stubbed) | 45% |
| GPU: Maxwell shader ISA | 81% |
| GPU: NVN API surface | 81% |
| GPU: formats + pipeline features | 83% |
| Audio | 94% |
| Input | 99% |
| Content: containers, crypto, updates, DLC | 91% |
| Saves + storage | 100% |
| Library applets | 48% |
| Video / media decode | 61% |
| **Overall** | **≈ 87%** |

Coverage is not compatibility: the long tail of command depth, shader corner cases and GPU behaviour is exactly what real games trip over first.

### Try it

Needs an Apple Silicon Mac, Xcode command line tools, a Rust toolchain, and your own keys and game.

```sh
cargo build --release -p napple-cli
make -C runtime && make -C packaging
studio/build_app.sh                      # optional GUI

target/release/napple ingest <game.xci|.nsp|.nsz> -k prod.keys
target/release/napple decomp <game> -k prod.keys -o out/ --updates latest --dlc all
```

### Legal, up front

You need to **own the game** and supply **your own `prod.keys` and firmware**. Nothing is downloaded, bundled or committed, and the repository contains no game bytes, keys or firmware. Builds are for personal use only. Napple is not affiliated with or endorsed by Nintendo.

---

## 👋 About me

I've spent 6+ years building services for banking, fintech and retail in Chile (**Itaú, Scotiabank, Transbank** projects), mostly in **TypeScript / Node.js (NestJS)** and **C# / .NET** on **AWS** and **GCP**. Napple is where I go low-level: Rust, C and Swift on Apple Silicon.

|   |   |
|---|---|
| 🔭 **Now** | Working at [ForPay](https://forpay.cl), and finishing my B.Eng. in Computer Science (Duoc UC, Dec 2027) |
| 🎓 **Certified** | AWS Cloud Practitioner · Oracle SQL · Oracle PL/SQL |
| 🗣️ **Languages** | Portuguese, Spanish, English (native-level) · Italian (intermediate) |

## 🧰 Tech

![Rust](https://img.shields.io/badge/Rust-000?style=flat&logo=rust&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-F05138?style=flat&logo=swift&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat&logo=dotnet&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle%20PL%2FSQL-F80000?style=flat&logo=oracle&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)

## 🗂️ Other projects

- [**Aperture**](https://github.com/erostalevi/Aperture): a fast, local, terminal-native image generation REPL for Apple Silicon (Python, PyTorch)
- [**typpo**](https://github.com/erostalevi/typpo): a typing-speed game for the command line (Shell)

---

<div align="center">

**Let's talk** · [LinkedIn](https://www.linkedin.com/in/erosneto/) · [talevineto@gmail.com](mailto:talevineto@gmail.com)

</div>
