# heliosminer-cg

A modern command-line CPU/GPU miner for NVIDIA and AMD GPUs, x64 and ARM64 CPUs, running on Windows and Linux hosts.

## Download

Get the latest version from [Releases](https://github.com/heliospool/heliosminer-cg/releases).

| File | For |
|---|---|
| `heliosminer-cg-<version>-windows-x64.zip` | Windows, 64-bit |
| `heliosminer-cg-<version>-linux-x64.tar.gz` | Linux, 64-bit x86: Ubuntu 22.04, Debian 12 and later |
| `heliosminer-cg-<version>-linux-arm64.tar.gz` | Linux, 64-bit ARM, a Raspberry Pi among them |
| `heliosminer-cg-<version>.sha256` | checksums for the files above |

## Algorithms

| Algorithm | Option | Coins |
|---|---|---|
| SHA256d (the default) | `-a sha256d` | BTC, BCH, DGB, CHTA and others |
| Allium | `-a allium` | Garlicoin and others |

## Features

- GPU mining on AMD and NVIDIA through OpenCL
- Optimized Allium mining on NVIDIA through CUDA
- Stratum v1 for both algorithms, Stratum v2 for SHA256d
- Web and terminal dashboards
- Built in API endpoints for monitoring and tooling support
- GPU temperature, fan, power and clock readings for supported devices
- Guided setup on the first run when no pool is given
- Autotune picks the best performing CPU and GPU settings while it mines
- GPU temperature target reduces load at limit
- Auto restart on error
- Custom logging for Screen, Web and File

## Quick start

    heliosminer-cg -a {sha256d, allium} -o stratum+tcp://pool:port -u wallet -p x

Launchers are included: `start-mining-sha256d` and `start-mining-allium` (`.bat` on Windows,
`.sh` on Linux). Set `POOL` and `WALLET` in one, then run it.

Web dashboard: `http://<miner address>:8028`

All options: `heliosminer-cg --help`, and the README included in the download.

## Reporting a problem

Open an [issue](https://github.com/heliospool/heliosminer-cg/issues) with:

- the output of `heliosminer-cg --version`
- the log file
