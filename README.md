# Assembly x86 Windows Learning Repository

Welcome! This repository is dedicated to learning **x86 Assembly language** for **Windows** systems. Whether you're a beginner or looking to deepen your understanding of low-level programming, this repository will serve as your hands-on practice ground.

## 📚 About This Repository

This repository contains examples, exercises, and projects focused on x86 Assembly programming for Windows. The goal is to understand how computers work at the lowest level, including CPU instructions, memory management, registers, and system calls.

## 🛠️ Development Environment

### Required Tools

- **IDE**: [Visual Studio 2022](https://visualstudio.microsoft.com/vs/)
- **Extension**: [VsVim](https://marketplace.visualstudio.com/items?itemName=JaredParMSFT.VsVim) - Vim emulation layer for Visual Studio
- **Assembler**: MASM (Microsoft Macro Assembler) - included with Visual Studio
- **OS**: Windows (x86 or x64)

### Setting Up Visual Studio 2022

1. **Download and Install Visual Studio 2022**
   - Visit [Visual Studio Downloads](https://visualstudio.microsoft.com/downloads/)
   - Download the Community (free), Professional, or Enterprise edition

2. **Install Required Components**
   - During installation, select the **"Desktop development with C++"** workload
   - This includes MASM (Microsoft Macro Assembler) which is necessary for assembling x86 code
   - Under Individual Components, ensure these are selected:
     - `MSVC v143 - VS 2022 C++ x64/x86 build tools`
     - `C++ ATL for latest v143 build tools (x86 & x64)`

3. **Install VsVim Extension**
   - Open Visual Studio 2022
   - Go to `Extensions` → `Manage Extensions`
   - Search for "VsVim"
   - Click `Download` and restart Visual Studio to complete the installation
   - Alternative: Download from [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=JaredParMSFT.VsVim)

### Creating an Assembly Project

1. Open Visual Studio 2022
2. Create a new project: `File` → `New` → `Project`
3. Select `Empty Project` (C++)
4. Configure your project name and location
5. Add a new `.asm` file to your project
6. Configure build settings:
   - Right-click your `.asm` file → `Properties`
   - Set `Item Type` to `Microsoft Macro Assembler`

## 🚀 Getting Started

### Your First Assembly Program

Here's a simple "Hello World" example for Windows x86 Assembly:

```asm
; Simple Windows x86 Assembly Program
.386
.model flat, stdcall
option casemap:none

include \masm32\include\windows.inc
include \masm32\include\kernel32.inc
include \masm32\include\masm32.inc

includelib \masm32\lib\kernel32.lib
includelib \masm32\lib\masm32.lib

.data
    msg db "Hello, Assembly World!", 0

.code
start:
    invoke StdOut, addr msg
    invoke ExitProcess, 0
end start
```

### Building and Running

1. Set your build configuration to `Debug` or `Release`
2. Press `F7` or go to `Build` → `Build Solution`
3. Press `Ctrl+F5` to run without debugging or `F5` to debug
4. For VsVim users: Use `:make` to build from command mode

## 📖 Learning Resources

### x86 Assembly Basics

- **Registers**: EAX, EBX, ECX, EDX, ESI, EDI, EBP, ESP, EIP
- **Segments**: CS (Code), DS (Data), SS (Stack), ES (Extra)
- **Instructions**: MOV, ADD, SUB, MUL, DIV, JMP, CALL, RET, PUSH, POP
- **Flags**: Zero Flag (ZF), Carry Flag (CF), Sign Flag (SF), Overflow Flag (OF)

### Recommended Learning Materials

#### Books
- "Assembly Language for x86 Processors" by Kip Irvine
- "Programming from the Ground Up" by Jonathan Bartlett
- "The Art of Assembly Language" by Randall Hyde

#### Online Resources
- [Intel® 64 and IA-32 Architectures Software Developer Manuals](https://software.intel.com/content/www/us/en/develop/articles/intel-sdm.html)
- [MASM Documentation](https://docs.microsoft.com/en-us/cpp/assembler/masm/masm-for-x64-ml64-exe)
- [x86 Instruction Set Reference](https://www.felixcloutier.com/x86/)
- [OSDev Wiki](https://wiki.osdev.org/Main_Page)

#### Video Tutorials
- Search for "x86 Assembly tutorial" on YouTube
- Davy Wybiral's Assembly Language Programming series
- HackUCF's x86 Assembly course

## 📂 Repository Structure

```
Assembly/
├── README.md          # This file
├── examples/          # Example programs (coming soon)
├── exercises/         # Practice exercises (coming soon)
└── projects/          # Larger projects (coming soon)
```

## 🎯 Learning Path

1. **Basics**
   - Understand CPU architecture and registers
   - Learn basic instructions (MOV, ADD, SUB)
   - Practice with simple arithmetic operations

2. **Control Flow**
   - Conditional jumps (JE, JNE, JG, JL, etc.)
   - Loops and iterations
   - Procedures and function calls

3. **Memory Management**
   - Stack operations
   - Heap allocation
   - Memory addressing modes

4. **Windows API**
   - System calls
   - Windows API functions
   - Console I/O
   - File operations

5. **Advanced Topics**
   - Inline assembly in C/C++
   - Optimization techniques
   - Reverse engineering basics

## 💡 VsVim Tips

VsVim brings Vim keybindings to Visual Studio. Here are some useful commands:

- `i` - Enter insert mode
- `Esc` - Return to normal mode
- `dd` - Delete line
- `/pattern` - Search for pattern
- `:%s/old/new/g` - Replace all occurrences
- `:w` - Save file
- `:make` - Build project
- `Ctrl+]` - Go to definition
- `Ctrl+O` - Go back

Configure VsVim by editing `%USERPROFILE%\_vsvimrc`

## 🤝 Contributing

This is a personal learning repository, but if you'd like to contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-example`)
3. Commit your changes (`git commit -m 'Add new example'`)
4. Push to the branch (`git push origin feature/new-example`)
5. Open a Pull Request

## 📝 Notes

- This repository focuses on **32-bit (x86)** assembly, not 64-bit (x64)
- All examples are designed for **Windows** operating systems
- Code is written and tested using **Visual Studio 2022** with **MASM**

## 📜 License

This repository is for educational purposes. Feel free to use the code for learning.

## 🔗 Useful Links

- [Visual Studio 2022 Documentation](https://docs.microsoft.com/en-us/visualstudio/)
- [VsVim GitHub Repository](https://github.com/VsVim/VsVim)
- [MASM Reference](https://docs.microsoft.com/en-us/cpp/assembler/masm/microsoft-macro-assembler-reference)

---

Happy Learning! 🚀 Remember: Assembly is challenging but incredibly rewarding. Take it one instruction at a time!
