# Swiftcord Archive

An archive of [Swiftcord](https://swiftcord.app) macOS releases.

**This repository is for educational purposes only.** It is not affiliated with or endorsed by Swiftcord or Discord. All rights to Swiftcord belong to its authors. Archived DMGs are preserved as published and may inadvertently include Discord assets or branding; those materials remain the property of their respective rights holders.

## How it works

A GitHub Action checks <https://swiftcord.app/download> every 4 hours. When it points to a new DMG, the action:

- saves it to the [Wayback Machine](https://web.archive.org/web/*/https://cdn.swiftcord.app/*) and links that capture as the release source
- publishes the DMG and any delta files linked for that build in the appcast, with a `.sha256` file for each artifact, as a release tagged with the DMG name
- appends the SHA-256 to [SHA256SUMS](SHA256SUMS)

It can also be run by hand from the Actions tab.

## Verifying a download

```sh
sha256sum -c Swiftcord-87.dmg.sha256
```

Each delta file also has its own `.sha256` file. On macOS use `shasum -a 256 -c` instead.
