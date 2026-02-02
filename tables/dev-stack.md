# Development Stack

## Table of Content

- [Complete Development Stack (All Approaches)](#complete-development-stack-all-approaches)
- [OS-Native vs Cross-Platform Software](#os-native-vs-cross-platform-software)
- [Desktop Development Stack](#desktop-development-stack)
- [Mobile Development Stack](#mobile-development-stack)
- [Web Development Stack](#web-development-stack)
- [Infrastructure & Tools](#infrastructure--tools)
- [Libraries, Utilities & CLI Tools Stack](#libraries-utilities--cli-tools-stack)
- [Key Insights](#key-insights)

### **Complete Development Stack (All Approaches)**

**Legend**: ✨ = Recommended choice for modern development (best balance of productivity, ecosystem, and performance)

| Category                  | Target Platform(s)      | Stack                         | Languages                     | Programming Style         | UI/Framework / APIs              | Examples                          |
| ------------------------- | ----------------------- | ----------------------------- | ----------------------------- | ------------------------- | -------------------------------- | --------------------------------- |
| **DESKTOP**               |                         |                               |                               |                           |                                  |                                   |
| Native macOS              | macOS                   | Xcode + Swift                 | Swift, Objective-C            | OOP, declarative          | SwiftUI, AppKit                  | Final Cut Pro, professional apps  |
| Native Windows            | Windows                 | Visual Studio + .NET          | C#, C++, VB.NET               | OOP, MVVM, WPF/WinUI      | WPF, WinUI, MAUI                 | MS Office, enterprise apps        |
| Native Linux              | Linux                   | Compiler + GUI toolkit        | C, C++, Rust, Python          | OOP, modular              | GTK, Qt                          | GNOME Builder, KDE                |
| Cross-Platform Desktop ✨| Win/Mac/Linux           | Qt/GTK + C++/Rust             | C++, Rust, Python             | OOP, modular              | Qt Widgets, Qt Quick, GTK        | Blender, Krita, VLC               |
| Native Games AAA          | Multiple (via engine)   | Native engine + hardware      | C++, HLSL, Metal              | OOP, ECS, performance     | DirectX, Metal, Vulkan           | Halo, X-Plane                     |
| Hybrid Desktop ✨        | Win/Mac/Linux           | Electron/Tauri + web stack    | JS, TS, Rust (Tauri)          | Declarative, modular      | HTML/CSS + React/Vue/Svelte      | VS Code, Discord, Obsidian        |
| **MOBILE**                |                         |                               |                               |                           |                                  |                                   |
| Native iOS                | iOS, iPadOS             | Xcode + Swift                 | Swift, Objective-C            | OOP, declarative          | SwiftUI, UIKit                   | Xcode, iOS native apps            |
| Native Android            | Android                 | Android Studio + Kotlin       | Kotlin, Java                  | OOP, functional-style     | Jetpack Compose, Material Design | Android Studio, Play Store apps   |
| Cross-Platform Mobile ✨ | iOS + Android           | Framework + native compile    | Dart, JS/TS, C#               | Declarative, reactive     | Flutter, React Native, Xamarin   | Telegram, many modern apps        |
| Mobile Cross-Platform Gen | iOS + Android (runtime) | Runtime + native compilation  | Dart, JS/TS                   | Declarative, reactive     | Flutter, React Native            | Instagram (partial), TikTok       |
| Progressive Web App       | Any browser             | Web + service workers         | JS, TS, PWA APIs              | Declarative, component    | Responsive web, HTML5            | PWA, Workbox, Next.js PWA         |
| **WEB**                   |                         |                               |                               |                           |                                  |                                   |
| Frontend                  | Browser                 | Node.js + bundler             | JS, TS, JSX                   | Declarative, component    | React, Vue, Angular, Svelte      | Vite, Next.js, Create React App   |
| Backend API ✨           | Server (any OS)         | Runtime + framework           | Node.js, Python, Go, Rust     | OOP, functional, async    | Express, FastAPI, Django, Actix  | Express.js, FastAPI, NestJS       |
| Full-Stack Web ✨         | Browser + Server        | SSR/SSG + framework           | JS, TS                        | Convention over config    | Next.js, Nuxt, SvelteKit, Remix  | Next.js, Remix, Astro             |
| Static Site Generator     | Browser                 | Compiler + markdown           | JS, Go, Rust                  | Template-based            | Hugo, Jekyll, Eleventy, Astro    | Hugo, Gatsby, Astro               |
| **SPECIAL PURPOSE**       |                         |                               |                               |                           |                                  |                                   |
| Cross-Platform General    | Multiple (abstracted)   | C++/Rust + abstraction layer  | C++, Rust, C#                 | OOP, modular              | Qt, GTK, Unity, Unreal           | Blender, Unity, Unreal Engine     |
| Web Application           | Browser                 | Browser + HTML/CSS/JS         | JS, TS, WASM                  | Declarative, reactive     | React, Vue, Svelte, WASM         | Figma, Google Docs, Notion        |

> **Summary**: ✨ marks indicate recommended modern stacks with best balance of productivity, ecosystem maturity, and performance.
> Choose **Native** for max performance + platform integration (trade-off: code duplication).
> Choose **Cross-Platform** for code reuse (trade-off: some overhead).
> Choose **Web/Hybrid** for rapid iteration + maximum reach (trade-off: less native feel).
> Choose **Full-Stack Web** when backend logic is critical.
> For games, use specialized **Game Engines**.

---

| Category              | Stack                         | Languages                  | Programming Style           | UI                    | Frameworks / APIs                | Examples                     |
| --------------------- | ----------------------------- | -------------------------- | --------------------------- | --------------------- | -------------------------------- | ---------------------------- |
| OS-Native Desktop     | Native OS + graphics libs     | C, C++, Swift, Objective-C | OOP, imperative             | Native, OS-consistent | Cocoa, Win32, WPF                | Final Cut Pro, MS Office     |
| Native Games AAA      | Native engine + hardware      | C++, HLSL, Metal           | OOP, ECS, performance-first | Native 3D             | DirectX, Metal, Vulkan           | Halo, X-Plane                |
| Cross-Platform Native | C++/Rust + abstraction layer  | C++, Rust, C#              | OOP, modular                | Qt/GTK widgets        | Qt, GTK, Unity, Unreal           | Blender, Unity, Unreal       |
| Web Applications      | Browser + HTML/CSS/JS         | JS, TS, WASM               | Declarative, reactive       | Responsive            | React, Vue, Svelte               | Figma, Google Docs           |
| Hybrid Desktop        | Chromium + Node.js            | JS, TS                     | Declarative, modular        | Web-in-native         | Electron, Tauri                  | VS Code, Discord, Obsidian   |
| Mobile Cross-Platform | Runtime + native compilation  | Dart, JS/TS                | Declarative, reactive       | Mobile UI             | Flutter, React Native            | Telegram, many modern apps   |

> **Key trade-offs**: Native = max performance + OS integration - portability. Cross-platform native = good performance + portability. Web/hybrid = max portability - some performance overhead.

---

### **Desktop Development Stack**

| Category              | Stack                        | Languages                  | Programming Style         | UI Framework         | Target OS        | Examples                       |
| --------------------- | ---------------------------- | -------------------------- | ------------------------- | -------------------- | ---------------- | ------------------------------ |
| Native macOS          | Xcode + Swift                | Swift, Objective-C         | OOP, declarative          | SwiftUI, AppKit      | macOS            | Xcode, professional apps       |
| Native Windows        | Visual Studio + .NET         | C#, C++, Visual Basic      | OOP, MVVM, WPF/WinUI      | WPF, WinUI, MAUI     | Windows          | Visual Studio, enterprise apps |
| Native Linux          | Compiler + GUI toolkit       | C, C++, Rust, Python       | OOP, modular              | GTK, Qt              | Linux            | GNOME Builder, KDE            |
| Cross-Platform Native | Qt/GTK + C++/Rust            | C++, Rust, Python          | OOP, modular              | Qt Widgets, Qt Quick | Win/Mac/Linux    | Blender, Qt Creator            |
| Hybrid (Web-based)    | Electron/Tauri + web stack   | JS, TS, Rust (Tauri)       | Declarative, modular      | HTML/CSS + frameworks| Win/Mac/Linux    | VS Code, Discord, Obsidian     |
| Enterprise & Business | .NET/Java + frameworks       | C#, Java                   | OOP, MVVM, MVC            | WPF, Swing, JavaFX   | Cross-platform   | Visual Studio, IntelliJ        |

> **Key characteristics**: Native = best UX + performance - code reuse. Electron = rapid dev + web skills - memory overhead. Tauri = modern web + lightweight.

---

### **Mobile Development Stack**

| Category              | Stack                    | Languages              | Programming Style       | UI/Framework         | Platforms        | Examples                       |
| --------------------- | ------------------------ | ---------------------- | ----------------------- | -------------------- | ---------------- | ------------------------------ |
| Native iOS            | Xcode + Swift            | Swift, Objective-C     | OOP, declarative        | SwiftUI, UIKit       | iOS, iPadOS      | Xcode, iOS frameworks          |
| Native Android        | Android Studio + Kotlin  | Kotlin, Java           | OOP, functional-style   | Jetpack Compose, XML | Android          | Android Studio, Material Design|
| Cross-Platform        | Framework + compilation  | Dart, JS/TS, C#        | Declarative, reactive   | Native widgets       | iOS + Android    | Flutter, React Native, Xamarin |
| Progressive Web App   | Web + service workers    | JS, TS, PWA APIs       | Declarative, component  | Responsive web       | Any browser      | PWA, Workbox, Next.js          |
| Backend for Mobile    | API + cloud services     | Node.js, Python, Go    | OOP, functional, async  | REST/GraphQL API     | Cloud            | Firebase, Supabase, AWS Lambda |

> **Key characteristics**: Native apps = max performance + platform features. Cross-platform = code reuse - some overhead. PWA = no install, offline support.

---

### **Web Development Stack**

| Category           | Stack                  | Languages              | Programming Style              | UI/Interface     | Frameworks / APIs              | Examples                       |
| ------------------ | ---------------------- | ---------------------- | ------------------------------ | ---------------- | ------------------------------ | ------------------------------ |
| Frontend           | Node.js + bundler      | JS, TS, JSX            | Declarative, component-based   | Browser          | React, Vue, Angular, Svelte    | Vite, Next.js, Create React App|
| Backend            | Runtime + framework    | Node.js, Python, Go, Rust | OOP, functional, REST APIs  | HTTP API         | Express, FastAPI, Django       | Express.js, FastAPI, NestJS    |
| Full-Stack         | SSR/SSG + framework    | JS, TS                 | Convention over config         | Universal (SSR)  | Next.js, Nuxt, SvelteKit, Remix| Next.js, Remix, Astro          |
| Static Sites       | Compiler + markdown    | JS, Go, Rust           | Template-based                 | Static HTML      | Hugo, Jekyll, Eleventy         | Hugo, Gatsby, Astro            |

> **Key characteristics**: Fast iteration cycles, npm/yarn ecosystem, runs in browser or server, maximum reach.

---

### **Infrastructure & Tools**

| Category              | Stack                    | Languages/Config     | Style        | Interface       | Technologies                  | Examples                           |
| --------------------- | ------------------------ | -------------------- | ------------ | --------------- | ----------------------------- | ---------------------------------- |
| IDEs & Editors        | Cross-platform + plugins | Any (via extensions) | Modular      | Native/Electron | IntelliJ, Eclipse, LSP        | VS Code, IntelliJ, Neovim          |
| Version Control       | Distributed VCS          | N/A                  | Distributed  | CLI/GUI         | Git                           | GitHub, GitLab, Git CLI            |
| Databases (SQL)       | RDBMS + ACID             | SQL                  | Declarative  | CLI/GUI         | PostgreSQL, MySQL             | PostgreSQL, MySQL, SQLite          |
| Databases (NoSQL)     | Document/KV store        | JSON, proprietary    | API-based    | Web UI/CLI      | MongoDB, Redis                | MongoDB, Redis, DynamoDB           |
| Containers            | Lightweight virt         | Dockerfile, YAML     | Declarative  | CLI/Web UI      | Docker, Kubernetes            | Docker, k8s, Podman                |
| CI/CD                 | Automated pipelines      | YAML, Shell          | Declarative  | Web UI          | GitHub Actions, Jenkins       | GitHub Actions, GitLab CI          |
| Infrastructure as Code| Provisioning automation  | HCL, YAML            | Declarative  | CLI             | Terraform, Ansible            | Terraform, Pulumi, CloudFormation  |
| Monitoring            | Metrics + logs + traces  | Query DSLs           | Declarative  | Dashboards      | Prometheus, Grafana           | Prometheus, Datadog, Grafana       |

> **Key characteristics**: Developer productivity, automation, scalability, observability.

---

### **Libraries, Utilities & CLI Tools Stack**

| Category              | Purpose                          | Languages              | Distribution     | Package Managers          | Examples                       |
| --------------------- | -------------------------------- | ---------------------- | ---------------- | ------------------------- | ------------------------------ |
| System Libraries      | Core OS functionality            | C, C++, Rust           | System package   | apt, brew, yum, chocolatey| glibc, OpenSSL, zlib           |
| Data Processing       | Data manipulation & analysis     | Python, Rust, Go       | pip, cargo, brew | pip, npm, cargo           | NumPy, Pandas, Polars          |
| Testing Frameworks    | Unit, integration, E2E testing   | Language-specific      | Package manager  | npm, pip, Maven, Cargo    | Jest, pytest, Vitest, Go test  |
| CLI Tools             | Command-line utilities           | Go, Rust, Python, Shell| Standalone binary| cargo, pip, npm, brew     | ffmpeg, curl, jq, ripgrep      |
| HTTP/Networking       | Web requests & protocols         | Multi-language         | Package manager  | npm, pip, Maven, Cargo    | axios, requests, reqwest       |
| Authentication & Crypto| Security & encryption libraries  | Multi-language         | Package manager  | npm, pip, Maven, Cargo    | bcrypt, jsonwebtoken, NaCl     |
| Logging & Monitoring  | Application logging & metrics    | Multi-language         | Package manager  | npm, pip, Maven, Cargo    | Winston, pino, Serilog, logrus |
| Database Drivers      | DB connectivity & ORM            | Multi-language         | Package manager  | npm, pip, Maven, Cargo    | Prisma, SQLAlchemy, mongoose   |

> **Key characteristics**: Libraries = reusable code, CLI tools = standalone execuutilities = solve specific problems, distributed via package managers or pre-built binaries.

---

### **Key Insights**

**Abstraction vs Performance**
- Native → max efficiency, min portability
- Cross-platform compiled → balanced performance + portability
- Web/containerized → max portability, runtime-dependent efficiency

**Common Language Patterns**
- Performance-critical → C, C++, Rust
- Rapid development → Python, C#, TypeScript, Dart
- Web/universal → JS, TypeScript, WASM

**Modern Trends**
- WASM bridges efficiency + portability
- Cross-platform frameworks (Qt, Flutter, Tauri) improve native feel
- Cloud-native with containers + orchestration as default
- Observability built-in from the start

**Recommended Stacks by Project Type**
- Web startup → TypeScript + Next.js/React + PostgreSQL + Docker
- Mobile app → Flutter or React Native + Firebase/Supabase
- Game → Unreal/Unity + C++/C#
- Embedded system → C/Rust + bare metal or RTOS
- Microservices → Go/Rust + Kubernetes + PostgreSQL/Redis
- Enterprise → Java/C# + Spring/ASP.NET + SQL + Kubernetes
