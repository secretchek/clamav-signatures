# ClamAV signatures mirror

Unmodified official ClamAV databases (`main.cvd`, `daily.cvd`, `bytecode.cvd`) with their official detached signatures (`*.cvd.sign`), refreshed every 6 hours by GitHub Actions from `database.clamav.net`.

Purpose: SecretChek servers cannot reach the official ClamAV CDN directly. They download the latest set from this repository's `signatures` release, verify SHA-256 against `manifest.json`, check the signature with `sigtool`, and reload `clamd`. ClamAV itself also verifies every CVD on load, so this mirror cannot change detection content.

- Download base: `https://github.com/secretchek/clamav-signatures/releases/download/signatures/`
- Only changed databases are downloaded (versions from the official `current.cvd.clamav.net` DNS record), well within ClamAV's fair-use limits.
- ClamAV and its signatures are © Cisco Talos, distributed under their license.
