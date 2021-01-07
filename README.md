# Haribote OS

32 bit Operating System based on the book "30 日でできる! OS 自作入門"

## Development Environment

- OS
  - Mac OS X 10.15.7 19H2
- Homebrew 2.7.1
- Editor
  - Visual Studio Code 1.52.1
- Binary Editor
  - Visual Studio Code with its extension ["Hex Editor"](https://marketplace.visualstudio.com/items?itemName=ms-vscode.hexeditor) v1.3.0

## Requirements

Requirements to develop Haribote OS on Mac OS X

- Assembler
  - [NASM](https://github.com/netwide-assembler/nasm) version 2.15.05 compiled on Aug 29 2020
- Emulator
  - [QEMU](https://www.qemu.org/) emulator version 5.1.0
- Utilities
  - [Mtools](https://www.gnu.org/software/mtools/) (GNU mtools) 4.0.26
    - Use `mformat`, `mcopy` in Mtools to create the disk image
- Compiler
  - [i386-elf-gcc](https://github.com/nativeos/homebrew-i386-elf-toolchain)
- Linker Script
  - Use the linker script as `hrb.ld` from section "linker script for OS"("OS 用リンカスクリプト") in [this website](https://vanya.jp.net/os/haribote.html#hrb).
- C Program for converting `hankaku.txt`
  - TODO from [『30 日でできる！OS 自作入門』を macOS Catalina で実行する](https://qiita.com/noanoa07/items/8828c37c2e286522c7ee)
  - chapter 5-5
- Function `sprintf`
  - TODO from [『30 日でできる！OS 自作入門』を macOS Catalina で実行する](https://qiita.com/noanoa07/items/8828c37c2e286522c7ee)
  - chapter 5-7

## Setup

### Installation of Requirements

- Install Assembler

```sh
brew install nasm
nasm --version
# NASM version 2.15.05 compiled on Aug 29 2020
```

- Install Emulator

```sh
brew install qemu
qemu-system-i386 --version
# QEMU emulator version 5.1.0
# Copyright (c) 2003-2020 Fabrice Bellard and the QEMU Project developers
```

- Install Mtools

```sh
brew install mtools
mtools --version
# mtools (GNU mtools) 4.0.26
# configured with the following options: disable-xdf disable-vold disable-new-vold disable-debug enable-raw-term
```

- Install Compiler

```sh
brew tap nativeos/i386-elf-toolchain
brew install i386-elf-binutils i386-elf-gcc
i386-elf-gcc --version
# i386-elf-gcc (GCC) 9.2.0
# Copyright (C) 2019 Free Software Foundation, Inc.
# This is free software; see the source for copying conditions.  There is NO
# warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

### Test

TODO

<!--
Requirements のインストールが終わったら Hello World! が make run で QEMU で起動できるかをチェックできるようにする
参考：https://qiita.com/noanoa07/items/8828c37c2e286522c7ee#b-%E5%AE%9F%E8%A1%8C%E6%96%B9%E6%B3%95
-->
