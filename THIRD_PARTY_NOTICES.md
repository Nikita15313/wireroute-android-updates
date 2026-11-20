# Сторонние компоненты WireRoute 3.1.14

## WireGuard Android

Java-библиотека и инструменты WireGuard поставляются с артефактом `com.wireguard.android:tunnel:1.0.20260102`. Библиотека использует Apache License 2.0. Программа WireRoute не связана с проектом WireGuard. WireGuard является зарегистрированным товарным знаком Jason A. Donenfeld.

Исходники и скрипты сборки доступны рядом с выпуском.

- [WireGuard Android 1.0.20260102](third-party/sources/wireguard-android-1.0.20260102-09b75c2bd37f749e2a8c85876394854113c74be7.zip), коммит `09b75c2bd37f749e2a8c85876394854113c74be7`. В архиве находятся Gradle, CMake и файлы совместимости с Android NDK.
- [WireGuard tools](third-party/sources/wireguard-tools-e2ecaaa739144997ccff89d6ad6ec81698ea6ced.zip), подмодуль `e2ecaaa739144997ccff89d6ad6ec81698ea6ced`, из которого собираются `libwg.so` и `libwg-quick.so`. [GNU GPL версии 2](third-party/licenses/WireGuard-Tools-COPYING.txt).
- [Termux ELF Cleaner](third-party/sources/elf-cleaner-7efc05090675ec6161b7def862728086a26c3b1f-source.zip), подмодуль `7efc05090675ec6161b7def862728086a26c3b1f`. Это утилита сборки. Архив содержит её исходники, лицензию и скрипты.

Для сборки инструментов распакуйте WireGuard Android и поместите содержимое двух архивов подмодулей в `tunnel/tools/wireguard-tools` и `tunnel/tools/elf-cleaner`. Используйте `tunnel/tools/CMakeLists.txt` и конфигурацию Gradle из архива Android. [Лицензия WireGuard Android](third-party/licenses/WireGuard-Android-COPYING.txt).

WireRoute использует нативный адаптер ввода и вывода пакетов поверх `wireguard-go`. Исходники адаптера находятся в [репозитории USB Bridge](https://github.com/Nikita15313/usb-bridge/tree/v0.15.8/source/wireroute-next/native). Go-модуль WireGuard закреплён на версии `v0.0.0-20250521234502-f333402bd9cb`. [Лицензия wireguard-go](https://github.com/WireGuard/wireguard-go/blob/f333402bd9cb/LICENSE).

## AndroidX и десугаринг Java

- Интерфейс использует `androidx.drawerlayout:drawerlayout:1.2.0` и его зависимости. [Лицензия AndroidX Apache 2.0](https://raw.githubusercontent.com/androidx/androidx/androidx-main/LICENSE.txt).
- Пакет `com.android.tools:desugar_jdk_libs:2.1.5` включает компоненты OpenJDK. Он распространяется под GPL версии 2 с исключением Classpath для обозначенных файлов. [Исходники 2.1.5](third-party/sources/desugar-jdk-libs-2.1.5-73170c345e6a762fc6a1f0301bb15218850023ef.zip) содержат лицензию и файлы сборки. [Лицензия и исключение](third-party/licenses/Desugar-JDK-LICENSE.txt).

## Режим интернета через USB

Режим USB использует hev-socks5-tunnel, hev-task-system, lwIP и libyaml. Копии уведомлений и лицензий находятся в [third-party/licenses](third-party/licenses/). Просмотреть исходники интеграции можно в [USB Bridge 0.15.8](https://github.com/Nikita15313/usb-bridge/tree/v0.15.8/source).

Контрольные суммы архивов находятся в [third-party/sources/SHA256SUMS](third-party/sources/SHA256SUMS).
