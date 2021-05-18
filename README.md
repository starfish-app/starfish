# Starfish

A Gemini browser for elementary OS.

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](COPYING)

![Starfish Screenshot](data/screenshot.png?raw=true)

## About

Starfish is a graphical client for the Gemini protocol built with GTK and Vala. The main goal of the project is to provide a native looking elementary OS application for reading Gemini sites. Read more on the project's Gemini page: [Starfish](gemini://josipantolis.from.hr/starfish/).

### Status

Starfish is currently in early development stage. It can already be used to surf Geminispace. It renders Gemtext pages and has basic support for viewing images. It supports user input as its defined in the Gemini spec. However, there are many missing features, such as client certificates, subscriptions, favorites, tabs, etc.

One of the missing features is the inclusion in package managers / app stores. Currently the only way to install Starfish is to compile it locally.

## Compile

All prerequisites can be met by installing `elementary-sdk`:

```sh
sudo apt install elementary-sdk
```

To build and install the app execute (from project's root directory):

```sh
meson build --prefix=/usr
cd build
ninja
sudo ninja install
```

### Test

After performing meson build you can run tests from inside `build` directory with:

```sh
meson test
```

### Translate

After adding user facing strings, remember to wrap them `_("like so")`, from inside the `build` directory execute:

```sh
ninja hr.from.josipantolis.starfish-pot
ninja hr.from.josipantolis.starfish-update-po
```

## License

[GNU GPLv3](COPYING)
Copyright © 2021 Josip Antoliš, josip.antolis@protonmail.com.

