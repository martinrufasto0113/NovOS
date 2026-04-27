<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:050509,30:0a0a1a,65:0d0d2b,100:00d4ff&height=210&section=header&text=🌌%20NovOS&fontSize=72&fontColor=00d4ff&animation=fadeIn&fontAlignY=42&desc=A%20Cinematic%2C%20Kernel-Driven%20Computing%20Environment%20for%20the%20Modern%20Web&descAlignY=65&descColor=7dd3fc&descSize=13" width="100%"/>

</div>

<div align="center">
  <img src="https://raw.githubusercontent.com/microsoft/fluentui-emoji/main/assets/Milky%20way/3D/milky_way_3d.png" width="110"/>
</div>

<br/>

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=16&pause=900&color=00D4FF&center=true&vCenter=true&width=860&lines=🌌+NovOS+Professional+Edition+v1.2.0-LTS;POSIX+VFS+backed+by+IndexedDB+—+True+persistence;40%2B+Integrated+Apps.+Infinite+Workspaces.;Mission+Control+%7C+Nova+AI+%7C+Aether+Design;Ctrl+%2B+Space+→+Spotlight.+Ctrl+%2B+Tab+→+Mission+Control.;The+boundary+between+web+and+OS+vanishes+here.)](https://git.io/typing-svg)

</div>

<div align="center">

[![Live Experience](https://img.shields.io/badge/Live-Experience-00d4ff?style=for-the-badge&logo=google-chrome&logoColor=white)](https://tcode-motion.github.io/NovOS/)
[![Version](https://img.shields.io/badge/Version-1.2.0--LTS-brightgreen?style=for-the-badge)](https://github.com/Tcode-Motion/NovOS)
[![Kernel Status](https://img.shields.io/badge/Kernel-Ready-blueviolet?style=for-the-badge)](https://github.com/Tcode-Motion/NovOS)
[![Architecture](https://img.shields.io/badge/Arch-POSIX--VFS-orange?style=for-the-badge)](https://github.com/Tcode-Motion/NovOS)
[![Security](https://img.shields.io/badge/Security-Verified-lightgrey?style=for-the-badge)](https://github.com/Tcode-Motion/NovOS)

</div>

<div align="center">

[![Stars](https://img.shields.io/github/stars/Tcode-Motion/NovOS?style=for-the-badge&color=00d4ff&label=⭐)](https://github.com/Tcode-Motion/NovOS/stargazers)
[![License](https://img.shields.io/badge/license-MIT-bd00ff?style=for-the-badge)](https://github.com/Tcode-Motion/NovOS)
[![Made By](https://img.shields.io/badge/Made_by-Tcode--Motion-181717?style=for-the-badge&logo=github)](https://github.com/Tcode-Motion)
[![Engine](https://img.shields.io/badge/Engine-React+Vite-61dafb?style=for-the-badge&logo=react&logoColor=white)](https://github.com/Tcode-Motion/NovOS)

</div>

---

<div align="center">

```
╔══════════════════════════════════════════════════════════════════════════╗
║                                                                          ║
║   Every shadow. Every translucent layer. Every kernel event.             ║
║   Designed to make the boundary between web and OS vanish.               ║
║   — Tcode-Motion  🌌                                                     ║
╚══════════════════════════════════════════════════════════════════════════╝
```

</div>

---

## 📖 Table of Contents

- [🌌 The Vision](#-the-vision)
- [🏗️ System Architecture](#️-system-architecture)
  - [The Micro-Kernel](#the-micro-kernel)
  - [The Virtual File System (VFS)](#the-virtual-file-system-vfs)
  - [AppLoader & Security](#apploader--security)
- [🖥️ User Interface & UX](#️-user-interface--ux)
  - [Cinematic Glassmorphism](#cinematic-glassmorphism)
  - [Spotlight Search](#spotlight-search)
  - [Mission Control](#mission-control)
  - [Workspaces](#workspaces)
- [📦 Application Ecosystem](#-application-ecosystem)
  - [Productivity Suite](#productivity-suite)
  - [System Utilities](#system-utilities)
  - [Creative & Media](#creative--media)
  - [AI Integration](#ai-integration)
- [📋 Full Application Registry](#-full-application-registry-extended)
- [⌨️ Command Line Reference](#️-command-line-reference)
- [🔐 Security & Identity](#-security--identity)
- [🛠️ Developer Guide](#️-developer-guide)
- [🛰️ Kernel Event Reference](#️-kernel-event-reference)
- [🎨 Design System Tokens](#-design-system-the-aether-tokens)
- [🚀 Roadmap & Future](#-roadmap--future)
- [🕰️ System Changelog](#️-system-changelog)
- [❓ Troubleshooting](#-troubleshooting)
- [📚 System Glossary](#-system-glossary)
- [📑 Contribution Guidelines](#-contribution-guidelines)
- [📜 License & Credits](#-license--credits)

---

## 🌌 The Vision

**NovOS** is more than just a frontend project — it is a meticulous recreation of a professional desktop environment inside the browser. Built with the goal of proving that a web-based interface can feel as responsive, powerful, and visually deep as a native operating system.

Every window shadow, every translucent material, and every kernel event is designed to immerse the user in a high-fidelity workspace where the boundary between "web page" and "operating system" vanishes.

> 🔗 **[Try the Live Experience →](https://tcode-motion.github.io/NovOS/)**

---

## 🏗️ System Architecture

NovOS follows a strictly modular architecture, separating the **Presentation Layer (React)** from the **Logic Layer (Kernel)**.

### The Micro-Kernel

The kernel is the "heart" of NovOS. It is a singleton instance that initializes during the boot sequence and manages all system resources.

- **Event Bus** — A centralized pub/sub system for inter-app communication.
- **Process Manager** — Tracks every open window as a unique process with its own PID, memory state, and priority.
- **Audio/Network Managers** — Managed subsystems that apps can tap into without direct browser API calls.

**Kernel Boot Lifecycle:**
```
kernel:booting → fs:ready → apps:init → kernel:ready
```

### The Virtual File System (VFS)

Our VFS is a full POSIX-compliant implementation backed by **IndexedDB**.

- **True Persistence** — Unlike `localStorage`, IndexedDB allows for large binary files and structured data storage that survives browser refreshes.
- **Path Resolution** — Supports absolute paths (`/etc/config`), relative paths (`../docs`), and home shortcuts (`~/desktop`).
- **Permissions** — Every file and folder has a 10-character permission string (e.g., `drwxr-xr-x`) and an owner/group assignment.

**System Paths:**
```
/bin       → Binary executables
/etc       → System configuration
/home      → User directories
/usr/apps  → Application bundles
/var/log   → System logs
/tmp       → Temporary storage
/mnt       → Mounted devices
```

**VFS Permissions Matrix:**
```
Owner (1-3): rwx   |   Group (4-6): rwx   |   Others (7-9): rwx
```

### AppLoader & Security

Applications are not just React components — they are treated as system packages.

1. **Registry** — All apps must be defined in `APP_REGISTRY` with specific dimensions and categories.
2. **Verification** — During boot, the system verifies cryptographic bundles in `/usr/apps`. If a bundle is missing or has an invalid signature, the kernel blocks the app launch.

**Application Lifetimes:**

| State | Description |
|:---|:---|
| `Idle` | Metadata loaded, bundle pending |
| `Ready` | Verified and ready to launch |
| `Running` | Active process in window manager |
| `Corrupted` | Verification failed |

---

## 🖥️ User Interface & UX

### Cinematic Glassmorphism

The design language of NovOS, titled **"Aether Design,"** focuses on:

- **Depth** — Variable blurs (8px to 32px) to signify visual hierarchy.
- **Luminance** — High-contrast text on translucent backgrounds for readability.
- **Micro-interactions** — Hover-induced glows, smooth window snapping, and magnetic dock icons.

### Spotlight Search

Accessible via `Ctrl + Space`, the Spotlight is the fastest way to navigate.

- **Fuzzy Search** — Find files and apps with minimal typing.
- **AI Integration** — Ask Nova questions directly from the search bar.
- **Quick Actions** — Type `theme light` or `theme dark` to instantly switch environments.

### Mission Control

Inspired by macOS, Mission Control (`Ctrl + Tab`) provides a bird's-eye view of all open windows. It uses a specialized layout algorithm to prevent window overlap during the overview, allowing for quick selection and workspace management.

### Workspaces

NovOS supports infinite virtual desktops. Move windows between workspaces to organize your workflow. Use the workspace switcher in the taskbar or the Mission Control overlay to jump between contexts.

---

## 📦 Application Ecosystem

### Productivity Suite

| App | Description | Key Features |
|:---|:---|:---|
| **✍️ Code Editor** | A professional IDE | Syntax highlighting, File tree, Auto-save, Multi-tab |
| **📝 Text Editor** | Lightweight notepad | Quick notes, RTF support, Local export |
| **📅 Calendar** | Event planner | Monthly view, Event reminders, System-wide sync |
| **💡 Notes** | Sticky notes | Markdown support, Color coding, Desktop pinning |
| **📈 Calculator** | Math engine | Scientific mode, History log, Unit conversion |

### System Utilities

- **📂 File Manager** — Your window into the VFS. Supports drag-and-drop, right-click context menus, and Grid/List view modes.
- **💻 Terminal** — A high-fidelity shell (`novash`). Supports piping, command history, custom aliases, and `.sh` scripting.
- **⚙️ Settings** — Deep system configuration. Change wallpapers, adjust glass opacity, manage user accounts.
- **📊 Task Manager** — Monitor active processes, kill runaway apps, view memory usage.
- **🛡️ Security Center** — Manage firewall rules and view system audit logs.

### Creative & Media

- **🎵 Music Player** — High-fidelity audio engine with visualizer support (.mp3, .wav).
- **🎬 Video Player** — Smooth playback with picture-in-picture mode.
- **🖼️ Gallery** — Image organization with metadata tagging and immersive light-box.
- **📷 Camera** — Hardware-integrated capture tool for system profile pictures.
- **🎙️ Recorder** — Capture audio directly into the VFS.

### AI Integration

- **🤖 Nova AI** — Your neural companion. Nova can read your files, help you write code, and explain system concepts. Lives in the dock, always ready.
  - `nova ask "[question]"` — Query Nova from the terminal.
  - `nova status` — Check AI engine connectivity.
  - Multi-file context analysis supported in v1.2.0.

---

## 📋 Full Application Registry (Extended)

### System Applications

| App | Description |
|:---|:---|
| **🛍️ App Store (Nexus)** | Download and update system bundles. One-click installation. |
| **📊 Task Manager** | High-level process oversight. |
| **📈 System Monitor** | Real-time CPU, memory, network, and disk I/O telemetry. |
| **👥 User Manager** | Add/remove users, modify groups, reset passwords, view last login. |
| **🎨 Theme Manager** | Real-time CSS injection. Presets: Cyberpunk, Minimalist, Arctic, Midnight. |
| **🛡️ Security Center** | Firewall rules and audit log viewer. |
| **🔄 Update Manager** | System-wide OTA update simulation. |

### Productivity & Office

| App | Description |
|:---|:---|
| **📅 Calendar** | Integrated with system time and notification center. |
| **💡 Notes** | Persistent markdown-based scratch pad. |
| **⏰ Reminders** | Time-based task tracking. |
| **👤 Contacts** | VFS-backed address book. |
| **📧 Email** | Lightweight IMAP-simulated client. |

### Utility Tools

| App | Description |
|:---|:---|
| **🧮 Calculator** | Scientific and base conversion modes. |
| **🕐 Clock** | World clock, Timer, and Stopwatch. |
| **📦 Compressor** | Zip/Unzip simulation for `.tar` and `.zip` files. |
| **⬇️ Download Manager** | Track virtual downloads from the web. |
| **📋 Clipboard** | View system-wide clipboard history. |
| **🌐 Browser (Nova Web)** | Secure sandbox browsing with bookmarks, history, and iframe isolation. |

---

## ⌨️ Command Line Reference

The NovOS Terminal (`novash`) supports 50+ built-in commands.

### File Management

| Command | Description |
|:---|:---|
| `ls [path]` | List directory contents |
| `cd [path]` | Change directory |
| `cat [file]` | View file contents |
| `mkdir [name]` | Create a new directory |
| `touch [name]` | Create an empty file |
| `rm [-r] [path]` | Remove file or directory |
| `cp [src] [dest]` | Copy files |
| `mv [src] [dest]` | Move or rename files |
| `find` | Search for files in VFS |
| `grep` | Pattern matching in files |

### System Control

| Command | Description |
|:---|:---|
| `ps` | List all active processes |
| `kill [pid]` | Terminate a process |
| `top` | Interactive process viewer |
| `uptime` | View system up-time |
| `whoami` | Display current user identity |
| `uname` | System info summary |
| `df` | View disk space usage |
| `mount` | View active filesystems |
| `clear` | Clear terminal screen |
| `help` | Show all available commands |

### Extended Shell Built-ins

| Command | Description |
|:---|:---|
| `alias` | Create command aliases |
| `export` | Set environment variables |
| `source` | Execute script in current shell |
| `history` | View command history |
| `date` | Current system time |
| `cal` | System calendar |
| `echo` | Print text to stdout |
| `sleep` | Pause execution |

### Advanced AI Commands

```bash
nova ask "[question]"   # Query the Nova AI
nova status             # Check AI engine connectivity
```

### Terminal Scripting

NovOS supports a subset of bash scripting. Create `.sh` files and run them in the VFS:

```bash
# backup.sh
echo "Starting backup..."
cp -r ~/Documents ~/Documents_Backup
echo "Backup complete at $(date)"
```

---

## 🔐 Security & Identity

NovOS is built with a multi-user mindset.

- **Root vs User** — Only users in the `root` group can modify system files in `/etc` or bundles in `/usr/apps`.
- **Identity Persistence** — User data is isolated. Logging in as `Operator` gives a desktop and VFS completely separate from `Guest`.
- **Cryptographic Bundles** — All system apps require a verified bundle in `/usr/apps` to launch. Missing or invalid signatures are blocked at boot.

**Default Admin Credentials:**

| Field | Value |
|:---|:---|
| **User** | `Operator` |
| **Pass** | `admin` |

---

## 🛠️ Developer Guide

### Project Structure

```
/src
  /components
    /apps        # Individual application components
    /os          # Core UI (Desktop, Dock, Taskbar)
    /overlays    # Global UI (Spotlight, Mission Control)
  /kernel        # The Engine (FS, AppLoader, Kernel.js)
  /store         # Global State (Zustand)
  /styles        # Global CSS and Design Tokens
```

### Adding a New App

**Step 1** — Create your component in `src/components/apps/`:

```jsx
// src/components/apps/MyApp.jsx
export default function MyApp() {
  return <div className="app-window">Hello from My App!</div>;
}
```

**Step 2** — Register the app in `src/appRegistry.js`:

```javascript
myApp: {
  title: 'My App',
  icon: 'rocket',
  category: 'Utilities',
  w: 600,
  h: 400
}
```

**Step 3** — Add a launcher to the desktop or dock in `osStore.js`.

> **Important:** Ensure your app responds to `Esc` for closing and works across all 4 workspaces.

### Using the Kernel API

You can access the kernel globally via `window.kernel` for debugging:

```javascript
// Write a file from the browser console
await window.kernel.fs.writeFile('/home/user/test.txt', 'Hello World');

// Read it back
const content = await window.kernel.fs.readFile('/home/user/test.txt');
console.log(content); // Hello World
```

### VFS Persistence Layer

The system uses a custom abstraction over IndexedDB for POSIX-like performance:

- **Batched Writes** — Multiple file operations committed in a single transaction.
- **Index-based Queries** — File searches by parent path optimized via IDB indexes.
- **Binary Support** — Images and blobs stored as `ArrayBuffer` to minimize memory overhead.

---

## 🛰️ Kernel Event Reference

The NovOS Kernel emits events that can be captured by apps or the OS itself.

| Event Name | Description | Data Payload |
|:---|:---|:---|
| `kernel:booting` | Boot sequence starts | None |
| `kernel:ready` | All systems (FS, Apps, Net) are online | `{ bootTime: number }` |
| `fs:ready` | IndexedDB connection established | None |
| `os:error` | Critical system error | `{ title: string, message: string }` |
| `window:focus` | User focuses a specific window | `{ id: string, app: string }` |
| `battery:change` | Device battery level updates | `{ level: number, charging: boolean }` |
| `network:change` | System goes online/offline | `{ online: boolean }` |

### System Daemons

| Daemon | Description |
|:---|:---|
| `novad` | AI background services |
| `fsd` | Filesystem sync daemon |
| `netd` | Connection monitor |
| `audiod` | Global sound engine |

---

## 🎨 Design System: The Aether Tokens

For developers styling custom apps, use the following CSS variables defined in `:root`:

### Surface Tokens

```css
--bg-primary        /* Main background (deep black) */
--glass-material    /* Translucent background for windows */
--glass-stroke      /* 1px border for glass edges */
--glass-shadow      /* Multi-layered drop shadow for depth */
--glass-bg          /* rgba(255, 255, 255, 0.05) */
--glass-border      /* rgba(255, 255, 255, 0.1) */
--blur-standard     /* 24px */
```

### Typography Tokens

```css
--font-main         /* Inter Variable */
--font-mono         /* JetBrains Mono (simulated) */
--text-heading      /* Bold, high-luminance white */
--text-body         /* Medium-luminance gray */
--text-primary      /* Optimized for dark backgrounds */
```

### Interaction & Accent Tokens

```css
--accent-cyan       /* #00d4ff — Default primary */
--accent-purple     /* #bd00ff — Secondary accent */
--accent-primary    /* #00d4ff */
--accent-glow       /* Primary branding glow */
--hover-glow        /* Radial gradient for hover effects */
--active-scale      /* 0.98 for tap feedback */
```

### Design Principles

| Principle | Value |
|:---|:---|
| Blur Saturation | 0.8 |
| Borders | 1px solid rgba(255,255,255,0.1) |
| Typography | Inter (Variable) |
| Overlays | Linear-to-Radial Glow |
| Material Opacity | 0.0 to 1.0 (configurable) |

---

## 🚀 Roadmap & Future

### ✅ v2.0 (Current)

- [x] Persistent VFS via IndexedDB
- [x] 40+ Integrated Apps
- [x] Multi-workspace support
- [x] Real Terminal (`novash`) & Code Editor (Monaco-powered)
- [x] Nova AI with multi-file context
- [x] Cryptographic bundle verification
- [x] Mission Control window overview

### 🔭 v3.0 (Planned)

- [ ] **Native File System Access** — Sync your local machine folders with NovOS
- [ ] **Extension API** — Allow developers to load third-party app bundles dynamically
- [ ] **Multiplayer Mode** — Collaborate on the same VFS with friends via WebRTC
- [ ] **Mobile Experience** — A specialized "Mobile Deck" UI for tablet users

---

## 🕰️ System Changelog

### v1.2.0 — Latest

- **Security** — Implemented cryptographic bundle verification for all apps
- **Performance** — Optimized VFS transaction batching by 40%
- **UX** — Added "Mission Control" window overview mode (`Ctrl + Tab`)
- **AI** — Nova now supports multi-file context analysis

### v1.1.0

- **Feature** — Added Virtual File System (VFS) with IndexedDB persistence
- **UI** — Introduced dynamic glassmorphism and the Aether theme engine
- **App** — Released "Code Editor" with full syntax highlighting

### v1.0.0

- **Initial Release** — Core kernel and basic window manager

---

## ❓ Troubleshooting

**VFS is corrupted or slow?**
Run this command in the terminal to perform a full system reset:
```bash
rm -rf /
```
Then refresh the page. The default filesystem will be re-populated automatically.

**App won't open?**
Ensure you have administrative privileges. Some system apps require a verified Security Bundle. Check the browser console for `[AppLoader] Security Violation` messages.

**Performance issues?**
NovOS is visually intensive. Go to **Settings > Personalization** and disable "Window Animations" to improve performance on older machines.

---

## 📚 System Glossary

| Term | Definition |
|:---|:---|
| **Aether Design** | The proprietary design language of NovOS, focusing on layered glassmorphism. |
| **Bootloader** | The sequence in `Kernel.js` that coordinates VFS mounting and app initialization. |
| **Bundle** | A cryptographic security token stored in `/usr/apps` required to launch system apps. |
| **Context** | The user identity (uid/gid) passed to FS operations to verify permissions. |
| **Event Bus** | The internal communication channel for system-wide notifications and inter-app messages. |
| **PID** | Process Identifier — a unique integer assigned to every active window or background service. |
| **VFS** | Virtual File System — the IndexedDB-backed abstraction layer that mimics a real disk. |
| **Workspace** | A virtual desktop container that holds a specific set of windows. |
| **novash** | The NovOS shell — the command-line interface powering the Terminal app. |
| **Nova** | The built-in AI assistant integrated throughout the OS. |

---

## 📑 Contribution Guidelines

We welcome contributions to the NovOS ecosystem!

1. **Fork the Repo** — Create your own branch for features.
2. **Coding Standards** — Follow the "Aether" design guidelines for all UI components.
3. **Kernel Integrity** — Do not modify `Kernel.js` without a verified PR.
4. **Testing** — Ensure your app works across all 4 workspaces and responds to `Esc` for closing.

---

## 📜 License & Credits

NovOS is licensed under the **MIT License**.

- **Icons** — [Fluent Emoji](https://github.com/microsoft/fluentui-emoji) by Microsoft
- **Typography** — [Inter](https://rsms.me/inter/) by Rasmus Andersson
- **Engine** — [React](https://reactjs.org/) + [Vite](https://vitejs.dev/)

---

## 👨‍💻 Made by Tcode-Motion

<div align="center">

| 🔥 Project | 📖 Description |
|:---|:---|
| 🌌 **NovOS** | A cinematic web OS — POSIX VFS, Nova AI, Aether Design |
| 🐉 **TechScript** | A programming language — Native Rust VM + web builder |
| 🧠 **Project JARVIS** | Personal AI assistant built in Python |
| 🎨 **3D Visuals** | WebGL particle systems + Three.js experiences |
| 🤖 **AR Keyboard** | Hand-gesture virtual keyboard with OpenCV + MediaPipe |

[![GitHub](https://img.shields.io/badge/GitHub-Tcode--Motion-181717?style=for-the-badge&logo=github)](https://github.com/Tcode-Motion)
[![YouTube](https://img.shields.io/badge/YouTube-@sachkaswitch-FF0000?style=for-the-badge&logo=youtube)](https://youtube.com/@sachkaswitch)
[![Live Demo](https://img.shields.io/badge/Live-NovOS-00d4ff?style=for-the-badge&logo=google-chrome&logoColor=white)](https://tcode-motion.github.io/NovOS/)

*"The future of computing is not on your disk, but in your mind."*

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00d4ff,40:0d0d2b,80:0a0a1a,100:050509&height=140&section=footer&text=🌌%20NovOS%20—%20The%20Web%20OS&fontSize=22&fontColor=00d4ff&animation=fadeIn&fontAlignY=62" width="100%"/>

</div>
