
# TMUX – Notes, Commands & Configuration

## 📺 Reference Video
- https://www.youtube.com/watch?v=GH3kpsbbERo

---

## ▶ Outside Terminal Commands (Shell)

### Start tmux
```bash
tmux
````

### Attach to a session

```bash
tmux attach -t 3
tmux attach -t <session_name>
```

### Kill a specific session

```bash
tmux kill-session -t <session_name>
```

### Kill all tmux sessions

```bash
tmux kill-server
```

### Count number of tmux sessions

```bash
tmux ls | wc -l
```

### List all tmux sessions

```bash
tmux ls
```

---

## ▶ Inside TMUX Commands

**Prefix key:** `Ctrl + b`

### 🪟 Basic Actions

| Action             | Keys               |
| ------------------ | ------------------ |
| New window         | `Ctrl + b c`       |
| Split vertically   | `Ctrl + b %`       |
| Split horizontally | `Ctrl + b "`       |
| Switch pane        | `Ctrl + b` + Arrow |
| Close pane         | `exit`             |
| Detach session     | `Ctrl + b d`       |

---

### 🔁 Session Management

* **Reattach session**

```bash
tmux attach
```

* **List sessions**

```
Ctrl + b → s
```

Use arrow keys → `Enter`

* **Rename session**

```
Ctrl + b → $
```

* **Command prompt (bottom pane)**

```
Ctrl + b → :
```

* Press `Tab` for options
* Type `exit` to terminate

---

### 🪟 Window & Pane Navigation

* **Create new window**

```
Ctrl + b → c
```

* **Next / Previous window**

```
Ctrl + b → n
Ctrl + b → p
```

* **List windows**

```
Ctrl + b → w
```

* **Zoom current pane**

```
Ctrl + b → Z
```

Hierarchy:

```
Session → Windows → Panes
```

---

## ⚙ tmux Configuration

### Edit tmux config

```bash
nano ~/.tmux.conf
```

### Reload config (no restart needed)

```bash
tmux source ~/.tmux.conf
```

---

## 📄 Sample ~/.tmux.conf

```tmux
# Enable mouse support
set -g mouse on

# Faster command sequence
set -sg escape-time 0

# Use vim-style keys in copy mode
setw -g mode-keys vi

# Better colors
set -g default-terminal "screen-256color"

# Split shortcuts
bind | split-window -h
bind - split-window -v
unbind '"'
unbind %

# Reload config
bind r source-file ~/.tmux.conf \; display-message "tmux reloaded"

# Status bar
set -g status-bg black
set -g status-fg white
```

---

## ✅ Best Practices

* Detach (`Ctrl + b d`) instead of closing terminals
* Use **one session per project**
* Name sessions clearly (`cpp`, `infra`, `notes`)
* Reload config instead of restarting tmux
* Keep configuration minimal

---

## 🧠 Mental Model

* **Session** → Workspace
* **Window** → Tabs
* **Pane** → Splits

