# Raspberry Pi 5 UEFI v0.2.7 [Soulveig Edition]

## English

### Changes since 0.2.6

- Updated the EDK2 base to `edk2-stable202608` while retaining UEFI 2.11 and Shell 2.2 reporting.
- Restored early LZMA decompression required by the Raspberry Pi firmware volume layout.
- Ported BCM2712 SD signaling control to the new SD/MMC API and synchronized the SDHCI and external signaling path during 3.3 V/1.8 V transitions.
- Retained the SD `CMD6` response CRC/index workaround, restoring microSD visibility in Boot Manager and writable access to `RPI_EFI.fd`.
- Restored persistent UEFI settings and verified that fan settings survive reset.
- Added SoC temperature refresh every 5 seconds without changing the selected menu focus.

## Русский

### Изменения относительно 0.2.6

- База EDK2 обновлена до `edk2-stable202608` с сохранением отображения UEFI 2.11 и Shell 2.2.
- Возвращена ранняя LZMA-декомпрессия, необходимая для структуры firmware volume Raspberry Pi.
- Управление напряжением SD на BCM2712 перенесено на новый API SD/MMC; SDHCI и внешний сигнальный тракт синхронно переключаются между 3,3 В и 1,8 В.
- Сохранён workaround CRC/индекса ответа SD `CMD6`, благодаря чему microSD снова видна в Boot Manager, а `RPI_EFI.fd` доступен для записи.
- Восстановлено сохранение настроек UEFI; сохранение параметров вентилятора после reset подтверждено на оборудовании.
- Температура SoC обновляется каждые 5 секунд без сброса выбранного пункта меню.
