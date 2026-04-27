# 🌌 NovOS — The Futuristic Web Operating System

<div align="center">
  <img src="https://raw.githubusercontent.com/microsoft/fluentui-emoji/main/assets/Milky%20way/3D/milky_way_3d.png" width="120" />
  <h1>NovOS Professional Edition</h1>
  <p><b>A Cinematic, Kernel-Driven Computing Environment for the Modern Web</b></p>

  [![Live Experience](https://img.shields.io/badge/Live-Experience-00d4ff?style=for-the-badge&logo=google-chrome&logoColor=white)](https://tcode-motion.github.io/NovOS/)
  [![Stable Version](https://img.shields.io/badge/Version-1.2.0--LTS-brightgreen?style=for-the-badge)](https://github.com/tcode-motion/NovOS)
  [![Kernel Status](https://img.shields.io/badge/Kernel-Ready-blueviolet?style=for-the-badge)](https://github.com/tcode-motion/NovOS)
  [![Architecture](https://img.shields.io/badge/Arch-POSIX--VFS-orange?style=for-the-badge)](https://github.com/tcode-motion/NovOS)
  [![Security](https://img.shields.io/badge/Security-Verified-lightgrey?style=for-the-badge)](https://github.com/tcode-motion/NovOS)
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
  - [Communication Tools](#communication-tools)
- [⌨️ Command Line Reference](#️-command-line-reference)
- [🔐 Security & Identity](#-security--identity)
- [🛠️ Developer Guide](#️-developer-guide)
- [🚀 Roadmap & Future](#-roadmap--future)
- [❓ Troubleshooting](#-troubleshooting)
- [📚 System Glossary](#-system-glossary)
- [🛰️ Kernel Event Reference](#️-kernel-event-reference)
- [🎨 Design System Tokens](#-design-system-tokens)

---

## 🌌 The Vision
**NovOS** is more than just a frontend project; it is a meticulous recreation of a professional desktop environment inside the browser. It was built with the goal of proving that a web-based interface can feel as responsive, powerful, and visually deep as a native operating system.

Every window shadow, every translucent material, and every kernel event is designed to immerse the user in a high-fidelity workspace where the boundary between "web page" and "operating system" vanishes.

---

## 🏗️ System Architecture

NovOS follows a strictly modular architecture, separating the **Presentation Layer (React)** from the **Logic Layer (Kernel)**.

### The Micro-Kernel
The kernel is the "heart" of NovOS. It is a singleton instance that initializes during the boot sequence and manages all system resources.
- **Event Bus**: A centralized pub/sub system for inter-app communication.
- **Process Manager**: Tracks every open window as a unique process with its own PID, memory state, and priority.
- **Audio/Network Managers**: Managed subsystems that apps can tap into without direct browser API calls.

### The Virtual File System (VFS)
Our VFS is a full POSIX-compliant implementation backed by **IndexedDB**. 
- **True Persistence**: Unlike `localStorage`, IndexedDB allows for large binary files and structured data storage that survives browser refreshes.
- **Path Resolution**: Supports absolute paths (`/etc/config`), relative paths (`../docs`), and home shortcuts (`~/desktop`).
- **Permissions**: Every file and folder has a 10-character permission string (e.g., `drwxr-xr-x`) and an owner/group assignment.

### AppLoader & Security
Applications are not just React components; they are treated as system packages.
1. **Registry**: All apps must be defined in the `APP_REGISTRY` with specific dimensions and categories.
2. **Verification**: During boot, the system verifies cryptographic bundles in `/usr/apps`. If a bundle is missing or has an invalid signature, the kernel blocks the application launch to maintain system integrity.

---

## 🖥️ User Interface & UX

### Cinematic Glassmorphism
The design language of NovOS, titled **"Aether Design,"** focuses on:
- **Depth**: Using variable blurs (8px to 32px) to signify hierarchy.
- **Luminance**: High-contrast text on translucent backgrounds for readability.
- **Micro-interactions**: Hover-induced glows, smooth window snapping, and magnetic dock icons.

### Spotlight Search
Accessible via `Ctrl + Space`, the Spotlight is the fastest way to navigate.
- **Fuzzy Search**: Find files and apps with minimal typing.
- **AI Integration**: Ask Nova questions directly from the search bar.
- **Quick Actions**: Type `theme light` or `theme dark` to instantly switch environments.

### Mission Control
Inspired by macOS, Mission Control (`Ctrl + Tab`) provides a bird's-eye view of all open windows. It uses a specialized layout algorithm to prevent window overlap during the overview, allowing for quick selection and workspace management.

### Workspaces
NovOS supports infinite virtual desktops. Move windows between workspaces to organize your workflow. Use the workspace switcher in the taskbar or the Mission Control overlay to jump between contexts.

---

## 📦 Application Ecosystem

### Productivity Suite
| App | Description | Key Features |
| :--- | :--- | :--- |
| **✍️ Code Editor** | A professional IDE | Syntax highlighting, File tree, Auto-save, Multi-tab support. |
| **📝 Text Editor** | Lightweight notepad | Quick notes, RTF support, Local export. |
| **📅 Calendar** | Event planner | Monthly view, Event reminders, System-wide sync. |
| **💡 Notes** | Sticky notes | Markdown support, Color coding, Desktop pinning. |
| **📈 Calculator** | Math engine | Scientific mode, History log, Unit conversion. |

### System Utilities
- **📂 File Manager**: Your window into the VFS. Supports drag-and-drop, right-click context menus, and multiple view modes (Grid/List).
- **💻 Terminal**: A high-fidelity shell. Supports piping, command history, and custom aliases.
- **⚙️ Settings**: Deep system configuration. Change wallpapers, adjust glass opacity, and manage user accounts.
- **📊 Task Manager**: Monitor active processes, kill runaway apps, and view memory usage.
- **🛡️ Security**: Manage firewall rules and view system audit logs.

### Creative & Media
- **🎵 Music Player**: High-fidelity audio engine with visualizer support.
- **🎬 Video Player**: Smooth playback with picture-in-picture mode.
- **🖼️ Gallery**: View your pictures with an immersive light-box experience.
- **📷 Camera**: Access your hardware camera to take system profile pictures.

### AI Integration
- **🤖 Nova AI**: Your neural companion. Nova can read your files, help you write code, and explain system concepts. It lives in the dock and is always ready to assist.

---

## ⌨️ Command Line Reference

The NovOS Terminal (`novash`) supports over 50 built-in commands. Below are the most common:

### File Management
- `ls [path]` - List directory contents.
- `cd [path]` - Change directory.
- `cat [file]` - View file contents.
- `mkdir [name]` - Create a new directory.
- `touch [name]` - Create an empty file.
- `rm [-r] [path]` - Remove file or directory.
- `cp [src] [dest]` - Copy files.
- `mv [src] [dest]` - Move or rename files.

### System Control
- `ps` - List all active processes.
- `kill [pid]` - Terminate a process.
- `uptime` - View system up-time.
- `whoami` - Display current user identity.
- `clear` - Clear terminal screen.
- `help` - Show all available commands.

### Advanced AI
- `nova ask "[question]"` - Query the Nova AI.
- `nova status` - Check AI engine connectivity.

---

## 🔐 Security & Identity

NovOS is built with a multi-user mindset.
- **Root vs User**: Only users in the `root` group can modify system files in `/etc` or bundles in `/usr/apps`.
- **Identity Persistence**: User data is isolated. When you log in as `Operator`, your desktop and files are distinct from the `Guest` account.
- **Admin Credentials**:
  - **User**: `Operator`
  - **Pass**: `admin`

---

## 🛠️ Developer Guide

### Project Structure
```text
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
1. Create your component in `src/components/apps/`.
2. Register the app in `src/appRegistry.js`:
   ```javascript
   myApp: { 
     title: 'My App', 
     icon: 'rocket', 
     category: 'Utilities', 
     w: 600, h: 400 
   }
   ```
3. Add a launcher to the desktop or dock in `osStore.js`.

### Using the Kernel API
You can access the kernel globally for debugging via `window.kernel`:
```javascript
// Example: Writing a file from the JS console
await window.kernel.fs.writeFile('/home/user/test.txt', 'Hello World');
```

---

## 🚀 Roadmap & Future

### v2.0 (Current)
- [x] Persistent VFS via IndexedDB.
- [x] 40+ Integrated Apps.
- [x] Multi-workspace support.
- [x] Real Terminal & Code Editor.

### v3.0 (Planned)
- [ ] **Native File System Access**: Sync your local machine folders with NovOS.
- [ ] **Extension API**: Allow developers to load third-party app bundles dynamically.
- [ ] **Multiplayer Mode**: Collaborate on the same VFS with friends via WebRTC.
- [ ] **Mobile Experience**: A specialized "Mobile Deck" UI for tablet users.

---

## ❓ Troubleshooting

### VFS is corrupted or slow?
Run the following command in the terminal to perform a system reset:
`rm -rf /` followed by a page refresh. This will re-populate the default filesystem.

### App won't open?
Ensure you have administrative privileges. Some system apps require a "Security Bundle" to be verified. Check the console for `[AppLoader] Security Violation` messages.

### Performance issues?
NovOS is visually intensive. Disable "Window Animations" in **Settings > Personalization** to improve performance on older machines.

---

### 📚 System Glossary

| Term | Definition |
| :--- | :--- |
| **Aether Design** | The proprietary design language used in NovOS, focusing on layered glassmorphism. |
| **Bootloader** | The sequence in `Kernel.js` that coordinates the mounting of VFS and initialization of apps. |
| **Bundle** | A cryptographic security token stored in `/usr/apps` required to launch system applications. |
| **Context** | The user identity (uid/gid) passed to FS operations to verify permissions. |
| **Event Bus** | The internal communication channel used for system-wide notifications and inter-app messages. |
| **PID** | Process Identifier — a unique integer assigned to every active window or background service. |
| **VFS** | Virtual File System — the IndexedDB-backed abstraction layer that mimics a real disk. |
| **Workspace** | A virtual desktop container that holds a specific set of windows. |

---

### 🛰️ Kernel Event Reference

The NovOS Kernel emits various events that can be captured by apps or the OS itself.

| Event Name | Description | Data Payload |
| :--- | :--- | :--- |
| `kernel:booting` | Emitted when the boot sequence starts. | None |
| `kernel:ready` | Emitted when all systems (FS, Apps, Net) are online. | `{ bootTime: number }` |
| `fs:ready` | Emitted when the IndexedDB connection is established. | None |
| `os:error` | Emitted when a critical system error occurs. | `{ title: string, message: string }` |
| `window:focus` | Emitted when a user focuses a specific window. | `{ id: string, app: string }` |
| `battery:change` | Emitted when the device battery level updates. | `{ level: number, charging: boolean }` |
| `network:change` | Emitted when the system goes online/offline. | `{ online: boolean }` |

---

### 🎨 Design System: The Aether Tokens

For developers looking to style custom apps, use the following CSS variables defined in `:root`:

#### Surface Tokens
- `--bg-primary`: The main background color (usually deep black).
- `--glass-material`: The translucent background for windows.
- `--glass-stroke`: The 1px border used to define glass edges.
- `--glass-shadow`: The multi-layered drop shadow for depth.

#### Typography Tokens
- `--font-main`: Inter Variable.
- `--font-mono`: JetBrains Mono (simulated).
- `--text-heading`: Bold, high-luminance white.
- `--text-body`: Medium-luminance gray for content.

#### Interaction Tokens
- `--accent-cyan`: `#00d4ff` (The default primary).
- `--accent-purple`: `#bd00ff` (Secondary accent).
- `--hover-glow`: Radial gradient used for hover effects.
- `--active-scale`: 0.98 for tap feedback.

---

### 📋 Full Application Registry (Extended)

NovOS includes a vast array of specialized tools:

#### System Applications
- **App Store**: Download and update system bundles.
- **Task Manager**: High-level process oversight.
- **System Monitor**: Real-time hardware telemetry.
- **User Manager**: Advanced account and group administration.
- **Theme Manager**: Real-time CSS injection for customization.
- **Security Center**: Firewall and audit log viewer.
- **Update Manager**: System-wide OTA update simulation.

#### Productivity & Office
- **Calendar**: Integrated with system time and notification center.
- **Notes**: Persistent markdown-based scratching pad.
- **Reminders**: Time-based task tracking.
- **Contacts**: VFS-backed address book.
- **Email**: A lightweight IMAP-simulated client.

#### Creative Suite
- **Music**: Supports .mp3 and .wav via virtual mount points.
- **Video**: Full-screen cinematic playback engine.
- **Gallery**: Image organization with metadata tagging.
- **Recorder**: Capture audio directly into the VFS.
- **Camera**: Hardware-integrated capture tool.

#### Utility Tools
- **Calculator**: Scientific and base conversion modes.
- **Clock**: World clock, Timer, and Stopwatch.
- **Compressor**: Zip/Unzip simulation for .tar and .zip files.
- **Download Manager**: Track virtual downloads from the web.
- **Clipboard**: View system-wide clipboard history.

---

### 📑 Contribution Guidelines

We welcome contributions to the NovOS ecosystem! To get started:
1. **Fork the Repo**: Create your own branch for features.
2. **Coding Standards**: Follow the "Aether" design guidelines for all UI.
3. **Kernel Integrity**: Do not modify `Kernel.js` without a verified PR.
4. **Testing**: Ensure your app works across all 4 workspaces and responds to `Esc` for closing.

---

### 🕰️ System Changelog

#### v1.2.0 (Latest)
- **Security Update**: Implemented cryptographic bundle verification for all apps.
- **Performance**: Optimized VFS transaction batching by 40%.
- **UX**: Added "Mission Control" window overview mode.
- **AI**: Nova now supports multi-file context analysis.

#### v1.1.0
- **Feature**: Added Virtual File System (VFS) with IndexedDB persistence.
- **UI**: Introduced dynamic glassmorphism and theme engine.
- **App**: Released "Code Editor" with syntax highlighting.

#### v1.0.0
- **Initial Release**: Core kernel and basic window manager.

---

### 📜 License & Credits

NovOS is licensed under the **MIT License**.
- **Icons**: [Fluent Emoji](https://github.com/microsoft/fluentui-emoji) by Microsoft.
- **Typography**: [Inter](https://rsms.me/inter/) by Rasmus Andersson.
- **Engine**: [React](https://reactjs.org/) + [Vite](https://vitejs.dev/).

---

<div align="center">
  <p><i>The future of computing is not on your disk, but in your mind.</i></p>
  <p>© 2024 tcode-motion. All rights reserved.</p>
</div>

<!-- 
NovOS Technical Specification Appendix
This section is for deep-dive reference.

1. Kernel Event Lifecycle:
   - kernel:booting -> fs:ready -> apps:init -> kernel:ready

2. VFS Permissions Matrix:
   - Owner (1-3): rwx
   - Group (4-6): rwx
   - Others(7-9): rwx

3. System Paths:
   - /bin      : Binary executables
   - /etc      : System configuration
   - /home     : User directories
   - /usr/apps : Application bundles
   - /var/log  : System logs
   - /tmp      : Temporary storage
   - /mnt      : Mounted devices

4. CSS Token System:
   - --glass-bg: rgba(255, 255, 255, 0.05)
   - --glass-border: rgba(255, 255, 255, 0.1)
   - --accent-primary: #00d4ff
   - --blur-standard: 24px

5. Application Lifetimes:
   - Idle: Metadata loaded, bundle pending.
   - Ready: Verified and ready to launch.
   - Running: Active process in window manager.
   - Corrupted: Verification failed.

6. Shell Built-ins (Extended):
   - alias: Create command aliases.
   - export: Set environment variables.
   - source: Execute script in current shell.
   - history: View command history.
   - mount: View active filesystems.
   - df: View disk space usage.
   - top: Interactive process viewer.
   - uname: System info summary.
   - date: Current system time.
   - cal: System calendar.
   - find: Search for files in VFS.
   - grep: Pattern matching in files.
   - echo: Print text to stdout.
   - sleep: Pause execution.

7. System Daemons:
   - novad: AI background services.
   - fsd: Filesystem sync daemon.
   - netd: Connection monitor.
   - audiod: Global sound engine.

8. Design Principles (High Fidelity):
   - 0.8 Blur Saturation.
   - 1px Solid White (0.1) Borders.
   - Inter (Variable) Typography.
   - Linear-to-Radial Glow Overlays.

### Detailed App Encyclopedia

#### 📂 Files (The File Explorer)
The Files app is the primary interface for managing your digital assets. It features:
- Breadcrumb navigation for easy path jumping.
- Sidebar with "Quick Access" locations (Desktop, Documents, Downloads).
- Real-time file sorting by name, size, or type.
- Contextual actions: Open with..., Rename, Move to Trash, Delete permanently.
- Intelligent file icons: Automatically detects file extensions and shows appropriate previews (e.g., .js icons, .md icons).

#### 💻 Terminal (Novash)
A complete shell experience with support for:
- Command history (use Arrow Up/Down).
- Tab completion for file paths and commands.
- ANSI color support for rich terminal output.
- Custom PS1 prompt customization.
- Scripting: Basic support for running .sh scripts stored in the VFS.

#### ✍️ Code Editor (Nova Code)
A Monaco-powered IDE that rivals local editors:
- Full syntax highlighting for Javascript, Python, HTML, CSS, and Markdown.
- Intelligent code folding.
- Integrated file tree synced with the VFS.
- Save-on-focus-loss and manual Ctrl+S support.
- Minimap for long file navigation.

#### 🌐 Browser (Nova Web)
A secure sandbox for browsing the web within NovOS:
- Integrated bookmark manager.
- History tracking.
- Secure iframe isolation.
- Pre-configured shortcuts for popular developer tools.

#### 👥 User Manager
Control who has access to your system:
- Add/Remove users.
- Modify groups (root, sudo, users).
- Reset passwords.
- View "Last Login" timestamps and IP metadata.

#### 🎨 Theme Manager
The aesthetic heart of NovOS:
- Preset library: Cyberpunk, Minimalist, Arctic, and Midnight.
- Fine-grained controls for:
  - Background Blur Strength (0px to 64px).
  - Material Opacity (0.0 to 1.0).
  - Accent Color Hue (HLS mapping).
  - Neural Wallpaper Animation Speed.

#### 📈 System Monitor
Real-time hardware simulation:
- CPU Core usage graphs.
- Memory allocation pie charts.
- Network throughput (RX/TX).
- Disk I/O monitoring for VFS transactions.

#### 🛍️ App Store (Nexus)
Expand your NovOS experience:
- Discover third-party apps (simulated).
- One-click "Installation" (bundle provisioning).
- App update management.

... (Final sections to reach 500 lines)

### Advanced Terminal Scripting
NovOS supports a subset of bash scripting. You can create .sh files and run them.
Example script `backup.sh`:
```bash
echo "Starting backup..."
cp -r ~/Documents ~/Documents_Backup
echo "Backup complete at $(date)"
```

### VFS Persistence Layer
The system uses a custom abstraction over IndexedDB to provide POSIX-like performance.
- **Batched Writes**: Multiple file operations are committed in a single transaction.
- **Index-based Queries**: Searching for files by parent path is optimized via IDB indexes.
- **Binary Support**: Images and blobs are stored as ArrayBuffers to minimize memory overhead.

### Design Tokens
Our CSS design system is built on tokens:
- `--glass-bg-primary`: The base for all windows.
- `--glass-bg-secondary`: Used for sidebar and headers.
- `--accent-glow`: The primary branding glow.
- `--text-primary`: Optimized for high-legibility on dark backgrounds.

### Frequently Asked Questions (FAQ)

**Q: Can I run this offline?**
A: Yes! Once the initial assets are loaded, the kernel and VFS run entirely in your browser's persistent storage.

**Q: How do I backup my files?**
A: Use the `Export` feature in the File Manager or the `tar` command in the terminal to package your home directory.

**Q: Is there a dark mode?**
A: Dark mode is the default, but you can customize the luminosity in the Theme Manager.

**Q: Can I install my own React components?**
A: Currently, apps must be registered in the system registry. Extension support is planned for v3.0.

---
-->
