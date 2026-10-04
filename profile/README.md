<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/FreeSense-org/.github/main/brand/lockup-dark.png">
  <img alt="FreeSense — open firewall distro" src="https://raw.githubusercontent.com/FreeSense-org/.github/main/brand/lockup-light.png" width="460">
</picture>

### The open firewall &amp; router distribution — **open source all the way down, including the updater.**

[![License](https://img.shields.io/badge/license-Apache--2.0-EA4F2D?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0)
[![Built on FreeBSD 16](https://img.shields.io/badge/built%20on-FreeBSD%2016-14181F?style=flat-square)](https://www.freebsd.org/)
[![Stable 1.0.x](https://img.shields.io/badge/stable-1.0.x-EA4F2D?style=flat-square)](https://www.freesense.org/download/)
[![Development 1.1](https://img.shields.io/badge/development-1.1%20nightly-14181F?style=flat-square)](https://www.freesense.org/download/)
[![Docs](https://img.shields.io/badge/docs-docs.freesense.org-EA4F2D?style=flat-square)](https://docs.freesense.org)

**[Website](https://www.freesense.org)** · **[Download](https://www.freesense.org/download/)** · **[Documentation](https://docs.freesense.org)** · **[News](https://www.freesense.org/news/)**

</div>

---

**FreeSense** is a community-owned firewall and router operating system, built from source on
FreeBSD 16 with a full web GUI and a curated set of networking packages. It grew out of the
open-source pfSense® CE codebase, but everything you run — the base OS, the packages, the web UI,
**and the update client** — is open, auditable, and published from infrastructure the community
controls. No accounts, no activation, no telemetry.

## What's new

- 🆕 **[NetSpider](https://www.freesense.org/apps/netspider/)** joins the FreeSense family — a free,
  open-source Layer 2 / Layer 3 network diagnostics tool for Windows that maps every device and
  pinpoints the failing hop.
- 🏗️ **Dedicated build server.** FreeSense now compiles on its own dedicated build machine — a
  self-hosted GitHub Actions runner (AMD Ryzen 7, 16 threads, KVM). Each component builds in a fresh,
  throwaway FreeBSD VM. The same build that took over two hours on GitHub-hosted runners now finishes
  in under 40 minutes.
- 🌙 **Nightly Development builds.** The rolling **1.1** line is planned every night at 01:00 UTC.
  Only components whose inputs changed are rebuilt, and verified results are published to the
  `devel` channel automatically.
- 🍓 **ARM64 &amp; Raspberry Pi preview.** A generic ARM64 UEFI installer plus Raspberry Pi 4B and
  Pi 5 appliance images, built next to amd64 in the same pipeline. Experimental, made for labs.
- ☁️ **Official cloud images.** Preinstalled QCOW2 and raw GPT disks (UFS or ZFS, BIOS and UEFI)
  for Proxmox, OpenStack, QEMU/KVM and bhyve.
- 📚 **[docs.freesense.org](https://docs.freesense.org)** — installation, upgrades, packages and
  operations guides.

## Releases

| Line | Status | What to expect |
|------|--------|----------------|
| **Stable 1.0.x** | Supported | The production line. Immutable releases; necessary security fixes ship as signed patch releases. |
| **Development 1.1** | Experimental | Rolling, rebuilt nightly from source. For labs and testing. Upgrading 1.0 → 1.1 is one-way. |

System and Optional Packages are built, signed and published independently: a System-only change
never forces a package rebuild. The FreeBSD platform pin advances every 14 days, and an ISO is
only published once a verified System + Packages pair passes its smoke tests.

## Why FreeSense

- 🔓 **Open all the way down — including the updater.** The piece that decides which firmware and
  packages your firewall trusts and installs is, on most "open" firewalls, a closed vendor binary.
  In FreeSense it's a small, readable, fully open implementation.
- 🛠️ **An open build &amp; release pipeline.** Every workflow, pin, build log and release decision
  is public in GitHub Actions. The heavy compilation runs on our dedicated build server, and its
  recipe is in the repository too: nothing is built off the record, and every artifact traces back
  to exact, inspectable source, ports and FreeBSD revisions.
- 📦 **Reproducible, from source.** The OS base is stock upstream FreeBSD plus a small, auditable
  [patch series](https://github.com/FreeSense-org/freesense-os-base/tree/main/patches) — no opaque
  fork to take on faith. Re-pin, re-apply, rebuild.
- 🔑 **Own your trust root.** Updates are RSA-signed and verified on the appliance before anything
  changes. Anyone can rebuild FreeSense under Apache 2.0 with **their own** signing key and run an
  independent, equally-official distribution.
- 🌐 **Independent infrastructure.** Signed packages at **pkg.freesense.org** and installer images
  at **downloads.freesense.org**, served as plain signed static files over a CDN — a firewall repo
  needs no application server.
- ♻️ **Upgrade boldly, roll back calmly.** ZFS boot environments snapshot the whole OS before an
  upgrade; pick a known-good one from the WebUI or the boot menu.

## Explore

| Repository | What's in it |
|------------|--------------|
| **[freesense](https://github.com/FreeSense-org/freesense)** | Base product source — installer, WebUI, system behavior and the `tools/` builder. |
| **[freesense-os-base](https://github.com/FreeSense-org/freesense-os-base)** | The build &amp; release control plane — FreeBSD 16 pin and patch series, GitHub Actions workflows, build runner recipe, signing and publication. |
| **[freesense-system-ports](https://github.com/FreeSense-org/freesense-system-ports)** | Operating-system ports overlay used to build the System repository and installation media. |
| **[freesense-packages](https://github.com/FreeSense-org/freesense-packages)** | Optional packages published through the FreeSense package manager. |
| **[freesense-docs](https://github.com/FreeSense-org/freesense-docs)** | Source for [docs.freesense.org](https://docs.freesense.org). |
| **[freesense.org](https://github.com/FreeSense-org/freesense.org)** | Project website, downloads page and live release feeds. |
| **[NetSpider](https://github.com/FreeSense-org/NetSpider)** | L2/L3 network diagnostics for Windows — part of the FreeSense family. |

> Built package binaries and ISO images are published to the CDN — they are not stored in Git.

---

**Upstream &amp; license.** FreeSense is a derivative work of **pfSense® CE**, © 2004–2016 Electric Sheep Fencing, LLC and © 2014–2026 Rubicon Communications, LLC (Netgate), originally published under the Apache License 2.0; portions originate from m0n0wall. FreeSense is licensed under the **Apache License 2.0**, and original copyright notices are retained per that license. *"pfSense" is a registered trademark of Electric Sheep Fencing, LLC, licensed to Netgate.* FreeSense is **not** pfSense and is **not** affiliated with, sponsored by, or endorsed by Netgate or Electric Sheep Fencing — the name is used only to identify the upstream project FreeSense is derived from. Provided **"AS IS"**, without warranty of any kind.
