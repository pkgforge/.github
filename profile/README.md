<p align="center">
    <a href="https://github.com/pkgforge/soar">
        <img src="https://github.com/user-attachments/assets/680eb489-d972-429c-b144-8b68c5048c3e" width="256">
    </a>
    <br>
    <b><a href="https://github.com/pkgforge">Package Forge</a></b>
</p>

---

## About

[![Discord](https://img.shields.io/discord/1313385177703256064?logo=%235865F2&label=Discord)](https://discord.gg/djJUs48Zbu)

[Package Forge](https://github.com/pkgforge) is rethinking package management for Unix systems. We carry statically compiled binaries and portable packages in AppImage and other formats, taken from upstream wherever upstream already ships them and built by us where nobody does, along with a [package manager](https://github.com/pkgforge/soar) that installs them without root.

---

## Projects

### Core

| Project | Description |
|---------|-------------|
| [soar](https://github.com/pkgforge/soar) | A modern, lightweight, distro-independent package manager built in Rust. |
| [soarpkgs](https://github.com/pkgforge/soarpkgs) | Declarative package manifests. Each one says where a package comes from and pins the artifact by checksum, rather than building it. Browse it at [soarpkgs.qaidvoid.dev](https://soarpkgs.qaidvoid.dev). |
| [builds](https://github.com/pkgforge/builds) | Builds the packages upstream does not ship itself, published as releases that soarpkgs pins like any other source. |
| [sbuilder](https://github.com/pkgforge/sbuilder) | The `sbuild` toolchain: resolve current versions, pin and hash artifacts, validate the tree, and generate metadata. |

### Desktop

| Project | Description |
|---------|-------------|
| [aeris](https://github.com/pkgforge/aeris) | A GUI that drives the package managers already installed, soar included. Experimental. |
| [aeris-registry](https://github.com/pkgforge/aeris-registry) | Adapter manifests, so teaching aeris a new package manager means writing TOML rather than code. |
| [aeris-metadata](https://github.com/pkgforge/aeris-metadata) | Icons and package name mappings, for managers that ship neither. |

### Sub-Organizations

| Organization | Purpose |
|--------------|---------|
| [PkgForge-Dev](https://github.com/pkgforge-dev) | Portable builds, mostly AppImages, for software that ships none of its own. One repository per project, and soarpkgs pins what they release like any other upstream. |
| [PkgForge-Security](https://github.com/pkgforge-security) | Security tools and research. |

---

## Get Involved

Most of what we need is small and self-contained. Pick whichever fits what you feel like doing:

- **Add a package.** A manifest in [soarpkgs](https://github.com/pkgforge/soarpkgs) is a short TOML file saying where the thing lives and what its checksum is. [The format](https://github.com/pkgforge/soarpkgs/blob/main/docs/FORMAT.md) fits on one page, and `sbuild` fills in the hashes for you.
- **Package something nobody has.** If upstream ships no portable build, [pkgforge-dev](https://github.com/pkgforge-dev) is where a new AppImage repo goes.
- **Teach aeris a package manager.** An adapter in [aeris-registry](https://github.com/pkgforge/aeris-registry) is TOML declaring which commands to run. No Rust required.
- **Find a missing icon.** Plenty of packages in [aeris-metadata](https://github.com/pkgforge/aeris-metadata) still have none, and tracking one down in the project's own repository takes a couple of minutes. Every one is checked before it ships.
- **Tell us what broke.** Bug reports on the repo it happened in are worth more than a star.

---

## AI Policy

AI-assisted contributions are welcome. We do not ask what wrote your patch, and the answer is not held against you. What matters is whether it is correct, whether you understand it, and whether you ran it. That is the same standard a hand-written patch meets.

It does rule out four things:

- **Read what you send.** A pull request you have not reviewed, cannot explain, and did not test is not a contribution. Volume does not substitute for any of the three.
- **Do not open issues you have not reproduced.** A generated bug report costs more time than a bad patch, because the behaviour it describes may never have happened.
- **Do not send generated security reports.** A plausible vulnerability that does not exist takes attention away from one that does. Report what you have confirmed, through [SECURITY.md](https://github.com/pkgforge/soarpkgs/blob/main/SECURITY.md).
- **Never invent a URL, a hash, or a version.** In [soarpkgs](https://github.com/pkgforge/soarpkgs) every one of those is checked against the real artifact, so a guessed value fails `sbuild validate` rather than shipping. Run the tooling first and it will tell you what it would tell us.

None of this is specific to AI, and we would ask it of anyone. AI is just what made it cheap to produce work that skipped all four, which is the only reason it needs saying.

---

### Community

Join the conversation on Discord:

<a href="https://discord.gg/djJUs48Zbu">
    <img src="https://github.com/user-attachments/assets/5a336d72-6342-4ca5-87a4-aa8a35277e2f" width="18" height="18">
    <strong>PkgForge Discord</strong>
</a> `➼` <code>https://discord.gg/djJUs48Zbu</code>
