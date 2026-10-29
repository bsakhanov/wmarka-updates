# Серверы обновлений Webmarka

Joomla проверяет новые версии расширений и скачивает архивы без входа в GitHub, поэтому из закрытого репозитория сервер обновлений не работает. Здесь лежат списки версий (`updates.xml`), журналы изменений для Joomla (`changelog.xml`) и — в выпусках этого репозитория — архивы расширений, исходники которых закрыты.

| Расширение | Сервер обновлений (адрес из манифеста) | Выпуски |
| --- | --- | --- |
| Webmarka Feeds (`plg_system_wmarkafeeds`) | `https://raw.githubusercontent.com/bsakhanov/wmarka-updates/main/plg_system_wmarkafeeds/updates.xml` | теги `plg_system_wmarkafeeds-vВЕРСИЯ` |

Файлы пишет сценарий выпуска в репозитории самого расширения (для Webmarka Feeds — `tools/release.py`); руками здесь ничего не правится. Тег выпуска — `<элемент>-v<версия>`, к выпуску прикладываются архив расширения и `SHA256SUMS.txt`; SHA-256 архива записан и в `updates.xml`, Joomla сверяет его перед установкой.

Открытые расширения Webmarka (модули Webmarka Articles, шаблоны wmarka и wmarka clean) держат сервер обновлений в своих репозиториях.

---

**Webmarka update servers.** Joomla checks for updates and downloads archives without signing in to GitHub, so an update server cannot live in a private repository. This repository holds the version lists, Joomla changelogs and release archives of Webmarka extensions whose sources are private. The files are written by each extension's release script; do not edit them by hand.
