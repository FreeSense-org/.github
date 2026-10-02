<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/FreeSense-org/.github/main/brand/lockup-dark.png">
  <img alt="FreeSense — open firewall distro" src="https://raw.githubusercontent.com/FreeSense-org/.github/main/brand/lockup-light.png" width="460">
</picture>

### The open firewall &amp; router distribution — **open source all the way down, including the updater.**

[![License](https://img.shields.io/badge/license-Apache--2.0-EA4F2D?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0)
[![Built on FreeBSD](https://img.shields.io/badge/built%20on-FreeBSD-14181F?style=flat-square)](https://www.freebsd.org/)
[![Packages](https://img.shields.io/badge/pkg-pkg.freesense.org-EA4F2D?style=flat-square)](https://pkg.freesense.org)
[![ISOs](https://img.shields.io/badge/downloads-downloads.freesense.org-14181F?style=flat-square)](https://downloads.freesense.org)

</div>

---

**FreeSense** is a community-owned firewall and router operating system, built from source on
FreeBSD with a hardened kernel, a full web GUI, and a curated set of networking packages.
It grew out of the open-source pfSense® CE codebase, but everything you run — the base OS, the
packages, the web UI, **and the update client** — is open, auditable, and published from
infrastructure the community controls.

## Why FreeSense

- 🔓 **Open all the way down — including the updater.** The piece that decides which firmware and
  packages your firewall trusts and installs is, on most "open" firewalls, a closed vendor binary.
  In FreeSense it's a small, readable, fully open implementation. Nothing about how your box updates
  itself is a black box.
- 🛠️ **An open build &amp; release pipeline.** Every package and ISO is built in public CI you can
  read top to bottom, cryptographically signed, and published to open infrastructure. No private
  build server, no "trust us" artifacts.
- 📦 **Reproducible, from source.** The OS base is stock upstream FreeBSD plus a small, auditable
  patch series — no opaque fork to take on faith. Re-pin, re-apply, rebuild.
- 🔑 **Own your trust root.** Anyone can rebuild FreeSense under Apache 2.0 with **their own** signing
  key and run an independent, equally-official distribution. That's the whole point.
- 🌐 **Independent infrastructure.** Signed packages at **[pkg.freesense.org](https://pkg.freesense.org)**
  and installer images at **[downloads.freesense.org](https://downloads.freesense.org)**, served as
  plain signed static files over a CDN — a firewall repo needs no application server.
- 🧭 **Release &amp; devel channels.** Pick a stable release channel or ride development, and upgrade
  cleanly between versions — release → release, devel → devel — straight from the web UI.

## Explore

| Repository | What's in it |
|------------|--------------|
| **[freesense](https://github.com/FreeSense-org/freesense)** | Main source &amp; build tree — the OS sources, the `tools/` builder, `build.sh`, and CI. |
| **[freesense-system-ports](https://github.com/FreeSense-org/freesense-system-ports)** | System and runtime ports used to build the operating system, update repository, and installation media. |
| **[freesense-packages](https://github.com/FreeSense-org/freesense-packages)** | Optional package ports and metadata published through the FreeSense package manager. |
| **[freesense-os-base](https://github.com/FreeSense-org/freesense-os-base)** | The open build &amp; release pipeline — world+kernel core packages and ports, built on CI, signed, shipped to R2. The FreeBSD base delta (patch series on a pinned upstream commit) lives on its per-version [`os-base/*` branches](https://github.com/FreeSense-org/freesense-os-base/tree/os-base/freebsd-16.0). |
| **[freesense.org](https://github.com/FreeSense-org/freesense.org)** | Project website and downloads page. |

> Built package binaries and ISO images are published to the CDN above — they are not stored in Git.

---

**Upstream &amp; license.** FreeSense is a derivative work of **pfSense® CE**, © 2004–2016 Electric Sheep Fencing, LLC and © 2014–2026 Rubicon Communications, LLC (Netgate), originally published under the Apache License 2.0; portions originate from m0n0wall. FreeSense is licensed under the **Apache License 2.0**, and original copyright notices are retained per that license. *"pfSense" is a registered trademark of Electric Sheep Fencing, LLC, licensed to Netgate.* FreeSense is **not** pfSense and is **not** affiliated with, sponsored by, or endorsed by Netgate or Electric Sheep Fencing — the name is used only to identify the upstream project FreeSense is derived from. Provided **"AS IS"**, without warranty of any kind.
