![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/gaofengnan/tigerbeetle-debian/total)
![GitHub Downloads (all assets, latest release)](https://img.shields.io/github/downloads/gaofengnan/tigerbeetle-debian/latest/total)
![GitHub Release](https://img.shields.io/github/v/release/gaofengnan/tigerbeetle-debian)
![GitHub Release Date](https://img.shields.io/github/release-date/gaofengnan/tigerbeetle-debian)

<h1>
   <p align="center">
     <a href="https://tigerbeetle.com/"><img src="https://github.com/gaofengnan/tigerbeetle-debian/blob/main/tigerbeetle-logo.png" alt="tigerbeetle Logo" width="128" style="margin-right: 20px"></a>
     <a href="https://www.debian.org/"><img src="https://github.com/gaofengnan/tigerbeetle-debian/blob/main/debian-logo.png" alt="Debian Logo" width="104" style="margin-left: 20px"></a>
     <br>tigerbeetle for Debian
   </p>
</h1>
<p align="center">
 The financial transactions database designed for mission critical safety and performance to power the next 30 years of <a href="https://docs.tigerbeetle.com/concepts/oltp">OLTP</a>
</p>

# tigerbeetle for Debian

> Fork of [dariogriffo/tigerbeetle-debian](https://github.com/dariogriffo/tigerbeetle-debian) (MIT); the original packaging is by Dario Griffo. Served at [deb.gaofn.xyz](https://deb.gaofn.xyz) for Debian 12 (bookworm) and 13 (trixie).

This repository contains build scripts to produce the _unofficial_ Debian packages
(.deb) for [tigerbeetle](https://github.com/tigerbeetle/tigerbeetle) hosted at [deb.gaofn.xyz](https://deb.gaofn.xyz)

Currently supported Debian distros are:
- Bookworm (v12)
- Trixie (v13)
- Forky (v14)
- Sid (testing)

Thanks to @ranjithrajv

Supported architectures:
- amd64 (x86_64) - All distributions
- arm64 (aarch64) - All distributions
- armel (ARM EABI) - All distributions

This is an unofficial community project to provide a package that's easy to
install on Debian. If you're looking for the tigerbeetle source code, see [tigerbeetle](https://github.com/tigerbeetle/tigerbeetle)

## Install/Update

### The Debian way

```sh
sudo install -d -m 0755 /etc/apt/keyrings
sudo curl -fsSL https://deb.gaofn.xyz/deb.gaofn.xyz.gpg -o /etc/apt/keyrings/deb.gaofn.xyz.gpg
sudo curl -fsSL https://deb.gaofn.xyz/deb.gaofn.xyz.sources -o /etc/apt/sources.list.d/deb.gaofn.xyz.sources
# Debian 12 (bookworm): fetch deb.gaofn.xyz-bookworm.sources instead
sudo apt update
sudo apt install -y tigerbeetle
```

### Manual Installation

1. Download the .deb package for your Debian version available on
   the [Releases](https://github.com/gaofengnan/tigerbeetle-debian/releases) page.
2. Install the downloaded .deb package.

```sh
sudo dpkg -i <filename>.deb
```
## Updating

To update to a new version, just follow any of the installation methods above. There's no need to uninstall the old version; it will be updated correctly.

## Building

### Build for single architecture
```sh
./build.sh <tigerbeetle_version> <build_version> <architecture>
# Example: ./build.sh 0.8.11 1 arm64
```

### Build for all architectures
```sh
./build.sh <tigerbeetle_version> <build_version> all
# Example: ./build.sh 0.8.11 1 all
```

## Roadmap

- [x] Produce a .deb package on GitHub Releases
- [x] Set up a debian mirror for easier updates
- [x] Multi-architecture support (amd64, arm64, armel, armhf, ppc64el, s390x)

## Disclaimer

- This repo is not open for issues related to tigerbeetle. This repo is only for _unofficial_ Debian packaging.
