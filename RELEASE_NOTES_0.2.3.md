# Raspberry Pi 5 UEFI 0.2.3 [Soulveig Edition]

## English

### Changes since 0.2.2

- Added a five-line hardware and firmware identification banner to the UEFI main screen.
- Shows the PCB revision, full board revision code and C1/D0 stepping.
- Shows the Raspberry Pi serial number and bootloader EEPROM build date; unavailable values are displayed as `N/A`.
- Shows `BCM2712 (ARM Cortex-A76)`, CPU clock and RAM capacity in GB on one line.
- Shows Soulveig Edition, UEFI specification and Shell versions on one line.
- Shows `SoC Temperature: N/A` when the temperature mailbox request is unavailable.
- Retains SoC temperature display and the existing fan, ACPI, microSD CMD6 and NVRAM fixes from 0.2.2.
- Uses automatic Device Tree selection. The release package does not force a D0 DTB and is not D0-only.

### Hardware validation

- Booted on three Raspberry Pi 5 boards with EEPROM `2026-06-17`.
- Automatic Device Tree selection reports one tested board as BCM2712 C1 and two as D0.
- UEFI boot and the new identification banner were verified.
- In the initial cold-boot checks the C1 board detected microSD immediately; both D0 boards required one warm reset before microSD appeared. Keep rollback media and physical access during testing.

## Русский

### Изменения относительно 0.2.2

- На главный экран UEFI добавлены пять строк идентификации оборудования и прошивки.
- Показываются PCB revision, полный revision code и stepping C1/D0.
- Показываются серийный номер Raspberry Pi и дата сборки bootloader EEPROM; недоступные значения выводятся как `N/A`.
- В одной строке показываются `BCM2712 (ARM Cortex-A76)`, частота CPU и объём RAM в GB.
- В одной строке показываются Soulveig Edition, версия спецификации UEFI и версия Shell.
- Если mailbox-запрос температуры недоступен, выводится `SoC Temperature: N/A`.
- Сохранены отображение температуры SoC, управление вентилятором, ACPI, исправление microSD CMD6 и сохранение NVRAM из версии 0.2.2.
- Используется автоматический выбор Device Tree. Пакет не принуждает D0 DTB и не предназначен только для D0.

### Аппаратная проверка

- Проверена загрузка на трёх Raspberry Pi 5 с EEPROM `2026-06-17`.
- При автоматическом выборе Device Tree одна плата определяется как BCM2712 C1, две как D0.
- Проверены загрузка UEFI и новые строки идентификации.
- В первых cold-boot тестах плата C1 определила microSD сразу; на обеих D0 потребовался один warm reset. При тестировании сохраняйте рабочий носитель для отката и физический доступ к плате.
