# sairex53

**A crash is a symptom. I'm interested in what caused it.**

I spend most of my time exploring Linux internals — tracing kernel behavior, investigating bugs, reading source code, and building tools to make complicated failures easier to understand.

My focus is **Linux kernel development, C/C++, eBPF, systems programming, and low-level debugging**.

I'm particularly interested in the problems that don't have obvious answers: reference-counting mistakes, unexpected kernel behavior, memory corruption, and failures that only appear under specific conditions.

## Where I focus

- **Linux kernel & syzbot** — reproducing reported bugs, investigating root causes, testing fixes, and working toward upstream patches.
- **eBPF & tracing** — kernel instrumentation, fentry/kprobes, BTF, CO-RE, and understanding what actually happens at runtime.
- **C/C++ & Linux internals** — systems utilities, process state, namespaces, cgroups, memory, and low-level interfaces.
- **Reverse engineering & security research** — examining implementation details, understanding unexpected behavior, and investigating vulnerabilities.

I'm more interested in understanding *why* something fails than making the symptoms disappear.

## Things I'm building

### [RefScope](https://github.com/sairex53/refscope)

**Investigating Linux kernel object lifetimes and reference-counting bugs.**

RefScope is an experimental eBPF-based tracing and offline analysis tool.

It captures selected kernel operations, reconstructs per-object event timelines, and compares separate runs to identify suspicious differences in reference behavior.

The goal is to make investigating use-after-free bugs, reference leaks, and incorrect object lifetime management less dependent on guesswork.

Currently a research prototype. Synthetic tests are passing, but validation against a reproduced real-world kernel bug is still in progress.

### [nsdiff](https://github.com/sairex53/nsdiff)

**When two Linux processes behave differently, find out what's different.**

A C utility for comparing process execution environments, including namespaces, cgroups, mounts, credentials, security settings, and runtime state.

Designed to make subtle differences between shells, services, containers, and other Linux environments easier to inspect.

## Beyond my own repositories

I'm interested in contributing to existing projects rather than building everything from scratch.

My priorities are Linux kernel fixes, eBPF tooling, debuggers, tracing infrastructure, and system utilities that other developers actually depend on.

**Upstream work:**

[bcc PR #5571](https://github.com/iovisor/bcc/pull/5571) — proposed fix for multiarch header resolution when building BPF programs.

I want to contribute changes that are reproducible, technically justified, tested, and useful beyond my own machine.

## Tools of the trade

**Languages:** `C` · `C++` · `Assembly` · `Bash`

**Systems:** `Linux` · `Linux Kernel` · `eBPF` · `libbpf` · `BTF` · `CO-RE` · `AArch64`

**Debugging & development:** `GDB` · `QEMU` · `Clang/LLVM` · `Git` · `Kernel Tracing`

**Areas of interest:** `Kernel Debugging` · `syzbot` · `Memory Safety` · `Reverse Engineering` · `Vulnerability Research`

## What I'm looking for

I'm open to **open-source collaboration, paid low-level development, and remote engineering opportunities** involving Linux, C/C++, kernel debugging, eBPF, and systems tooling.

I'm especially interested in working with people who maintain real software, investigate difficult bugs, or build tools used by other developers.

If you have a reproducible Linux issue, a difficult debugging problem, or a systems project worth contributing to, I'd be interested in discussing it.

You can reach me through the contact link on my [GitHub profile](https://github.com/sairex53).

---

`Reproduce → Trace → Understand → Fix → Verify`

**Less guesswork. Better tools. Fewer unexplained bugs.**
