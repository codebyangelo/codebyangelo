# 👋 Hi, I'm Angelo

**Systems Security Engineer & AI Agent Defense Architect**
Bridging **low-level systems engineering** (kernel tracing, binary reversing, memory safety) with **deterministic security guardrails for autonomous AI agents** (Model Context Protocol, AST verification, and fail-closed sidecars).

---

### 🛡️ Merged Upstream Contributions

I contribute verified bug fixes, kernel tracing updates, memory safety patches, and regression suites to foundational open-source security and reversing tools:

#### ⚡ [iovisor/bcc](https://github.com/iovisor/bcc) (BPF Compiler Collection)
* **[PR #5546](https://github.com/iovisor/bcc/pull/5546)**: Migrated `tools/killsnoop` from brittle `sys_kill` kprobes to stable kernel tracepoints (`sys_enter_kill`, `tkill`, `tgkill`). Resolved breakage introduced in Linux 5.11+ and brought the Python implementation into parity with modern libbpf-tools.

#### 🔍 [radareorg/radare2](https://github.com/radareorg/radare2) & [radare2-testbins](https://github.com/radareorg/radare2-testbins)
* **[PR #26852](https://github.com/radareorg/radare2/pull/26852)**: Resolved SIGSEGV memory corruption in the PDB parser for enums with modified underlying types (`eLF_MODIFIER` pointer cast fix).
* **[PR #26862](https://github.com/radareorg/radare2/pull/26862)** & **[testbins #146](https://github.com/radareorg/radare2-testbins/pull/146)**: Built and upstreamed the minimal binary PDB test fixture and unit tests for type parsing.
* **[PR #26771](https://github.com/radareorg/radare2/pull/26771)**, **[PR #26617](https://github.com/radareorg/radare2/pull/26617)** & **[PR #26606](https://github.com/radareorg/radare2/pull/26606)**: Multi-stage refactor of math expression error handling across `cmd_seek` and `cmd_write` core commands (#23362), eliminating silent invalid writes and adding unit test coverage.

---

### 🚀 Flagship Security Architectures

#### 🦞 [Project Lobster](https://github.com/codebyangelo/project_lobster_v0.4.0)
*A context-aware security sidecar protecting autonomous AI agents against logic and injection attacks.*
* **stdio MCP Security Proxy**: Intercepts and validates Model Context Protocol tool invocations using per-session sliding-window tracking.
* **Hybrid Defense**: Pairs local deterministic "Iron Dome" rules with LLM intelligence under strict **fail-closed** security invariants.
* Built with concurrency-safe rate limiters, Trivy CI container scanning, and structured telemetry.

#### 🦗 [Project Mantis](https://github.com/codebyangelo/project-mantis)
*Autonomous DFIR framework for SIFT Workstations orchestrating memory forensics.*
* Orchestrates Volatility 3 and FLS via a multi-agent Finite State Machine (FSM).
* Uses a deterministic sieve and **"Hard Grounding" citation layer** to eliminate LLM hallucinations, generating traceable MITRE ATT&CK incident reports.

#### 🐙 [Project Octopus Core](https://github.com/codebyangelo/project-octopus-core)
*Agnostic security verification platform and repository profiler.*
* Performs automated architecture discovery and dynamic AST fallback sandboxing.
* Audits codebases against **NIST AI RMF**, **OWASP LLM Top 10**, and **MITRE**, emitting compliant **SARIF 2.1.0** reports.

#### 🐚 [Project Hermit](https://github.com/codebyangelo/project-hermit)
*Autonomous self-optimization daemon and dynamic MCP tool host.*
* Profiles, mutates, and tests routines inside isolated RAM-disk sandboxes using AST mutators and dual-phase scheduling.

---

### 🔬 Research & Threat Modeling

* **[Copilot Enterprise Privilege Escalation](https://github.com/codebyangelo/copilot-privilege-escalation-report-2025)**: Technical report detailing container path hijacking vulnerabilities leading to root escalation in Microsoft Copilot Enterprise environments.
* **[Agent-Native Threat Architecture](https://github.com/codebyangelo/agent-native-dev-report-2025)**: Threat models for context poisoning and agent hijacking mapped against NIST and ISO/IEC frameworks.

---

### 🧰 Technical Arsenal

* **Languages & Systems:** C, Python, Rust, Bash, Linux Kernel & Tracing (eBPF/BCC, tracepoints, kprobes), QEMU/KVM
* **Binary & Reverse Engineering:** radare2, Volatility 3, GDB, PDB internals, Memory Layout Analysis
* **AI Security & Protocols:** Model Context Protocol (MCP), LLM Guardrails, AST Parsing, SARIF, NIST AI RMF, OWASP LLM Top 10, MITRE ATT&CK