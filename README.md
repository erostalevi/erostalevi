| Project | What it is | Stack |
|---|---|---|
| [Aperture](https://github.com/erostalevi/Aperture) | Terminal-native image generation REPL — local SDXL inference with model management, a background job queue, and an upscaling pipeline | Python, PyTorch, Apple Silicon |
| [mdma](https://github.com/erostalevi/mdma) | Minimal, keyboard-first Markdown editor for macOS | Swift |
| [typpo](https://github.com/erostalevi/typpo) | CLI typing-speed game | Shell |
[![LinkedIn](https://img.shields.io/badge/LinkedIn-erosneto-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/erosneto/)
[![Email](https://img.shields.io/badge/Email-talevineto%40gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:talevineto@gmail.com)
![Location](https://img.shields.io/badge/Santiago-Chile-2ea44f?style=flat&logo=googlemaps&logoColor=white)

## What I work with
</div>

`TypeScript` `Node.js` `NestJS` `C# / .NET` `React` `Python` `PostgreSQL` `Oracle PL/SQL` `Redis` `Docker` `Kubernetes` `AWS` `GCP` `Terraform` `CI/CD`
---

## Contact
## 👋 About

[LinkedIn](https://www.linkedin.com/in/erosneto/) · talevineto@gmail.com
I'm a **backend / full-stack developer** with 6+ years of experience on banking, fintech and retail projects for **Itaú, Scotiabank and Transbank**. My daily drivers are **TypeScript / Node.js (NestJS)** and **C# / .NET**, deployed on **AWS** and **GCP**.

On my own time I go lower-level: Rust, C and Swift, mostly on Apple Silicon.

|   |   |
|---|---|
| 🔭 **Now** | Freelance full-stack work, plus finishing my B.Eng. in Computer Science (Duoc UC, Dec 2027) |
| 🧪 **Building** | [Napple](https://github.com/erostalevi/Napple), a native Apple Silicon runtime for Switch games |
| 📱 **Shipped** | Mobile apps live on the App Store and Google Play |
| 🎓 **Certified** | AWS Cloud Practitioner · Oracle SQL · Oracle PL/SQL |
| 🗣️ **Languages** | Portuguese, Spanish, English (native-level) · Italian (intermediate) |

---

## 🚀 Featured projects

### 🍎 [Napple](https://github.com/erostalevi/Napple)
**Turn a Switch game you own into a native Apple Silicon app.**

![Rust](https://img.shields.io/badge/Rust-000?style=flat&logo=rust&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![Objective-C](https://img.shields.io/badge/Objective--C-438eff?style=flat)
![SwiftUI](https://img.shields.io/badge/SwiftUI-F05138?style=flat&logo=swift&logoColor=white)
![Metal](https://img.shields.io/badge/Metal-black?style=flat&logo=apple&logoColor=white)
![Status](https://img.shields.io/badge/status-early%20%2F%20experimental-yellow?style=flat)

The Switch and every Apple Silicon Mac are both ARM64, so instead of emulating the console, Napple runs the game's own machine code natively and rewrites ahead of time only what macOS forbids. A Horizon HLE runtime answers the console OS calls, and the GPU API (NVN) is translated to Metal. **No emulator, no JIT.**

- **AArch64 rewriter** for the reserved `x18` register, thread pointer, `svc` calls and timer counters
- **Horizon kernel + HLE services**: threads, scheduling, memory, IPC, with offline answers for online services
- **NVN → Metal** with a Maxwell shader-ISA translator
- **Audio and input** over Core Audio and GameController
- **Napple Studio**, a SwiftUI app: drop a game on the window, watch the pipeline run, install the result
- A per-game **compatibility matrix** tracked with evidence

You bring your own game, keys and firmware; the repo contains none of them.

---

### 🎨 [Aperture](https://github.com/erostalevi/Aperture)
**A fast, local, terminal-native image generation REPL for Apple Silicon.**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Apple Silicon](https://img.shields.io/badge/Apple%20Silicon-black?style=flat&logo=apple&logoColor=white)

Load the model once, then iterate at the prompt with full control over every parameter. Local SDXL inference with model management, a background job queue and an upscaling pipeline, all without leaving the terminal.

---

### ⌨️ [typpo](https://github.com/erostalevi/typpo)
**A simple typing-speed game for the command line.**
