# RPI 5 UEFI 0.2.9 [Soulveig Edition]

## English

### Changes since 0.2.8

- Restores the `FANC` / `RPI0003` ACPI device required by the ESXi `rpitherm`
  temperature and fan-control driver.
- Exposes only the five narrow mailbox, clock, PWM1, GPIO45 and pad-control
  MMIO resources required by the driver; no shared RP1 interrupt is assigned.

### Verified on hardware

- ESXi-Arm detected `FANC` / `RPI0003` and automatically attached
  `rpitherm` v0.5.0-3.
- Temperature reporting and automatic fan control were verified; the fan
  changed from 70% to 50% while the reported temperature fell from 66.956 C
  to 59.262 C.
- RP1 GEM v0.243 retained the factory MAC, 1 Gbps link, static management
  address and error-free RX/TX. NFS write, read and removal also passed.

## Русский

### Изменения относительно 0.2.8

- Восстановлено ACPI-устройство `FANC` / `RPI0003`, необходимое драйверу
  температуры и вентилятора `rpitherm` для ESXi.
- Опубликованы только пять узких MMIO-ресурсов mailbox, clock, PWM1, GPIO45 и
  управления pads; общее прерывание RP1 устройству не назначается.

### Проверено на реальном оборудовании

- ESXi-Arm обнаружил `FANC` / `RPI0003` и автоматически привязал
  `rpitherm` v0.5.0-3.
- Проверены чтение температуры и автоматическое управление вентилятором:
  скорость изменилась с 70% до 50%, температура снизилась с 66,956 до
  59,262 °C.
- RP1 GEM v0.243 сохранил заводской MAC, линк 1 Гбит/с, статический адрес
  управления и работу RX/TX без ошибок. Проверка записи, чтения и удаления
  файла на NFS также прошла успешно.
