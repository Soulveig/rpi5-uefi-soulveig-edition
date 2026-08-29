# RPI 5 UEFI 0.2.8 [Soulveig Edition]

## English

### Changes since 0.2.7

- Reads the Raspberry Pi factory board MAC through the firmware protocol and
  programs it into the RP1 Cadence GEM SA1 registers before ESXi starts.
- Enables the RP1 GEM ESXi driver to use the unique board MAC without a module
  parameter or generated fallback address.

## Русский

### Изменения относительно 0.2.7

- Заводской MAC платы Raspberry Pi читается через firmware-протокол и
  записывается в регистры SA1 контроллера Cadence GEM в RP1 до запуска ESXi.
- Драйвер RP1 GEM для ESXi получает уникальный MAC платы без параметра модуля
  и без сгенерированного fallback-адреса.
