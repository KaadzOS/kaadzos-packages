<div align="center">
  <img src="https://raw.githubusercontent.com/KaadzOS/.github/main/assets/kaadzoslogo.png" alt="KaadzOS" width="100%">
</div>

<p align="center">
  <sub>APT FRONT END &nbsp;·&nbsp; PKEXEC / SUDO &nbsp;·&nbsp; ZENITY</sub>
</p>

<p align="center">
  <strong>GUI manners, shell guts.</strong><br>
  Every name is one argument. Every privileged step asks first.
</p>

<p align="center">
  <a href="https://kaadzos.pages.dev/docs/">Manual</a> &nbsp;·&nbsp;
  <a href="https://kaadzos.pages.dev">Website</a> &nbsp;·&nbsp;
  <a href="https://github.com/KaadzOS/KaadzOS/blob/main/config/includes.chroot/usr/local/bin/kaadzos-packages">Helper source</a> &nbsp;·&nbsp;
  <a href="https://github.com/KaadzOS/KaadzOS/blob/main/packs/admin.pack">Admin pack</a>
</p>

## Skeleton, on purpose

`kaadzos-packages` currently ships from the main monorepo as a POSIX-sh front end behind `$mod+Shift+p`, the Waybar package module and the **Packages** desktop entry. This repository is the stable address for package-front-end work if it ever earns an independent cycle.

| Piece | Where it actually lives |
| --- | --- |
| Front end | [`kaadzos-packages`](https://github.com/KaadzOS/KaadzOS/blob/main/config/includes.chroot/usr/local/bin/kaadzos-packages) |
| Safe file actions | [`kaadzos-file-action`](https://github.com/KaadzOS/KaadzOS/blob/main/config/includes.chroot/usr/local/bin/kaadzos-file-action) |
| Synaptic and pkexec | [`packs/admin.pack`](https://github.com/KaadzOS/KaadzOS/blob/main/packs/admin.pack) |
| Tests | [`ci/test-packages.sh`](https://github.com/KaadzOS/KaadzOS/blob/main/ci/test-packages.sh) |

## The boundary

The helper validates a package name, passes it as one argv, confirms destructive actions with a cancel default, and keeps failed apt output in `~/.cache/kaadzos/apt.log`. No wrapper daemon, no new runtime.

## Licence

MIT; see [`LICENSE`](LICENSE).

<sub>Debian is a registered trademark of Software in the Public Interest, Inc. KaadzOS is an independent project.</sub>
