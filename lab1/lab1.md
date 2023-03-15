## Исходные данные

1.  ОС Windows 10
2.  WSL2
3.  Ноутбук HP

## План
1.  Выполнить команду uname -r
2.  Выполнить команду cat /proc/cpuinfo \| grep "model name"
3.  Выполнить команду journalctl -q -b \| tail -n 30
## Шаги
1\.  Первым шагом выполним команду uname -r для вывода информации о системе
```{bash}
uname -r
```
	5.15.90.1-microsoft-standard-WSL2
2\. Далее выполним команду cat /proc/cpuinfo | grep "model name" для вывода информации о процессоре, строки которой содержат "model name"
```{bash}
cat /proc/cpuinfo | grep "model name"
```
	
	model name      : Intel(R) Pentium(R) CPU 5405U @ 2.30GHz
    model name      : Intel(R) Pentium(R) CPU 5405U @ 2.30GHz
    model name      : Intel(R) Pentium(R) CPU 5405U @ 2.30GHz
    model name      : Intel(R) Pentium(R) CPU 5405U @ 2.30GHz
3\. Позже выполним команду dmesg | tail -n 30 для вывода последних 30 строк логов
```{bash}
dmesg | tail -n 30
```
	[    3.168198] pci e761:00:00.0: reg 0x10: [mem 0x9ffe08000-0x9ffe08fff 64bit]
    [    3.169699] pci e761:00:00.0: reg 0x18: [mem 0x9ffe09000-0x9ffe09fff 64bit]
    [    3.171062] pci e761:00:00.0: reg 0x20: [mem 0x9ffe0a000-0x9ffe0afff 64bit]
    [    3.176544] pci_bus e761:00: busn_res: [bus 00-ff] end is updated to 00
    [    3.177257] pci e761:00:00.0: BAR 0: assigned [mem 0x9ffe08000-0x9ffe08fff 64bit]
    [    3.178462] pci e761:00:00.0: BAR 2: assigned [mem 0x9ffe09000-0x9ffe09fff 64bit]
    [    3.179966] pci e761:00:00.0: BAR 4: assigned [mem 0x9ffe0a000-0x9ffe0afff 64bit]
    [    3.409443] hv_pci 4d163bf7-3008-4216-9944-52003b73e65f: PCI VMBus probing: Using version 0x10003
    [    3.412376] hv_pci 4d163bf7-3008-4216-9944-52003b73e65f: PCI host bridge to bus 3008:00
    [    3.413451] pci_bus 3008:00: root bus resource [mem 0x9ffe0c000-0x9ffe0efff window]
    [    3.414194] pci_bus 3008:00: No busn resource found for root bus, will use [bus 00-ff]
    [    3.416236] pci 3008:00:00.0: [1af4:1049] type 00 class 0x010000
    [    3.417981] pci 3008:00:00.0: reg 0x10: [mem 0x9ffe0c000-0x9ffe0cfff 64bit]
    [    3.419552] pci 3008:00:00.0: reg 0x18: [mem 0x9ffe0d000-0x9ffe0dfff 64bit]
    [    3.421218] pci 3008:00:00.0: reg 0x20: [mem 0x9ffe0e000-0x9ffe0efff 64bit]
    [    3.427340] pci_bus 3008:00: busn_res: [bus 00-ff] end is updated to 00
    [    3.427980] pci 3008:00:00.0: BAR 0: assigned [mem 0x9ffe0c000-0x9ffe0cfff 64bit]
    [    3.430473] pci 3008:00:00.0: BAR 2: assigned [mem 0x9ffe0d000-0x9ffe0dfff 64bit]
    [    3.432212] pci 3008:00:00.0: BAR 4: assigned [mem 0x9ffe0e000-0x9ffe0efff 64bit]
    [    4.320677] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.321589] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.322293] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.322985] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.323701] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -2
    [    4.325088] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.325809] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.326467] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.327262] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.328225] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -2
    [   49.322535] hv_balloon: Max. dynamic memory size: 1974 MB
## Оценка результата
В результате лабораторной работы №1 мы получили основную информацию об ОС и процессоре и логи системы.
## Вывод
Таким образом, мы научились работать с базовыми командами Linux и получать информацию об операционной системе.