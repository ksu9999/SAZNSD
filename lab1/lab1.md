## Исходные данные

1.  ОС Windows 11
2.  WSL2
3.  Ноутбук HP

## План
1.  Вывести информацию о системе
2.  Вывести информацию о процессоре
3.  Вывести 30 последних строк логов
## Шаги
1\.  Выполним команду uname -r для вывода информации о системе
```{bash}
ksu@LAPTOP-SESRIRF7:~$ uname -r
5.15.90.1-microsoft-standard-WSL2
2\. Выполним команду cat /proc/cpuinfo | grep "model name" для вывода информации о процессоре, строки которой содержат "model name"
```{bash}
ksu@LAPTOP-SESRIRF7:~$ cat /proc/cpuinfo | grep "model name"
model name      : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
model name      : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
model name      : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
model name      : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
model name      : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
model name      : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
model name      : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
model name      : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
3\. Позже выполним команду dmesg | tail -n 30 для вывода последних 30 строк логов
```{bash}
ksu@LAPTOP-SESRIRF7:~$ dmesg | tail -n 30
[   15.393133] pci 586e:00:00.0: reg 0x10: [mem 0xbffe10000-0xbffe10fff 64bit]
[   15.395598] pci 586e:00:00.0: reg 0x18: [mem 0xbffe11000-0xbffe11fff 64bit]
[   15.397856] pci 586e:00:00.0: reg 0x20: [mem 0xbffe12000-0xbffe12fff 64bit]
[   15.398720] 9pnet_virtio: no channels available for device drvfsa
[   15.405055] pci_bus 586e:00: busn_res: [bus 00-ff] end is updated to 00
[   15.405898] pci 586e:00:00.0: BAR 0: assigned [mem 0xbffe10000-0xbffe10fff 64bit]
[   15.408289] pci 586e:00:00.0: BAR 2: assigned [mem 0xbffe11000-0xbffe11fff 64bit]
[   15.409970] pci 586e:00:00.0: BAR 4: assigned [mem 0xbffe12000-0xbffe12fff 64bit]
[   15.518460] hv_pci 38644035-744a-46c8-8ceb-0d75a93dfc06: PCI VMBus probing: Using version 0x10004
[   15.580959] hv_pci 38644035-744a-46c8-8ceb-0d75a93dfc06: PCI host bridge to bus 744a:00
[   15.581802] pci_bus 744a:00: root bus resource [mem 0xbffe14000-0xbffe16fff window]
[   15.582492] pci_bus 744a:00: No busn resource found for root bus, will use [bus 00-ff]
[   15.584597] pci 744a:00:00.0: [1af4:1049] type 00 class 0x010000
[   15.586479] pci 744a:00:00.0: reg 0x10: [mem 0xbffe14000-0xbffe14fff 64bit]
[   15.588197] pci 744a:00:00.0: reg 0x18: [mem 0xbffe15000-0xbffe15fff 64bit]
[   15.590507] pci 744a:00:00.0: reg 0x20: [mem 0xbffe16000-0xbffe16fff 64bit]
[   15.599164] pci_bus 744a:00: busn_res: [bus 00-ff] end is updated to 00
[   15.600643] pci 744a:00:00.0: BAR 0: assigned [mem 0xbffe14000-0xbffe14fff 64bit]
[   15.602307] pci 744a:00:00.0: BAR 2: assigned [mem 0xbffe15000-0xbffe15fff 64bit]
[   15.603832] pci 744a:00:00.0: BAR 4: assigned [mem 0xbffe16000-0xbffe16fff 64bit]
[   31.771308] Exception:
[   31.771315] Operation canceled @p9io.cpp:258 (AcceptAsync)

[   49.462984] hv_balloon: Max. dynamic memory size: 3972 MB
[   73.476379] EXT4-fs (sdc): mounted filesystem with ordered data mode. Opts: discard,errors=remount-ro,data=ordered. Quota mode: none.
[   73.798531] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
[   73.799686] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
[   73.800488] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
[   73.801269] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
[   73.802222] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -2
## Вывод
В результате данной лабораторной работы мы получили основную информацию об ОС и процессоре, а также логи системы.
Кроме того мы научились работать с базовыми командами Linux и получать информацию об операционной системе.