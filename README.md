# MinUI Zero kernel source

GPL-2.0 corresponding source for the Linux kernel that [MinUI Zero](https://github.com/Zero-Labs-CFW/MinUI-Zero) ships on the TrimUI Brick, Brick Pro and Smart Pro. The tarballs are attached to this repo's releases, one release per kernel build.

| Kernel build | First shipped in | Source | Base kernel |
|---|---|---|---|
| 4.9.191-zero (ship10) | MinUI Zero v1.10.0 | `zero-tg5040-kernel-4.9.191-zero-ship10-src.tar.gz` | `linux-4.9.191-a133.tar.xz` |

## ship10

- **Source:** `zero-tg5040-kernel-4.9.191-zero-ship10-src.tar.gz`, sha256 `09be0b470b138f615125722e97302d29be1a617c2807d26a6265a4f5141d3960`. Every patch in order, the kernel config, the build scripts, the toolchain Dockerfile and the source of the built-in init (zinit). It rebuilds the shipped files byte for byte (Image md5 `8ba3c20ee111a6562d4d08f55f642e23`, zero-recovery.img md5 `00a9ee1e92378cfc3313e73e83f8b24d`).
- **Base kernel:** `linux-4.9.191-a133.tar.xz`, sha256 `93710f3a1f1a54678641fe15b7898fd64bc151b63377ac698c5eced8806fa743`. Allwinner's Linux 4.9.191 for the A133, as Creality's Sonic Pad SDK has it (`CrealityTech/sonic_pad_os` at `7f37a7f`, `lichee/linux-4.9`), as packed by [plastron](https://github.com/ericreinsmidt/plastron).
- **Patches and build method** come from plastron by Eric Reinsmidt (at `b897f7c`), with MinUI Zero's own patches on top.

The PowerVR GPU libraries and firmware that ship with the kernel are Imagination Technologies' closed binaries, unmodified; no source exists for them. The full notice ships on the device as `LICENSES/zero-kernel/NOTICE.txt` and in MinUI Zero's [`THIRD_PARTY_NOTICES.md`](https://github.com/Zero-Labs-CFW/MinUI-Zero/blob/main/THIRD_PARTY_NOTICES.md).

Linux is licensed under the GNU General Public License version 2; see `COPYING`.
