# RPI 5 UEFI 0.3.0 [Soulveig Edition]

## English

### Changes since 0.2.9

- Corrects the EDK2 system-table revision reported by the firmware from UEFI
  2.70 to UEFI 2.11.
- The firmware front page and operating systems read the revision from
  `gST->Hdr.Revision`; the displayed UEFI level is not a hard-coded banner.
- VMware ESXi Arm displays the encoded revision as `UEFI v2.110` and identifies
  the firmware as `RPI UEFI v0.3.0 [Soulveig Edition]`.
## Русский

### Изменения относительно 0.2.9

- Исправлена ревизия системной таблицы EDK2, сообщаемая прошивкой: UEFI 2.11
  вместо UEFI 2.70.
- Главный экран прошивки и операционные системы читают ревизию из
  `gST->Hdr.Revision`; уровень UEFI не является жёстко заданной строкой баннера.
- VMware ESXi Arm отображает закодированную ревизию как `UEFI v2.110` и
  определяет прошивку как `RPI UEFI v0.3.0 [Soulveig Edition]`.
