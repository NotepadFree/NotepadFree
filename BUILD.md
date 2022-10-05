# 通过 Microsoft Visual Studio 构建NotepadFree

**前置要求:**

 - Microsoft Visual Studio 2022 (C/C++ Compiler, v143 toolset for win32, x64, arm64)

由一个 Visual Studio 解决方案构建的三个组件：

 - `notepad++.exe`: (包含 `libSciLexer.lib`)
 - `libScintilla.lib` : 基于 [Scintilla](https://www.scintilla.org/) 的静态库
 - `libLexilla.lib` : 基于 [Lexilla](https://www.scintilla.org/Lexilla.html) 的静态库

NotepadFree 始终使用Boost 正则表达式 PCRE 支持而不是普通 Scintilla 使用的默认 c++11 正则表达式 ECMAScript 构建。

## 构建 `notepad++.exe`:

 1. 打开 [`PowerEditor\visual.net\notepadPlus.sln`](https://github.com/NotepadFree/NotepadFree/blob/main/PowerEditor/visual.net/notepadPlus.sln)
 2. 选择配置 (Debug 或 Release) and 和平台 (x64 、 Win32 或 ARM64)
 3. 像一个普通Visual Studio项目一样构建 NotepadFree 解决方案。这也将构建依赖的 Scintilla 和 Lexilla 项目。

### 构建 `libScintilla.lib` 和 `libLexilla.lib`

这是在构建整个解决方案时自动完成的。所以通常你不需要关心这个。

# 通过MinGW-GCC构建NotepadFree

这个方案存在于源码的，gcc文件夹中，但我从未尝试过。
