# Kashot Flatpak repo

Self-hosted Flatpak repository for [Kashot](https://kashot.org) — a fast, free, tray-resident screenshot tool with a built-in annotation editor. One Rust binary on Windows, macOS, and Linux.

## Install on Linux

```sh
flatpak remote-add --if-not-exists kashot https://repo.kashot.org/kashot.flatpakrepo
flatpak install kashot org.kashot.Kashot
flatpak run org.kashot.Kashot
```

Works on every distro that ships Flatpak — Fedora, Linux Mint, Pop!_OS, openSUSE, Arch, Manjaro, elementary, Endless OS, Ubuntu, Debian, and more. **Does not depend on Flathub**; this repo is hosted directly by the Kashot maintainer.

## Why a separate repo

Flathub is the conventional Flatpak distribution channel. Kashot also has a Flathub submission in flight, but until that lands (or for users who prefer not to enable Flathub) this repo is the immediate way to install Kashot via Flatpak.

## How updates work

Each release tag in [singhpratech/kashot](https://github.com/singhpratech/kashot) triggers a GitHub Actions build that publishes the new version to the OSTree repo served from this site. `flatpak update` picks it up like any other remote.

## Sources

- App source: https://github.com/singhpratech/kashot
- Build manifest: [`dist/flatpak/org.kashot.Kashot.yaml`](https://github.com/singhpratech/kashot/blob/main/dist/flatpak/org.kashot.Kashot.yaml) in the main repo
- Build workflow: [`.github/workflows/build-flatpak-repo.yml`](https://github.com/singhpratech/kashot/blob/main/.github/workflows/build-flatpak-repo.yml)

License: Apache-2.0
