# BrewVisual

A native macOS interface for managing Homebrew formulae, casks, and taps.

BrewVisual is available in English and German. Published downloads are signed with an Apple Developer ID certificate and notarized by Apple.

## Screenshots

![BrewVisual 0.6.0 dashboard in English](assets/screenshots/dashboard.png)

*Dashboard in BrewVisual 0.6.0 (English interface).*

![BrewVisual 0.6.0 menu bar icon with one available update](assets/screenshots/menu-bar-icon.png)

*Menu bar icon in BrewVisual 0.6.0 with one available update.*

![BrewVisual 0.6.0 menu bar update overlay in English](assets/screenshots/menu-bar-overlay.png)

*Menu bar update overlay in BrewVisual 0.6.0 (English interface).*

## Features

- Browse installed formulae and casks, discover packages, and manage taps.
- Browse and search packages from an installed third-party tap.
- See available updates, library counts, and recent command activity together on the dashboard.
- Install, uninstall, and upgrade packages from the main window.
- Pin and unpin installed formulae and casks to control package upgrades.
- View available updates in the menu bar and upgrade an individual package or all available packages.
- Inspect package versions, dependencies, caveats, and project links.
- Follow command and download progress, and review technical output in the command log.
- Run Homebrew diagnostics and preview cleanup candidates before confirming cleanup.

## Requirements

- macOS 27 or later
- Apple Silicon (arm64)
- An existing [Homebrew installation](https://brew.sh)

BrewVisual does not install Homebrew for you. New users see a three-step introduction covering Homebrew, permissions, and optional login startup. Homebrew must be available before setup can finish. Existing users keep their preferences and can open the guide through **Review introduction** in **Settings → Permissions**.

## Install with Homebrew

```sh
brew install --cask felix-lorenz/tap/brewvisual
```

The [Homebrew tap](https://github.com/felix-lorenz/homebrew-tap) downloads a versioned release archive and verifies its SHA-256 checksum.

## Update BrewVisual

Quit BrewVisual when no Homebrew command is running, then run:

```sh
brew update
brew upgrade --cask felix-lorenz/tap/brewvisual
```

## Direct download

Download the ZIP from the [latest release](https://github.com/felix-lorenz/brewvisual-releases/releases/latest). The release notes include its SHA-256 checksum.

Extract the ZIP and move `BrewVisual.app` to Applications. To update a direct installation, quit BrewVisual and replace the existing app with the app from the latest ZIP.

## Package checks and upgrades

By default, BrewVisual checks for updates at launch after any required introduction is complete, and every six hours while it is running. These checks run `brew update` to refresh Homebrew and package metadata; they do not upgrade installed formulae or casks.

In **Settings → General**, launch checks and periodic checks can be enabled independently. The periodic interval accepts whole hours from 1 to 24. You start package installation, removal, and upgrades explicitly, and **Check now** in the menu bar runs an on-demand check.

## Start at login

Login startup is optional and off for new users. After installing BrewVisual in Applications, enable **Start at login** in the introduction or **Settings → Permissions**. Existing login preferences are preserved. If macOS requires approval, use **Open Login Items settings** in Settings.

At login, BrewVisual opens in the menu bar without a main window or Dock icon when Homebrew is available. If Homebrew is missing, open the app manually to follow its installation guidance. Once setup is complete, opening BrewVisual from Finder or Spotlight, or choosing **Open BrewVisual** in the menu bar, shows the main window and Dock icon. Closing all app windows returns it to menu-bar-only operation.

## App Management and administrator access

When upgrading a cask, macOS may require App Management permission. BrewVisual cannot automatically verify its current authorization. It provides guidance in **Settings → Permissions** and explains how to recover after an observed access failure. Use **Open System Management** to open **System Settings → Privacy & Security → App Management** and enable access for BrewVisual. If BrewVisual is missing, add it with **+**.

If Homebrew needs `sudo` for a protected installation step, BrewVisual presents a secure administrator password prompt. The password is passed only to `sudo`; it is not stored or included in the command log.

## Support

Report bugs or request features through [GitHub Issues](https://github.com/felix-lorenz/brewvisual-releases/issues). Include your BrewVisual, macOS, and Homebrew versions, steps to reproduce the problem, and relevant command output. Remove personal information from screenshots and logs before sharing them.

You can also support BrewVisual's development on [Ko-fi](https://ko-fi.com/felixlorenz). The sidebar's **Support me on Ko-fi** link opens this page in your browser.

## About this repository

This public repository provides product documentation, screenshots, release notes, and distribution archives. The source repository is private.

BrewVisual is an independent app and is not affiliated with or endorsed by the Homebrew project.
