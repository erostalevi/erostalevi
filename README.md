<div align="center">

# Eros Talevi

### Backend & full-stack engineer · systems tinkerer

Six years shipping services for banks, fintechs and retailers in Chile.<br>
Off the clock, I build native tooling for Apple Silicon.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-erosneto-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/erosneto/)
[![Email](https://img.shields.io/badge/Email-talevineto%40gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:talevineto@gmail.com)
![Location](https://img.shields.io/badge/Santiago-Chile-2ea44f?style=flat&logo=googlemaps&logoColor=white)

</div>

---

## 👋 About

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

![Shell](https://img.shields.io/badge/Shell-4EAA25?style=flat&logo=gnubash&logoColor=white)

A small, fun CLI project for measuring your typing speed.

---

## 🛠️ Tech I use

**Backend & cloud**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle%20PL%2FSQL-F80000?style=flat&logo=oracle&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)

**Frontend & systems**

![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Rust](https://img.shields.io/badge/Rust-000?style=flat&logo=rust&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-F05138?style=flat&logo=swift&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)

---

<div align="center">

**Let's talk** · [LinkedIn](https://www.linkedin.com/in/erosneto/) · [talevineto@gmail.com](mailto:talevineto@gmail.com)

</div>
