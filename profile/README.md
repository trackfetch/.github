<p align="center">
  <img src="assets/logo.png" alt="trackfetch logo" width="128">
</p>

<h1 align="center">trackfetch</h1>

<p align="center">A text file of songs in, tagged MP3s with cover art out.</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
    <img alt="trackfetch: a text file of songs in, tagged MP3s with cover art out" src="assets/banner-light.svg" width="800">
  </picture>
</p>

English | [Українська](README.uk.md) | [Русский](README.ru.md)

trackfetch reads a plain text file with one `Artist - Title` per line. For
each song it takes metadata and cover art from configurable free sources,
picks the best-matching YouTube audio and saves an MP3 with full ID3 tags.
A run can be interrupted at any point and resumed later, even with a
thousand songs in the list.

- **Configurable metadata.** iTunes (default), Deezer, MusicBrainz, VocaDB
  and optional Spotify.
- **Album art.** Taken from the winning metadata source, then the Cover Art
  Archive for MusicBrainz, then YouTube thumbnails.
- **Correct download.** trackfetch scores five YouTube results per song.
  Official audio wins; covers, karaoke, nightcore, sped-up, slowed, remix
  and reaction versions lose.
- **Format of choice.** MP3 for any player, or Opus and M4A, which keep
  YouTube's original audio without re-encoding.
- **Resume where you stopped.** Downloaded songs go to `done.txt` and are
  skipped next run. Failures land in `failed.txt` with the reason.
- **Plays everywhere.** Tags are written as ID3v2.3, understood by Windows
  Explorer, Apple Music, Android, car stereos and most players.
- **Any alphabet.** Cyrillic and other non-Latin titles are matched
  correctly and kept in file names.
- **No Python required.** Prebuilt binaries for Linux, macOS and Windows on
  x86_64 and ARM64.

## Install

Pick one. Homebrew and Nix also install yt-dlp, FFmpeg and Deno for you;
with the other ways you need them separately. The default iTunes source
needs no API key. A free Spotify API key is optional and only needed if you
select Spotify.

pipx (Python 3.10+):

    pipx install trackfetch

Homebrew (macOS and Linux):

    brew install trackfetch/tap/trackfetch

Nix (Linux and Apple Silicon Macs):

    nix profile install github:trackfetch/trackfetch

Standalone binaries for Linux, macOS and Windows (x86_64 and ARM64) are on
the [releases page](https://github.com/trackfetch/trackfetch/releases/latest).

## Repository

- Main repository: <https://github.com/trackfetch/trackfetch>
- PyPI: <https://pypi.org/project/trackfetch/>
- Documentation: the [README](https://github.com/trackfetch/trackfetch#readme)
  covers configuration, metadata and music sources, troubleshooting and the
  tldr cheat sheet
- Homebrew tap: <https://github.com/trackfetch/homebrew-tap>

## Contributing

Bug reports, matching improvements, docs fixes and translations are welcome.
See [CONTRIBUTING.md](https://github.com/trackfetch/trackfetch/blob/master/CONTRIBUTING.md)
for how to report a wrong match and set up a development environment.
Security issues go through
[Security → Report a vulnerability](https://github.com/trackfetch/trackfetch/security/advisories/new),
not a public issue.

## License

[GPL-3.0-or-later](https://github.com/trackfetch/trackfetch/blob/master/LICENSE)
