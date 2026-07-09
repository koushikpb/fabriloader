# fabriloader

A custom injectable runtime loader for [Fabric](https://fabricmc.net/) mods, written in Rust.

fabriloader is a native library (`cdylib`) that attaches to a running Minecraft JVM via `JNI_OnLoad`. Once loaded, it authenticates the user, fetches and decrypts a mod payload, and defines the classes, mixins, resources, and access wideners directly into the game at runtime — without touching the game's own mod folder.

## Features

- Native JVM injection through JNI
- Runtime class definition via a custom classloader
- Mixin service and ASM bytecode transformation
- Encrypted payload delivery and on-the-fly decryption (AES)
- User login, session handling, and auto-update
- Cross-platform message boxes (Windows / macOS / Linux)

## Build

```sh
cargo build --release
```

The output is a platform-native shared library (`.dll` / `.dylib` / `.so`) to be injected into the target JVM.

## Status

> **Archived.** Built in early 2025 targeting Minecraft 1.21. No longer maintained.

## License

Released under the [MIT License](LICENSE).
