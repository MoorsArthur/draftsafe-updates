# Draftsafe updates

This repository distributes Draftsafe update metadata and versioned downloads.
The full development repository is private during the initial trial. The
Thunderbird XPI and MCP bundles published here contain readable program code.

| File | Purpose |
| --- | --- |
| `thunderbird-updates.json` | Thunderbird's stable self-hosted update manifest |
| `update-manifest.json` | Ed25519-signed MCP release metadata |
| Release assets | Versioned XPI, MCP bundle, checksums and smoke report |

The add-on ID is `draftsafe-tools@armain.be`. The 0.7.0 add-on needs one
manual update to enter this self-hosted channel. The MCP updater is opt-in,
checks a pinned public key and bundle hash, and stages newer releases for the
next MCP launch. Neither updater sends mailbox contents or a bridge token.

New releases are published only after the private source release gate passes
its tests, build and isolated Thunderbird smoke test. Versioned release files
are uploaded before either stable manifest is changed. A failed or unavailable
update check leaves the installed version usable.

Draftsafe is MIT-licensed. The public key and implementation details are in
the source project's documentation available to collaborators. No signing
private key or mailbox data belongs in this repository.
