
# Neovim (nvim) – Basic Useful Commands & Shortcuts

---

## 🚀 Starting & Exiting Neovim

### Open files
```bash
nvim file.txt
nvim .
````

### Exit commands

| Action               | Command |
| -------------------- | ------- |
| Quit                 | `:q`    |
| Save & quit          | `:wq`   |
| Force quit (no save) | `:q!`   |
| Save                 | `:w`    |

---

## 🧠 Modes in Neovim

| Mode         | Key        |
| ------------ | ---------- |
| Normal mode  | `Esc`      |
| Insert mode  | `i`        |
| Visual mode  | `v`        |
| Visual line  | `V`        |
| Visual block | `Ctrl + v` |
| Command mode | `:`        |

---

## ✍️ Insert Mode Shortcuts

| Action               | Key |
| -------------------- | --- |
| Insert at cursor     | `i` |
| Insert at line start | `I` |
| Insert at line end   | `A` |
| New line below       | `o` |
| New line above       | `O` |

---

## 🧭 Navigation

### Basic movement

| Action | Key |
| ------ | --- |
| Left   | `h` |
| Down   | `j` |
| Up     | `k` |
| Right  | `l` |

### Faster movement

| Action         | Key  |
| -------------- | ---- |
| Word forward   | `w`  |
| Word backward  | `b`  |
| End of word    | `e`  |
| Line start     | `0`  |
| Line end       | `$`  |
| Top of file    | `gg` |
| Bottom of file | `G`  |

---

## 📋 Copy, Cut, Paste

| Action            | Key  |
| ----------------- | ---- |
| Copy (yank) line  | `yy` |
| Copy selection    | `y`  |
| Paste below       | `p`  |
| Paste above       | `P`  |
| Cut (delete) line | `dd` |
| Cut selection     | `d`  |

---

## ↩ Undo / Redo

| Action | Key        |
| ------ | ---------- |
| Undo   | `u`        |
| Redo   | `Ctrl + r` |

---

## 🔍 Search & Replace

### Search

| Action          | Key     |
| --------------- | ------- |
| Search forward  | `/text` |
| Search backward | `?text` |
| Next match      | `n`     |
| Previous match  | `N`     |

### Replace

```vim
:%s/old/new/g
```

---

## 🧱 Working with Lines

| Action         | Key        |
| -------------- | ---------- |
| Delete line    | `dd`       |
| Duplicate line | `yy` → `p` |
| Join lines     | `J`        |
| Indent right   | `>>`       |
| Indent left    | `<<`       |

---

## 🪟 Windows & Splits

| Action           | Key          |
| ---------------- | ------------ |
| Horizontal split | `:split`     |
| Vertical split   | `:vsplit`    |
| Switch window    | `Ctrl + w w` |
| Close window     | `Ctrl + w q` |

---

## 📁 Buffers (Open Files)

| Action          | Command         |
| --------------- | --------------- |
| List buffers    | `:ls`           |
| Next buffer     | `:bnext`        |
| Previous buffer | `:bprev`        |
| Open buffer     | `:buffer <num>` |
| Close buffer    | `:bd`           |

---

## 🧪 Useful Neovim Commands

| Action               | Command    |
| -------------------- | ---------- |
| Reload file          | `:e`       |
| File info            | `Ctrl + g` |
| Show command history | `q:`       |
| Run shell command    | `:!ls`     |

---

## ⚙ Helpful Defaults (Recommended)

Add to `~/.config/nvim/init.lua`:

```lua
vim.opt.number = true
vim.opt.relativenumber = true
vim.opt.wrap = false
vim.opt.expandtab = true
vim.opt.shiftwidth = 4
vim.opt.tabstop = 4
vim.opt.clipboard = "unnamedplus"
```

---

## 🧠 Mental Model

* **Normal mode** → navigation & commands
* **Insert mode** → typing
* **Visual mode** → selection

> Stay in **Normal mode** as much as possible.

---

## ✅ Must-remember shortcuts

* `Esc` → Always go back to normal
* `:wq` → Save & quit
* `dd` → Delete line
* `yy` → Copy line
* `/` → Search
* `u` → Undo

---

