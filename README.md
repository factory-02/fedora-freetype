# Информация

[![Support](https://cdn-storage.github.io/images/badges/info.support.svg)](https://sysadmins.community/)
[![Documentation](https://cdn-storage.github.io/images/badges/info.documentation.svg)](https://sysadmins.wiki/)
[![Source](https://cdn-storage.github.io/images/badges/info.source.svg)](https://github.com/factory-02/fedora-freetype)
[![Changelog](https://cdn-storage.github.io/images/badges/info.changelog.svg)](CHANGELOG.md)
[![Code of Conduct](https://cdn-storage.github.io/images/badges/info.coc.svg)](https://metainfo.github.io/coc/)
[![Contributing](https://cdn-storage.github.io/images/badges/info.contributing.svg)](https://metainfo.github.io/contributing/)
[![Authors](https://cdn-storage.github.io/images/badges/info.authors.svg)](AUTHORS)
[![Issues](https://cdn-storage.github.io/images/badges/info.issues.svg)](https://github.com/factory-02/fedora-freetype/issues)
[![Repository](https://cdn-storage.github.io/images/badges/repository.rpm.svg)](https://copr.fedorainfracloud.org/coprs/metastore/fedora-freetype/)
[![License](https://cdn-storage.github.io/images/badges/license.gpl-3.0.svg)](LICENSE)
[![Liberapay](https://cdn-storage.github.io/images/badges/donate.liberapay.svg)](https://liberapay.com/metadata/donate)
[![Patreon](https://cdn-storage.github.io/images/badges/donate.patreon.svg)](https://patreon.com/metadata)
[![By METADATA](https://cdn-storage.github.io/images/badges/by.metadata.svg)](https://metadata.foundation/)

SPEC-файл для создания RPM-пакета **freetype**.

## Установка

1. Подключить репозиторий **METASTORE**: `dnf copr enable metastore/fedora-freetype`.
2. Установить пакет: `dnf install freetype`.

## Настройка

В файл `/etc/fonts/local.conf` добавить:

```xml
<?xml version='1.0'?>
<!DOCTYPE fontconfig SYSTEM 'fonts.dtd'>
<fontconfig>
    <match target="font">
        <edit mode="assign" name="rgba">
        <const>rgb</const>
        </edit>
    </match>
    <match target="font">
        <edit mode="assign" name="hinting">
        <bool>true</bool>
        </edit>
    </match>
    <match target="font">
        <edit mode="assign" name="hintstyle">
        <const>hintfull</const>
        </edit>
    </match>
    <match target="font">
        <edit mode="assign" name="antialias">
        <bool>true</bool>
        </edit>
    </match>
    <match target="font">
        <edit mode="assign" name="lcdfilter">
        <const>lcddefault</const>
        </edit>
    </match>
</fontconfig>
```