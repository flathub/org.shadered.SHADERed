# Flatpak for SHADERed

## Installation

This Flatpak is available on
[Flathub](https://flathub.org/apps/details/org.shadered.SHADERed).
After following the [Flatpak setup guide](https://flatpak.org/setup/),
you can install it by entering the following command in a terminal:

```bash
flatpak install --user flathub org.shadered.SHADERed -y
```

Once the Flatpak is installed, you can run SHADERed using your desktop environment's
application launcher.

## Updating

This Flatpak follows the latest stable SHADERed version.
To update it, run the following command in a terminal:

```bash
flatpak update
```

## Building from source

Install Git, follow the
[flatpak-builder setup guide](https://docs.flatpak.org/en/latest/first-build.html)
then enter the following commands in a terminal:

```bash
git clone --recursive https://github.com/flathub/org.shadered.SHADERed.git
cd org.shadered.SHADERed/
flatpak install --user flathub org.freedesktop.Sdk//24.08 -y
flatpak-builder --force-clean --install --user -y builddir org.shadered.SHADERed.yaml
```

If all goes well, the Flatpak will be installed after building. You can then
run it using your desktop environment's application launcher.

You can speed up incremental builds by installing [ccache](https://ccache.dev/)
and specifying `--ccache` in the flatpak-builder command line (before `builddir`).
