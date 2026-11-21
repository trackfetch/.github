<p align="center">
  <img src="assets/logo.png" alt="логотип trackfetch" width="128">
</p>

<h1 align="center">trackfetch</h1>

<p align="center">
  <b>Текстовый файл с песнями на входе, MP3 с тегами и обложками на выходе.</b>
</p>

<p align="center">
  <a href="https://pypi.org/project/trackfetch/"><img alt="PyPI" src="https://img.shields.io/pypi/v/trackfetch?color=3775A9&logo=pypi&logoColor=white"></a>
  <a href="https://pypi.org/project/trackfetch/"><img alt="Python" src="https://img.shields.io/pypi/pyversions/trackfetch?logo=python&logoColor=white"></a>
  <a href="https://github.com/trackfetch/trackfetch/releases/latest"><img alt="Релиз" src="https://img.shields.io/github/v/release/trackfetch/trackfetch?logo=github"></a>
  <a href="https://github.com/trackfetch/trackfetch/blob/master/LICENSE"><img alt="Лицензия" src="https://img.shields.io/badge/license-GPL--3.0--or--later-blue"></a>
</p>

<p align="center">
  <a href="#установка">Установка</a> ·
  <a href="#возможности">Возможности</a> ·
  <a href="https://github.com/trackfetch/trackfetch/blob/master/README.ru.md">Документация</a> ·
  <a href="https://github.com/trackfetch/trackfetch/releases/latest">Релизы</a>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/trackfetch/.github/main/profile/assets/banner-dark.svg">
    <img alt="trackfetch" src="https://raw.githubusercontent.com/trackfetch/.github/main/profile/assets/banner-light.svg" width="800">
  </picture>
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.uk.md">Українська</a> · <b>Русский</b>
</p>

---

trackfetch читает обычный текстовый файл, где на каждой строке записано
`Исполнитель - Название`, подбирает для каждой песни метаданные, обложку и
лучшее аудио на YouTube или SoundCloud и сохраняет файл с полными тегами.
Работу можно прервать в любой момент и продолжить позже, даже если в списке
тысяча песен.

## Возможности

| **Точный подбор**                 | Из пяти результатов YouTube побеждает официальное аудио, а каверы, караоке, nightcore, ремиксы и реакции проигрывают                          |
| --------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Метаданные и обложки**          | iTunes, Deezer, MusicBrainz, VocaDB и необязательный Spotify; обложка из победившего источника, затем Cover Art Archive, затем превью YouTube |
| **Формат на выбор**               | MP3 для любого плеера или Opus и M4A без перекодирования                                                                                      |
| **Продолжение с места остановки** | Скачанные песни записываются в `done.txt`, ошибки с причиной в `failed.txt`                                                                   |
| **Любой алфавит**                 | Кириллица и другие нелатинские названия правильно сопоставляются и сохраняются                                                                |
| **Python не нужен**               | Бинарники для Linux, macOS и Windows на x86_64 и ARM64                                                                                        |

## Установка

Homebrew и Nix сами ставят yt-dlp, FFmpeg и Deno, при остальных способах их
нужно поставить отдельно. Источнику iTunes по умолчанию ключ API не нужен.

**pipx** (Python 3.10+)

```bash
pipx install trackfetch
```

**Homebrew** (macOS и Linux)

```bash
brew install trackfetch/tap/trackfetch
```

**Nix** (Linux и Mac на Apple Silicon)

```bash
nix profile install github:trackfetch/trackfetch
```

Готовые бинарники лежат на странице
[релизов](https://github.com/trackfetch/trackfetch/releases/latest).

## Ссылки

- [PyPI](https://pypi.org/project/trackfetch/)
- [Документация](https://github.com/trackfetch/trackfetch/blob/master/README.ru.md): конфигурация, источники метаданных и музыки, решение проблем
- [Homebrew tap](https://github.com/trackfetch/homebrew-tap)

## Участие в проекте

Отчёты об ошибках, улучшения подбора, правки документации и переводы
приветствуются. Как сообщить о неправильном совпадении и настроить среду
разработки, написано в
[CONTRIBUTING.md](https://github.com/trackfetch/trackfetch/blob/master/CONTRIBUTING.md).
Вопросы безопасности передавайте через
[Security → Report a vulnerability](https://github.com/trackfetch/trackfetch/security/advisories/new),
а не через публичный issue.

<p align="center">
  <sub>Лицензия <a href="https://github.com/trackfetch/trackfetch/blob/master/LICENSE">GPL-3.0-or-later</a></sub>
</p>