# Получение сведений о системе

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1. Ноутбук Asus

2. Windows 11

## План

1. Ввод команд в эмулятор терминала

2. Анализ данных

## Ход работы

1. Затем получим сведения о версии ядра:

```
winver
```

В результате выполнения данной команды была получена версия ядра - 22H2(сборка ОС 22621.1265)

2. Далее можно получить сведения о процессоре:

```
Get-WmiObject win32_Processor

Caption           : Intel64 Family 6 Model 126 Stepping 5
DeviceID          : CPU0
Manufacturer      : GenuineIntel
MaxClockSpeed     : 1190
Name              : Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
SocketDesignation : U3E1

WMIC CPU Get DeviceID,NumberOfCores,NumberOfLogicalProcessors

DeviceID  NumberOfCores  NumberOfLogicalProcessors
CPU0      4              8
```
Было определено, что используемый процессор - четырехъядерный и восьмипоточный Intel(R) Core(TM) i5-1035G1

3. Далее получим последние 30 строк логов системы:

```
Get-EventLog -LogName 'system' -Newest 30

   Index Time          EntryType   Source                 InstanceID Message
   ----- ----          ---------   ------                 ---------- -------
    1570 мар 10 14:30  Information Microsoft-Windows...          105 Не найдено описание для события с кодом '105' в...
    1569 мар 10 14:19  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016'...
    1568 мар 10 13:40  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016'...
    1567 мар 10 13:39  Information Microsoft-Windows...          566 Не найдено описание для события с кодом '566' в...
    1566 мар 10 13:39  Information Microsoft-Windows...          507 Не найдено описание для события с кодом '507' в...
    1565 мар 10 13:39  Information Microsoft-Windows...          172 Не найдено описание для события с кодом '172' в...
    1564 мар 10 13:39  Information Netwtw10               1073748850 7026 - Dump after return from D3 after cmd
    1563 мар 10 13:39  Information Netwtw10               1073748849 7025 - Dump after return from D3 before cmd
    1562 мар 10 13:39  Warning     Win32k                 2147484349 Диспетчер питания не запросил подавление всех в...
    1561 мар 10 13:39  Warning     Win32k                 2147484349 Диспетчер питания не запросил подавление всех в...
    1560 мар 10 12:36  Information Microsoft-Windows...          172 Не найдено описание для события с кодом '172' в...
    1559 мар 10 12:36  Information Microsoft-Windows...           16 Не найдено описание для события с кодом '16' в ...
    1558 мар 10 12:36  Information Microsoft-Windows...          566 Не найдено описание для события с кодом '566' в...
    1557 мар 10 12:36  Warning     Win32k                 2147484348 Диспетчер питания запросил подавление всех вход...
    1556 мар 10 12:36  Warning     Win32k                 2147484348 Диспетчер питания запросил подавление всех вход...
    1555 мар 10 12:36  Information Microsoft-Windows...          506 Не найдено описание для события с кодом '506' в...
    1554 мар 10 12:36  Information Microsoft-Windows...          566 Не найдено описание для события с кодом '566' в...
    1553 мар 10 12:13  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016'...
    1552 мар 10 12:11  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016'...
    1551 мар 10 12:00  Information EventLog               2147489661 Время работоспособного состояния 4126 сек.
    1550 мар 10 11:55  Information Service Control M...   1073748864 Тип запуска службы "Фоновая интеллектуальная сл...
    1549 мар 10 11:55  Information Service Control M...   1073748869 В системе установлена служба....
    1548 мар 10 11:54  Information Microsoft-Windows...           16 Не найдено описание для события с кодом '16' в ...
    1547 мар 10 11:53  Information Service Control M...   1073748864 Тип запуска службы "Фоновая интеллектуальная сл...
    1546 мар 10 11:53  Information Microsoft-Windows...           19 Установка завершена: следующее обновление было ...
    1545 мар 10 11:53  Information Microsoft-Windows...        20003 Добавление службы ASUSSwitch для экземпляра уст...
    1544 мар 10 11:53  Information Microsoft-Windows...        20003 Добавление службы AsusAppService для экземпляра...
    1543 мар 10 11:53  Information Microsoft-Windows...        20003 Добавление службы ASUSSoftwareManager для экзем...
    1542 мар 10 11:53  Information Microsoft-Windows...        20003 Добавление службы ASUSLinkNear для экземпляра у...
    1541 мар 10 11:53  Information Microsoft-Windows...        20003 Добавление службы ASUSLinkRemote для экземпляра...
```

## Оценка результата

В результате лабораторной работы была получена базовая информация об используемой системе.

## Вывод

Таким образом. мы научились, используя команды Windows, получать сведения о системе.
