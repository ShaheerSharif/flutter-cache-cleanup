# Flutter Setup Arch Linux

This flutter setup includes a pacman post transaction hook which clears flutter cache everytime the `flutter-bin` package is installed, upgraded or removed.

## Setup

```sh
# cp zz-99-custom-flutter-cache-clear.hook /etc/pacman.d/hooks/zz-99-custom-flutter-cache-clear.hook
# install -m755 flutter-cache-cleanup /usr/local/bin/flutter-cache-cleanup
```

