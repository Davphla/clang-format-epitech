# Clang-Format Configuration

This repository contains a `.clang-format` configuration file for formatting C, C++, and other related source code files. This file can be used with various editors and IDEs to ensure consistent code style across your projects.
 
## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
  - [Visual Studio Code (VSCode)](#visual-studio-code-vscode)
  - [Emacs](#emacs)
  - [Neovim (nvim)](#neovim-nvim)
  - [Command Line](#command-line)
- [Customizing the Configuration](#customizing-the-configuration)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Ensure you have `clang-format` installed. You can install it via your package manager:
   - **Ubuntu**: `sudo apt install clang-format`
   - **macOS**: `brew install clang-format`
   - **Arch**: `sudo pacman -S clang`
   - **Other**: Download from the [LLVM releases page](https://releases.llvm.org/download.html).

2. Copy the .clang-format file to your project root for consistency with your teammates, or to your home directory (~) for global use.

```bash
   curl -o ~/.clang-format https://raw.githubusercontent.com/Davphla/clang-format-epitech/refs/heads/main/.clang-format
```
## Usage

### Visual Studio Code (VSCode)

1. Install the **C/C++** extension from the Extensions Marketplace.
2. Open your workspace settings and change (if needed) the following configuration in settings:
   ```json
   {
       "C_Cpp.clang_format_style": "file"
   }
   ```
3. Now, you can use `Ctrl + Shift + I` to format the current document. 
3. Or you can also format your code using the command palette (`Ctrl + Shift + P`) and typing `Format Document`.

### Emacs

1. Install the `clang-format` package if you haven't already.
2. Add the following to your Emacs configuration file (`.emacs` or `init.el`):
   ```elisp
   (require 'clang-format)
   (global-set-key (kbd "C-c C-f") 'clang-format-region)
   ```
3. You can format the current region or buffer by using `C-c C-f`.

### Neovim (nvim)

1. Install the `clang-format` plugin using your preferred plugin manager (e.g., `vim-plug`):
   ```vim
   Plug ("sbdchd/neoformat")
   ```
2. Add the following configuration to your `init.vim` or `init.lua`:
   ```vim
   vim.cmd("autocmd FileType c,cpp setlocal formatprg=clang-format")
   ```
3. You can format your code by running `:Neoformat`.

### Command Line

You can also use `clang-format` directly from the command line. Navigate to your project directory and run:
```bash
clang-format -i <filename>
```
Replace `<filename>` with the name of the file you want to format. The `-i` flag edits the file in place.

## Customizing the Configuration

You can customize the `.clang-format` file to suit your coding style preferences. Refer to the [Clang-Format Style Options](https://clang.llvm.org/docs/ClangFormatStyleOptions.html) for a comprehensive list of available options. 

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue if you have suggestions or improvements.

---

Feel free to modify this README to better fit your project's needs!
