# FreeSense

**An open-source firewall & router distribution — a community rebuild and rebrand of [pfSense](https://www.pfsense.org/)® CE, built from source on FreeBSD and published under the Apache License 2.0.**

FreeSense takes the open-source pfSense CE codebase, rebuilds it cleanly from source, and ships it under a neutral, community-owned name and package repository. The whole firewall stack — FreeBSD base, kernel, `rc` system, PHP/nginx web GUI, and the configuration system — is built end-to-end and distributed from infrastructure we control.

---

## Repositories

| Repository | What's in it |
|------------|--------------|
| **[freesense](https://github.com/FreeSense-org/freesense)** | The main source & build tree — rebranded `src/`, the `tools/` builder, `build.sh`, and CI. |
| **[freesense-ports](https://github.com/FreeSense-org/freesense-ports)** | The ports overlay / poudriere recipes — `FreeSense-*` port Makefiles and the package build set. |
| **[freesense.org](https://github.com/FreeSense-org/freesense.org)** | The project website and downloads page. |

> Built package binaries are published to **`pkg.freesense.org`** and installer images to **`downloads.freesense.org`** — they are not stored in Git.

---

## How it fits together

- A FreeBSD **package repository is just signed static files over HTTPS**, so FreeSense's `pkg` repo and ISO images are served as plain static objects from a CDN — no application server.
- Installed systems fetch packages from **`pkg.freesense.org`** and verify them against a fingerprint that ships in the OS, so only repositories signed with the FreeSense key are trusted as "official."
- Anyone can rebuild FreeSense from source under the Apache License with **their own** signing key — that's the point of an open distribution.

---

## License & attribution

FreeSense is licensed under the **Apache License, Version 2.0**.

FreeSense is a **derivative work of pfSense CE**, Copyright © 2004–2016 Electric Sheep Fencing, LLC and © 2014–2026 Rubicon Communications, LLC (Netgate), originally published under the Apache License 2.0. Original copyright notices are retained in accordance with that license. Portions are originally based on m0n0wall.

> **"pfSense" is a registered trademark of Electric Sheep Fencing, LLC, licensed to Netgate.** FreeSense is **not** pfSense and is **not** affiliated with, sponsored by, or endorsed by Netgate or Electric Sheep Fencing. The pfSense name is used here only to identify the upstream project from which FreeSense is derived.

This software is provided **"AS IS"**, without warranty of any kind. See the `LICENSE` and `NOTICE` files in each repository.
