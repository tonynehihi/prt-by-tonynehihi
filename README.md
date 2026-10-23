<p align="center">
  <img alt="Premiere by Tonynehihi" src="assets/app-icon/prt-icon-1024.png" width="180">
</p>

<h1 align="center">Premiere by Tonynehihi</h1>

<p align="center">
  <b>A personal fork of <a href="https://github.com/storytold/filmcraft">FilmCraft</a> — rebranded and customized by Tony for his own use.</b><br>
  Not an official release. Personal use only.
</p>

## Origin

All of the original source code in this project is [FilmCraft](https://github.com/storytold/filmcraft) by **storytold** — a video editing application written in Rust, released under the **MIT / Apache-2.0** licenses (see `LICENSE-MIT` and `LICENSE-APACHE` in this repo, kept unchanged from the original).

This repository is **not** the official FilmCraft and is not a public product release. It is a copy that Tony took, renamed to **Premiere by Tonynehihi**, and adjusted for his own personal workflow. All credit for the original software belongs to storytold and the FilmCraft contributors.

> "PowerPoint" and "Microsoft PowerPoint" are trademarks of Microsoft. This personal project is not affiliated with or endorsed by Microsoft in any way; the name is used only for Tony's private use.

## What Tony changed

- **Name & identity**: the app is called "Premiere by Tonynehihi", with its own Adobe-style **PrT** icon (dark navy panel, periwinkle letters — the Premiere look), About screen and macOS bundle (`PrT.app`).
- **Built-in self-update**: the app checks the Releases of this repo for the newest version — once at launch (with the release's changelog on screen when something new exists) and any time from *Help → Check for Updates*. On macOS it then downloads, builds and installs the update by itself; the current version is only swapped out for a few seconds at the very end, and the previous version is kept as a backup.
- **Clean Help menu**: About Premiere by Tonynehihi / Check for Updates / Keyboard Shortcuts / Reveal Log Files / System Compatibility Report — and **no links back to the upstream project anywhere in the app** (the header Discord button, the Home screen community links, the Help-menu website/GitHub links and the upstream docs links in Settings and the shortcuts panel are all removed).

Settings, documents and data folders keep their original FilmCraft names, so nothing already on the machine is orphaned by the rename.

## Installing on macOS

The Mac build is a source build, compiled with Cargo on Tony's own machine. In short:

```bash
cargo build --release -p deckcraft
packaging/macos/package.sh --arch aarch64
```

The DMG lands in `dist/release/`. Full instructions (clean install, removing the old build, Gatekeeper troubleshooting) are in `packaging/macos/HUONG-DAN.md` (in Vietnamese).

Once Premiere by Tonynehihi is installed, there is no need to repeat these steps for each new version: just open the app and use **Check for Updates**.

## License

Kept from the original project: **MIT OR Apache-2.0**. Tony's modifications in this repo are offered under the same terms, with the attribution above.
