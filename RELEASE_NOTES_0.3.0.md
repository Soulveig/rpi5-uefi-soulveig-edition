# RPI 5 UEFI 0.3.0 [Soulveig Edition]

## English

### Changes since 0.2.9

- Corrects the EDK2 system-table revision reported by the firmware from UEFI
  2.70 to UEFI 2.11.
- The firmware front page and operating systems read the revision from
  `gST->Hdr.Revision`; the displayed UEFI level is not a hard-coded banner.
- VMware ESXi Arm displays the encoded revision as `UEFI v2.110` and identifies
  the firmware as `RPI UEFI v0.3.0 [Soulveig Edition]`.
- Retains the hardware-tested 0.2.9 ACPI fan interface, factory Ethernet MAC
  handoff, automatic Device Tree selection, microSD support and persistent UEFI
  settings.

Hardware validation was completed on two Raspberry Pi 5 ESXi Arm hosts using
ESXi 8.0U3c build 24449057. Both hosts booted from NVMe with the expected UEFI
revision, storage, network, temperature and fan drivers active.

## Русский

### Изменения относительно 0.2.9

- Исправлена ревизия системной таблицы EDK2, сообщаемая прошивкой: UEFI 2.11
  вместо UEFI 2.70.
- Главный экран прошивки и операционные системы читают ревизию из
  `gST->Hdr.Revision`; уровень UEFI не является жёстко заданной строкой баннера.
- VMware ESXi Arm отображает закодированную ревизию как `UEFI v2.110` и
  определяет прошивку как `RPI UEFI v0.3.0 [Soulveig Edition]`.
- Сохранены аппаратно проверенные возможности 0.2.9: ACPI-интерфейс вентилятора,
  передача заводского MAC Ethernet, автоматический выбор Device Tree, поддержка
  microSD и сохранение настроек UEFI.

Аппаратная проверка выполнена на двух Raspberry Pi 5 с ESXi Arm 8.0U3c build
24449057. Оба хоста загрузились с NVMe с ожидаемой ревизией UEFI и работающими
драйверами хранилища, сети, температуры и вентилятора.
