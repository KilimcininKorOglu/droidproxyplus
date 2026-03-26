# DroidProxy

A native macOS menu bar app that proxies Claude Code authentication for use with AI coding tools like [<img src="factory-logo.svg" alt="Factory.ai" height="16">](https://app.factory.ai) Droids. Built on [CLIProxyAPIPlus](https://github.com/router-for-me/CLIProxyAPIPlus).

## Setup

See [SETUP.md](SETUP.md) for authentication and Factory configuration instructions.

## Requirements

- macOS 13.0+ (Ventura or later)

## Build

```
make build
```

To create the .app bundle:

```
./create-app-bundle.sh
```

## Project Structure

```
src/
├── Sources/
│   ├── main.swift              # App entry point
│   ├── AppDelegate.swift       # Menu bar & window management
│   ├── ServerManager.swift     # Server process control & auth
│   ├── SettingsView.swift      # Main UI
│   ├── AuthStatus.swift        # Auth file monitoring
│   ├── ThinkingProxy.swift     # Thinking parameter injection proxy
│   ├── TunnelManager.swift     # Network tunnel management
│   ├── IconCatalog.swift       # Icon loading & caching
│   ├── NotificationNames.swift # Notification constants
│   └── Resources/
│       ├── cli-proxy-api-plus  # CLIProxyAPIPlus binary
│       ├── config.yaml         # Server config
│       ├── icon-active.png     # Menu bar icon (active)
│       ├── icon-inactive.png   # Menu bar icon (inactive)
│       └── icon-claude.png     # Claude service icon
├── Package.swift
└── Info.plist
```

## License

MIT
