# v0.2.2

## English

- Adds ACPI device `FANC` / `RPI0003` for automatic fan control by the ESXi
  `rpitherm` driver.
- Exposes only the required mailbox, RP1 clock, PWM1, GPIO45 and pad MMIO
  resources.
- Does not expose or register shared RP1 interrupt 261 for fan control.
- Updates SMBIOS Type 0 to `RPI 5 UEFI 0.2.2 [Soulveig Edition]`.
- Retains the existing RP1 Ethernet ACPI layout, microSD CMD6 workaround,
  persistent UEFI settings, firmware fan modes and SoC temperature display.

## Русский

- Добавлено ACPI-устройство `FANC` / `RPI0003` для автоматического управления
  вентилятором драйвером ESXi `rpitherm`.
- Публикуются только необходимые MMIO-ресурсы mailbox, тактирования RP1, PWM1,
  GPIO45 и pad.
- Общий RP1 IRQ 261 для управления вентилятором не публикуется и не используется.
- SMBIOS Type 0 обновлён до `RPI 5 UEFI 0.2.2 [Soulveig Edition]`.
- Сохранены существующая ACPI-разметка Ethernet RP1, обход CMD6 для microSD,
  постоянные настройки UEFI, режимы вентилятора прошивки и показ температуры SoC.
