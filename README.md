# Swiftcord Archive

An archive of [Swiftcord](https://swiftcord.app) macOS releases.

**This repository is for educational purposes only.** It is not affiliated with or endorsed by Swiftcord or Discord. All rights to Swiftcord belong to its authors.

## How it works

A GitHub Action checks https://swiftcord.app/download every 4 hours. When it points to a new DMG, the action:

- publishes the DMG and its `.sha256` file as a release tagged with the DMG name (for example `Swiftcord-87`)
- appends the SHA-256 to [SHA256SUMS](SHA256SUMS)

It can also be run by hand from the Actions tab.

## Verifying a download

```sh
sha256sum -c Swiftcord-87.dmg.sha256
```

On macOS use `shasum -a 256 -c` instead.
