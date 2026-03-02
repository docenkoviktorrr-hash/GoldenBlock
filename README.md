# WinLock-EDU: Windows Security Research & Pentesting Tool (v3)

## ⚠️ LEGAL DISCLAIMER
**FOR EDUCATIONAL PURPOSES ONLY.**
This project is a Proof-of-Concept (PoC) created to study the behavior of UI-blocking software and low-level Windows API interactions. The author is NOT responsible for any damage caused by misuse of this tool. Unauthorized use against systems without prior consent is illegal.

---

## 🔍 Project Overview
WinLock-EDU is a research application that demonstrates how system-level functions can be used to restrict user access. It explores the following concepts:
* **UI Hijacking:** Using `WS_EX_TOPMOST` and `WS_POPUP` to override the Windows Desktop.
* **Input Blocking:** Testing the limitations of the `BlockInput` API.
* **Kernel-Level Interaction:** Triggering a controlled System Crash (BSOD) via `NtRaiseHardError` in `ntdll.dll`.
* **Persistence:** Demonstrating how software survives a reboot using the `HKCU\Run` registry key.

## 🛠 Compilation (MinGW-w64)
To build the binary without a console window and with static linking:
```bash
g++ winlocker.cpp -o SecurityTest.exe -mwindows -luser32 -ladvapi32 -lkernel32 -lwininet -static -s
