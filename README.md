# Dashchan Extension: dvach (/po fork)

Это форк dvach-расширения Dashchan с возможностью просмотра лайков в /po, /news и некоторых других разделах.

## Установка:
1. Если у вас установлено оригинальное расширение двача от Mishiranu, удалите его вручную (Настройки -> Форумы -> 2ch.hk -> Удалить расширение).
2. Скачайте и установите это расширение: [DashchanDvachPoLikes.apk](https://raw.githubusercontent.com/f77/Dashchan-Extensions/master/update/package/DashchanDvachPoLikes.apk)
3. Выключите частичную загрузку тредов, чтобы изменения лайков отображались сразу же после перезагрузки страницы. (Настройки -> Форумы -> 2ch.hk -> Частичная загрузка тредов).

## The original Mishiranu dvach extension on which this fork version is based:
[DashchanDvach.apk](https://raw.githubusercontent.com/f77/Dashchan-Extensions/master/update/package/DashchanDvach.apk)


# Dashchan Extensions

This repository is designed to store Dashchan extensions source code.

The source code is available in specific branch for every extension.

Use `git clone -b %CHAN_NAME% https://github.com/Mishiranu/Dashchan-Extensions` to clone specific branch.

Video player libraries extension is located in the [neighboring repository](https://github.com/Mishiranu/Dashchan-Webm).

General dependencies: [Public API](https://github.com/Mishiranu/Dashchan-Library), [Static Library](https://github.com/Mishiranu/Dashchan-Static).

## Building Guide

1. Install JDK 8 or higher
2. Install Android SDK, define `ANDROID_HOME` environment variable or set `sdk.dir` in `local.properties`
3. Install Gradle
4. Run `gradle assembleRelease`

The resulting APK file will appear in `build/outputs/apk` directory.

The API library may be updated. Use `gradle --refresh-dependencies assembleRelease` to build, then.

### Build Signed Binary

You can create `keystore.properties` in the source code directory with the following properties:

```properties
store.file=%PATH_TO_KEYSTORE_FILE%
store.password=%KEYSTORE_PASSWORD%
key.alias=%KEY_ALIAS%
key.password=%KEY_PASSWORD%
```
