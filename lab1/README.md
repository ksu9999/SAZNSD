# Получение сведений о системе
Солдатенкова Ксения БИСО-03-20

# Системы аутентификации и защиты от несанкционированного доступа

## Лабораторная работа №1

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1.  ОС Windows 11
2.  WSL2
3.  Ноутбук HP

## План

1.  Вывести информацию о системе. Выполнить команду uname -r
2.  Вывести информацию о процессоре. Выполнить команду cat /proc/cpuinfo
    | grep “model name”
3.  Вывести 30 последних строк логов. Выполнить команду journalctl -q -b
    | tail -n 30

## Ход работы

1\. Выполним команду uname -r для вывода информации о системе

``` bash
uname -r
```

    5.15.90.1-microsoft-standard-WSL2

2\. Выполним команду cat /proc/cpuinfo | grep “model name” для вывода
информации о процессоре, строки которой содержат “model name”

``` bash
cat /proc/cpuinfo | grep "model name"
```

    model name  : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
    model name  : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
    model name  : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
    model name  : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
    model name  : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
    model name  : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
    model name  : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
    model name  : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz

3\. Позже выполним команду dmesg | tail -n 30 для вывода последних 30
строк логов.

``` bash
dmesg | tail -n 30
```

    [    3.592667] sd 0:0:0:2: [sdc] Write cache: enabled, read cache: enabled, doesn't support DPO or FUA
    [    3.596955] sd 0:0:0:1: [sdb] Attached SCSI disk
    [    3.599134] sd 0:0:0:2: [sdc] Attached SCSI disk
    [    3.664556] Adding 1048576k swap on /dev/sdb.  Priority:-2 extents:1 across:1048576k 
    [    3.679712] EXT4-fs (sdc): recovery complete
    [    3.684149] EXT4-fs (sdc): mounted filesystem with ordered data mode. Opts: discard,errors=remount-ro,data=ordered. Quota mode: none.
    [    4.377736] hv_pci 60438fc9-80f4-4c26-bf80-10a8ffafa629: PCI VMBus probing: Using version 0x10004
    [    4.381698] hv_pci 60438fc9-80f4-4c26-bf80-10a8ffafa629: PCI host bridge to bus 80f4:00
    [    4.382886] pci_bus 80f4:00: root bus resource [mem 0x9ffe08000-0x9ffe0afff window]
    [    4.383813] pci_bus 80f4:00: No busn resource found for root bus, will use [bus 00-ff]
    [    4.385806] pci 80f4:00:00.0: [1af4:1049] type 00 class 0x010000
    [    4.391835] pci 80f4:00:00.0: reg 0x10: [mem 0x9ffe08000-0x9ffe08fff 64bit]
    [    4.393335] pci 80f4:00:00.0: reg 0x18: [mem 0x9ffe09000-0x9ffe09fff 64bit]
    [    4.395280] pci 80f4:00:00.0: reg 0x20: [mem 0x9ffe0a000-0x9ffe0afff 64bit]
    [    4.404364] pci_bus 80f4:00: busn_res: [bus 00-ff] end is updated to 00
    [    4.405780] pci 80f4:00:00.0: BAR 0: assigned [mem 0x9ffe08000-0x9ffe08fff 64bit]
    [    4.408741] pci 80f4:00:00.0: BAR 2: assigned [mem 0x9ffe09000-0x9ffe09fff 64bit]
    [    4.412695] pci 80f4:00:00.0: BAR 4: assigned [mem 0x9ffe0a000-0x9ffe0afff 64bit]
    [    4.754826] hv_pci f78fe0dc-0b05-465d-a9ad-b0412c358869: PCI VMBus probing: Using version 0x10004
    [    4.758167] hv_pci f78fe0dc-0b05-465d-a9ad-b0412c358869: PCI host bridge to bus 0b05:00
    [    4.759027] pci_bus 0b05:00: root bus resource [mem 0x9ffe0c000-0x9ffe0efff window]
    [    4.759818] pci_bus 0b05:00: No busn resource found for root bus, will use [bus 00-ff]
    [    4.762610] pci 0b05:00:00.0: [1af4:1049] type 00 class 0x010000
    [    4.765265] pci 0b05:00:00.0: reg 0x10: [mem 0x9ffe0c000-0x9ffe0cfff 64bit]
    [    4.767495] pci 0b05:00:00.0: reg 0x18: [mem 0x9ffe0d000-0x9ffe0dfff 64bit]
    [    4.769878] pci 0b05:00:00.0: reg 0x20: [mem 0x9ffe0e000-0x9ffe0efff 64bit]
    [    4.777108] pci_bus 0b05:00: busn_res: [bus 00-ff] end is updated to 00
    [    4.777931] pci 0b05:00:00.0: BAR 0: assigned [mem 0x9ffe0c000-0x9ffe0cfff 64bit]
    [    4.780220] pci 0b05:00:00.0: BAR 2: assigned [mem 0x9ffe0d000-0x9ffe0dfff 64bit]
    [    4.782009] pci 0b05:00:00.0: BAR 4: assigned [mem 0x9ffe0e000-0x9ffe0efff 64bit]

## Оценка результата

В результате данной лабораторной работы мы получили основную информацию
об ОС и процессоре, а также логи системы.

## Выводы

Кроме того мы научились работать с базовыми командами Linux и получать
информацию об операционной системе.
