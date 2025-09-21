
<div align="right">
  <details>
    <summary >🌐 Language</summary>
    <div>
      <div align="center">
        <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=en">English</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=zh-CN">简体中文</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=zh-TW">繁體中文</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=ja">日本語</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=ko">한국어</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=hi">हिन्दी</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=th">ไทย</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=fr">Français</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=de">Deutsch</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=es">Español</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=it">Italiano</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=ru">Русский</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=pt">Português</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=nl">Nederlands</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=pl">Polski</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=ar">العربية</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=fa">فارسی</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=tr">Türkçe</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=vi">Tiếng Việt</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=id">Bahasa Indonesia</a>
        | <a href="https://openaitx.github.io/view.html?user=Koromix&project=koffi&lang=as">অসমীয়া</
      </div>
    </div>
  </details>
</div>

<a href="https://buymeacoffee.com/koromix" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="41" width="174"></a>

# Overview

Koffi is a fast and easy-to-use C FFI module for Node.js, featuring:

* Low-overhead and fast performance (see [benchmarks](https://koffi.dev/benchmarks))
* Support for primitive and aggregate data types (structs and fixed-size arrays), both by reference (pointer) and by value
* Javascript functions can be used as C callbacks (since 1.2.0)
* Well-tested code base for popular OS/architecture combinations

The following combinations of OS and architectures __are officially supported and tested__ at the moment:

ISA / OS           | Windows     | Linux    | macOS       | FreeBSD     | OpenBSD
------------------ | ----------- | -------- | ----------- | ----------- | --------
x86 (IA32) [^1]    | ✅ Yes      | ✅ Yes   | ⬜️ *N/A*    | ✅ Yes      | ✅ Yes
x86_64 (AMD64)     | ✅ Yes      | ✅ Yes   | ✅ Yes      | ✅ Yes      | ✅ Yes
ARM32 LE [^2]      | ⬜️ *N/A*    | ✅ Yes   | ⬜️ *N/A*    | 🟨 Probably | 🟨 Probably
ARM64 (AArch64) LE | ✅ Yes      | ✅ Yes   | ✅ Yes      | ✅ Yes      | 🟨 Probably
RISC-V 64 [^3]     | ⬜️ *N/A*    | ✅ Yes   | ⬜️ *N/A*    | 🟨 Probably | 🟨 Probably

[^1]: The following call conventions are supported: cdecl, stdcall, MS fastcall, thiscall.
[^2]: The prebuilt binary uses the hard float ABI and expects a VFP coprocessor. Build from source to use Koffi with a different ABI (softfp, soft).
[^3]: The prebuilt binary uses the LP64D (double-precision float) ABI. The LP64 ABI is supported in theory if you build Koffi from source but this is untested. The LP64F ABI is not supported.

Use the following links for more information:

- Documentation: https://koffi.dev/
- Changelog: https://koffi.dev/changelog
- Source code: https://codeberg.org/Koromix/rygel/ (see below for an explanation)

# Source code

This repository does not contain the code of Koffi but only exists as a front. For pratical reasons, I've started using a single repository for all my projects in 2018 because it is easier to manage.

The source code is available here: https://codeberg.org/Koromix/rygel/ (in the *src/koffi* subdirectory).

Monorepositories have two killer features for me:

* Cross-project refactoring
* Simplified dependency management

You can find a more detailed rationale here: https://danluu.com/monorepo/

# Build manually

Koffi is built with a custom CMake-wrapper called CNoke, which also lives in the monorepository. Don't try to run CMake manually because it will fail.

Follow the [documented build instructions](https://koffi.dev/contribute#build-from-source) to build Koffi from source.

# License

This program is free software: you can redistribute it and/or modify it under the terms of the **MIT License**.

Find more information here: https://choosealicense.com/licenses/mit/
