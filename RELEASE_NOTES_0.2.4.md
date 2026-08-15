# Raspberry Pi 5 UEFI 0.2.4 [Soulveig Edition]

## English

### Changes since 0.2.3

- Updated the EDK2 base to upstream commit `2970e5699ba6267f3384ffab20f96647578aebc8` dated 2026-08-12.
- Updated the reported UEFI specification revision from 2.70 to 2.11.
- Kept the UEFI Shell protocol at its actual version 2.2.
- Ported the Raspberry Pi 5 platform to the current PeilessSec, ARM MMU, exception-handler, FDT, ACPI and GPT library interfaces required by the new EDK2 base.
- Retained the established PL011 serial implementation; the incompatible dual-serial experimental bindings are not part of this release.
- Retained the fan control, ESXi ACPI devices, microSD CMD6 workaround, NVRAM persistence, SoC temperature and board-identification features from 0.2.3.
- Updated the SMBIOS and main-screen release string to `RPI 5 UEFI 0.2.4 [Soulveig Edition]`.

### Hardware validation

- The complete EDK2 2.11 source and platform configuration booted successfully on Raspberry Pi 5 under the final `0.2.4-AE` validation label.
- The published `0.2.4` image is rebuilt from that same source and configuration; the only intentional source-level difference is the release label change from `0.2.4-AE` to `0.2.4`.
- Keep the previous 0.2.3 image and physical access available for rollback.

## Русский

### Изменения относительно 0.2.3

- Основа EDK2 обновлена до upstream-коммита `2970e5699ba6267f3384ffab20f96647578aebc8` от 2026-08-12.
- Сообщаемая версия спецификации UEFI обновлена с 2.70 до 2.11.
- Протокол UEFI Shell сохранён в его фактической версии 2.2.
- Платформа Raspberry Pi 5 перенесена на актуальные интерфейсы PeilessSec, ARM MMU, обработчиков исключений, FDT, ACPI и GPT, необходимые новой базе EDK2.
- Сохранена проверенная реализация PL011; несовместимые экспериментальные dual-serial-привязки в релиз не включены.
- Сохранены управление вентилятором, ACPI-устройства ESXi, исправление microSD CMD6, сохранение NVRAM, температура SoC и идентификация платы из версии 0.2.3.
- Строка версии SMBIOS и главного экрана обновлена до `RPI 5 UEFI 0.2.4 [Soulveig Edition]`.

### Аппаратная проверка

- Полная конфигурация EDK2 2.11 и платформы успешно загрузилась на Raspberry Pi 5 под финальной проверочной меткой `0.2.4-AE`.
- Публикуемый образ `0.2.4` пересобран из тех же исходников и конфигурации; единственное намеренное отличие на уровне исходников — смена релизной метки `0.2.4-AE` → `0.2.4`.
- Для отката сохраняйте предыдущий образ 0.2.3 и физический доступ к плате.
