# RPI 5 UEFI 0.2.9 [Soulveig Edition]

## English

### Changes since 0.2.8

- Restores the `FANC` / `RPI0003` ACPI device required by the ESXi `rpitherm`
  temperature and fan-control driver.
- Exposes only the five narrow mailbox, clock, PWM1, GPIO45 and pad-control
  MMIO resources required by the driver; no shared RP1 interrupt is assigned.

## Русский

### Изменения относительно 0.2.8

- Восстановлено ACPI-устройство `FANC` / `RPI0003`, необходимое драйверу
  температуры и вентилятора `rpitherm` для ESXi.
- Опубликованы только пять узких MMIO-ресурсов mailbox, clock, PWM1, GPIO45 и
  управления pads; общее прерывание RP1 устройству не назначается.
