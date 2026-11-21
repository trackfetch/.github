<p align="center">
  <img src="assets/logo.png" alt="логотип trackfetch" width="128">
</p>

<h1 align="center">trackfetch</h1>

<p align="center">Текстовий файл із піснями на вході, MP3 з тегами та обкладинками на виході.</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
    <img alt="trackfetch: текстовий файл із піснями на вході, MP3 з тегами та обкладинками на виході" src="assets/banner-light.svg" width="800">
  </picture>
</p>

[English](README.md) | Українська | [Русский](README.ru.md)

trackfetch читає звичайний текстовий файл, де в кожному рядку записано
`Виконавець - Назва`. Для кожної пісні він бере метадані й обкладинку з
налаштовуваних безкоштовних джерел, обирає найвідповідніше аудіо на YouTube
і зберігає MP3 з повними ID3-тегами. Роботу можна перервати будь-коли й
продовжити пізніше, навіть якщо у списку тисяча пісень.

- **Налаштовувані метадані.** iTunes (типово), Deezer, MusicBrainz, VocaDB
  і необов'язковий Spotify.
- **Обкладинка альбому.** Береться у джерела метаданих, що перемогло, потім
  з Cover Art Archive для MusicBrainz, потім із прев'ю YouTube.
- **Правильне завантаження.** trackfetch оцінює п'ять результатів YouTube на
  кожну пісню. Офіційне аудіо виграє, а кавери, караоке, nightcore,
  прискорені, сповільнені версії, ремікси та реакції програвють.
- **Формат на вибір.** MP3 для будь-якого плеєра або Opus і M4A, які
  зберігають оригінальний звук YouTube без перекодування.
- **Продовження з місця зупинки.** Завантажені пісні записуються в
  `done.txt` і при наступному запуску пропускаються. Помилки потрапляють у
  `failed.txt` разом із причиною.
- **Грає скрізь.** Теги записуються у форматі ID3v2.3, який розуміють
  Провідник Windows, Apple Music, Android, автомагнітоли та більшість
  плеєрів.
- **Будь-яка абетка.** Кирилиця та інші нелатинські назви правильно
  зіставляються та зберігаються в іменах файлів.
- **Python не потрібен.** Готові бінарники для Linux, macOS і Windows на
  x86_64 та ARM64.

## Встановлення

Вибери будь-який спосіб. Homebrew і Nix самі ставлять yt-dlp, FFmpeg і Deno;
при інших способах їх треба поставити окремо. Джерелу iTunes типово ключ
API не потрібен. Безкоштовний ключ Spotify API необов'язковий і потрібен,
лише якщо вибрати Spotify.

pipx (Python 3.10+):

    pipx install trackfetch

Homebrew (macOS і Linux):

    brew install trackfetch/tap/trackfetch

Nix (Linux і Mac на Apple Silicon):

    nix profile install github:trackfetch/trackfetch

Готові бінарники для Linux, macOS і Windows (x86_64 та ARM64) — на сторінці
[релізів](https://github.com/trackfetch/trackfetch/releases/latest).

## Репозиторій

- Основний репозиторій: <https://github.com/trackfetch/trackfetch>
- PyPI: <https://pypi.org/project/trackfetch/>
- Документація: [README](https://github.com/trackfetch/trackfetch/blob/master/README.uk.md)
  описує конфігурацію, джерела метаданих і музики, розв'язання проблем і
  можливість продовжити перерване завантаження
- Homebrew tap: <https://github.com/trackfetch/homebrew-tap>

## Контриб'ютори

Звіти про помилки, покращення підбору, правки документації та переклади —
вітаються. Дивіться
[CONTRIBUTING.md](https://github.com/trackfetch/trackfetch/blob/master/CONTRIBUTING.md),
як повідомити про неправильний збіг і налаштувати середовище розробки.
Питання безпеки передавайте через
[Security → Report a vulnerability](https://github.com/trackfetch/trackfetch/security/advisories/new),
а не через публічний issue.

## Ліцензія

[GPL-3.0-or-later](https://github.com/trackfetch/trackfetch/blob/master/LICENSE)
