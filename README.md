# Heath Howren

I reverse engineer things. Mostly Windows binaries, kernel drivers and firmware, with a side of vulnerability research when something looks off.

I've been doing this publicly as [**Cyborg Elf**](https://www.youtube.com/c/cyborgelf) since 2015, first on YouTube and now through [Game Reversal Club](https://gamereversal.club), where I teach reverse engineering on software you own. By day I'm a cyber research engineer.

[gamereversal.club](https://gamereversal.club) · [YouTube](https://www.youtube.com/cyborgelf) · [Forum](https://gamereversal.club/forum/) · [Discord](https://discord.gg/NwRFmp3J2J) · [LinkedIn](https://www.linkedin.com/in/heath-howren/)

## What I'm working on

**[Pointer Lab](https://github.com/HeathHowren/Pointer-Lab)** is a memory research tool for Windows x64 that I wrote in C++20 because I wanted something I fully understood. It attaches to a process, scans and tracks values, freezes and writes them, disassembles, sets breakpoints and injects DLLs. It ships as one statically-linked exe with a practice target so you have something safe to point it at. GPLv2.

**[Signature Lab](https://github.com/HeathHowren/Signature-Lab)** is an x64dbg plugin I wrote to make byte signatures that survive a game update. It decodes every instruction so it only wildcards the bytes that actually move, checks the result against the whole module, and when the code isn't unique it signs whatever refers to it instead and gives you the math to get back. It outputs x64dbg, IDA, code+mask, C++ and Pointer Lab patterns. MIT.

**Smaller tools** that go with them, all MIT:

- **[sigscan](https://github.com/HeathHowren/sigscan)** is a single-header C++20 pattern scanner. It reads x64dbg, IDA, code+mask and Cheat Engine style signatures and finds them in a buffer, a file or a live process.
- **[iretable-tools](https://github.com/HeathHowren/iretable-tools)** converts, diffs, rebases and lints Pointer Lab project files, and imports Cheat Engine tables.
- **[hookscan](https://github.com/HeathHowren/hookscan)** finds the inline, import and export hooks in a running process by comparing its modules with the files on disk.
- **[debug-bench](https://github.com/HeathHowren/debug-bench)** runs about thirty anti-debug checks against itself and tells you which ones fire. Point your debugger-hiding setup at it.
- **[procpcap](https://github.com/HeathHowren/procpcap)** captures one process's network traffic to a pcapng for Wireshark.
- **[openxr-pose-layer](https://github.com/HeathHowren/openxr-pose-layer)** is an OpenXR API layer that logs, records and replays head and controller tracking.
- **[pe-mcp](https://github.com/HeathHowren/pe-mcp)** is an MCP server that gives an AI agent static analysis of a PE file: imports, strings, disassembly, xrefs and signatures.
- **[claude-game-re-plugin](https://github.com/HeathHowren/claude-game-re-plugin)** is a Claude Code plugin that teaches the Handbook's workflows and drives Pointer Lab, pe-mcp and the rest. It blocks memory writes unless you turn them on.

[**The Game Hacker's Handbook**](https://gamereversal.club/books/game-hackers-handbook/) is the book I wish I'd had when I started. 6 parts, 44 chapters, starting at memory scanning and ending in kernel mode and how anti-cheats work. Every example compiles under MSVC /W4 against lab targets you're allowed to poke at.

**Older stuff** like [CSGO-Cheats](https://github.com/HeathHowren/CSGO-Cheats), the [DX9 Kiero hook](https://github.com/HeathHowren/CSGO-ImGui-DX9-Kiero-Hook), [HWID-Info-Grabber](https://github.com/HeathHowren/HWID-Info-Grabber) and [Pattern-Scanning](https://github.com/HeathHowren/Pattern-Scanning) is from my early years. I leave it up because people still learn from it, but the tools above are a better picture of how I write code now. sigscan replaces Pattern-Scanning.

## What I work with

C and C++ most of the time, Python for glue, Rust when I get the chance, and enough x86/x64 assembly to read what the compiler did. IDA Pro, Ghidra, WinDbg, x64dbg, QEMU and Wireshark for analysis. Windows user and kernel mode, Linux, and embedded boards over UART or JTAG. Firmware extraction and emulation, fuzzing, exploit development.

## Background

Two B.S. degrees from Purdue, Cybersecurity and Computer Infrastructure & Network Engineering Technology, with a minor in Biometrics. Security+.

## Looking for

Vulnerability research, reverse engineering, hardware and firmware RE, or CNO development. If that's what you do, I'd like to talk.

heath@gamereversal.club · [heathhowren@yahoo.com](mailto:heathhowren@yahoo.com)

<p align="center">
  <img src="github-metrics.svg" alt="GitHub metrics">
</p>

<sub>Game Reversal Club is a personal project, funded and run independently. Nothing there is affiliated with, endorsed by, or representative of any employer, client, or institution.</sub>
