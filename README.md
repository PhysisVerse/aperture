# APERTURE

### Unified Client for the Physis Ecosystem

Aperture is the primary application layer for interacting with the Physis ecosystem. It provides a unified operational interface across platforms, including iOS, Android, Desktop, and Web. The project focuses on maintainability, modular architecture, and consistent behavior across all supported environments.

---

## Repository Structure

```text
physis-aperture/
│
├── apps/                         # Platform‑specific client applications
│   ├── aperture-ios/             # iOS client (Swift / SwiftUI)
│   ├── aperture-android/         # Android client (Kotlin / Compose)
│   ├── aperture-desktop/         # Desktop client (Tauri: Rust + React)
│   └── aperture-web/             # Web client (Next.js)
│
├── packages/                     # Cross‑platform shared modules
│   ├── design-tokens/            # UI tokens: color, typography, spacing
│   ├── copy/                     # Shared string tables and localization keys
│   ├── api-schema/               # OpenAPI/Proto contract definitions
│   ├── core-ts/                  # Shared TypeScript SDK
│   └── core-rust/                # Shared Rust SDK
│
├── docs/                         # Documentation for architecture and processes
│   ├── architecture/             # System architecture and internal design
│   ├── onboarding/               # SmartSpot onboarding specifications
│   ├── ui/                       # UI system and component documentation
│   └── operations/               # Release, workflows, and operational processes
│
├── scripts/                      # Utility and automation scripts
│   ├── format-all.sh
│   ├── validate-schema.sh
│   └── generate-tokens.sh
│
├── .github/workflows/            # CI/CD pipelines
│   ├── ios-ci.yml
│   ├── android-ci.yml
│   ├── desktop-ci.yml
│   ├── web-ci.yml
│   └── lint.yml
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## Purpose

Aperture provides a unified access layer for users interacting with:

* SmartSpot node onboarding and management
* ASTRALIS identity, staking, and network participation
* SYNCRAL device and automation control
* Cross‑environment workflows (local device ⇄ edge ⇄ cloud)

The objective is to deliver consistent interaction patterns and a predictable operational model across all supported platforms.

---

## Platform Approach

Each platform implementation uses its native framework and tooling:

### iOS — Swift/SwiftUI

Native implementation optimized for reliability, lifecycle management, and integration with platform services.

### Android — Kotlin/Compose

Native implementation following contemporary Android UI and state management standards.

### Desktop — Tauri (Rust + React)

Lightweight desktop application using a Rust backend and a React‑based interface.

### Web — Next.js

Web client optimized for performance, structured routing, and interoperability with TypeScript packages.

---

## Shared Modules

Shared code is placed in `packages/` to maintain consistency and reduce duplication.

* **design-tokens/** — Defines UI tokens for platform‑specific consumption.
* **copy/** — Centralized string keys for all clients.
* **api-schema/** — Single source of truth for API definitions.
* **core-ts/** & **core-rust/** — Cross‑platform domain and protocol logic.

Benefits:

* Consistent behavior across clients
* Smaller platform‑specific codebases
* Simplified maintenance and updates

---

## Contributing

Development follows a straightforward branch‑based workflow:

* `main` contains stable and deployable code.
* New work is performed in short‑lived `feature/*` branches.
* Platform‑specific changes are made within `apps/`.
* Shared logic is contributed through `packages/`.
* Documentation updates are placed in `docs/`.

CI pipelines validate each platform and shared module.

---

## License

Hyrbid © Physis Labs LLC — governed by the Physis DAO.

Usage, distribution, and contributions follow DAO‑defined policies.

