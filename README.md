# AncesTale-final

**Version 0.7.9 Developer Preview**

AncesTale-final is an open-source desktop application exploring genealogy and interactive historical storytelling. Developed by Jeremiah Burke O'Neal using C++ and Qt 6.

## Screenshot

![AncesTale-final](docs/screenshot.png)

## About this preview

- Genealogy and historical storytelling interface
- Fictional sample family records
- Offline desktop environment
- Snap and Flatpak packaging for x86-64 Linux

External integrations are disabled. Signing, live multiplayer, voice, server deployment and AI automation are not working public features in this preview. Installation and launch have been tested; multimedia playback remains unverified.

## Install using Snap

```sh
sudo snap install ancestale-final --edge
```

[Snap Store](https://snapcraft.io/ancestale-final)

## Install using Flatpak

Download the bundle from the [GitHub release](https://github.com/we6jbo/AncesTale-final/releases/tag/v0.7.9-preview).

```sh
flatpak install --user --bundle ancestale-final_0.7.9_x86_64.flatpak
flatpak run io.github.we6jbo.AncesTaleFinal
```

Requires the KDE 6.11 runtime. Flathub publication is deferred.

## Build from source

Requires CMake, a C++17 compiler, Qt 6 (Widgets, Network, Multimedia), and OpenSSL development libraries.

```sh
git clone https://github.com/we6jbo/AncesTale-final.git
cd AncesTale-final
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --parallel 2
./build/AncesTale-final
```

## License

The current edition is distributed under GPL-3.0-only. Earlier source editions remain available under their respective tags: `v0.7.9-mit`, `v0.7.9-apache2`, and `v0.7.9-gpl3`.

Previous license documents and copyright notices are preserved in the LICENSES directory.

Qt, OpenSSL and multimedia dependencies retain their respective licenses and applicable third-party notices.

## Development blog

[AncesTale-final Goes Public](https://j03.page/2026/11/15/ancestale-final-goes-public/) (forthcoming; URL provisional).

## Download verification

Download both packages and `SHA256SUMS.txt` from the GitHub release into the same directory, then run:

```sh
sha256sum -c SHA256SUMS.txt
```

Copyright 2026 Jeremiah Burke O'Neal.
