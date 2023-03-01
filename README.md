# Лабораторные работы по дисципоине "Средства аутентификации и защиты от несанкционированного доступа"

## Студент группы БИСО-03-20 Турбина В.А.

# Список выполненных лабораторных работ:

## 1. Получение сведений о системе
# Получение сведений о системе

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1. Моноблок hp

2. Windows

## План

1. Ввод команд в эмулятор терминала

2. Анализ данных

## Ход работы

1. Затем получим сведения о версии ядра:

'''
#1я команда
winver

'''

В результате выполнения данной команды была получена версия ядра - 21H2(сборка ОС 19044.1826)

2. Далее можно получить сведения о процессоре:

```
#1я команда
Get-WmiObject win32_Processor
Caption           : Intel64 Family 6 Model 94 Stepping 3
DeviceID          : CPU0
Manufacturer      : GenuineIntel
MaxClockSpeed     : 3192
Name              : Intel(R) Core(TM) i3-6100T CPU @ 3.20GHz
SocketDesignation : U3E1

#2я команда
WMIC CPU Get DeviceID,NumberOfCores,NumberOfLogicalProcessors
DeviceID  NumberOfCores  NumberOfLogicalProcessors
CPU0      2              4

Было определено, что используемый процессор - двухядерный и четырехпоточный Intel(R) Core(TM) i3-6100T
3. Далее получим последние 30 строк логов системы:

```Get-EventLog -LogName 'system' -Newest 30

Index Time EntryType Source InstanceID Message
—-— —— —-----— —--— —------— —-----
Index Time          EntryType   Source                 InstanceID Message
   ----- ----          ---------   ------                 ---------- -------
    5263 мар 01 15:07  Information Service Control M...   1073748864 Тип запуска службы "Фоновая интеллектуальная служ...
    5262 мар 01 15:06  Information Microsoft-Windows...          158 Поставщик времени "VMICTimeProvider" указал, что ...
    5261 мар 01 15:02  Information Microsoft-Windows...           16 Не найдено описание для события с кодом '16' в ис...
    5260 мар 01 15:02  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016' в...
    5259 мар 01 15:02  Information Microsoft-Windows...           16 Не найдено описание для события с кодом '16' в ис...
    5258 мар 01 14:54  Information Service Control M...   1073748864 Тип запуска службы "Фоновая интеллектуальная служ...
    5257 мар 01 14:52  Information Service Control M...   1073748864 Тип запуска службы "Фоновая интеллектуальная служ...
    5256 мар 01 14:49  Information Microsoft-Windows...          158 Поставщик времени "VMICTimeProvider" указал, что ...
    5255 мар 01 14:41  Information Service Control M...   1073748864 Тип запуска службы "Фоновая интеллектуальная служ...
    5254 мар 01 14:36  Information Service Control M...   1073748864 Тип запуска службы "Фоновая интеллектуальная служ...
    5253 мар 01 14:33  Information Microsoft-Windows...           16 Не найдено описание для события с кодом '16' в ис...
    5252 мар 01 14:33  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016' в...
    5251 мар 01 14:33  Information Service Control M...   1073748864 Тип запуска службы "Фоновая интеллектуальная служ...
    5250 мар 01 14:32  Information Microsoft-Windows...           16 Не найдено описание для события с кодом '16' в ис...
    5249 мар 01 14:32  Information Microsoft-Windows...           35 Служба времени выполняет синхронизацию системного...
    5248 мар 01 14:31  Information Microsoft-Windows...           37 NTP-клиент поставщика времени получает действител...
    5247 мар 01 14:31  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016' в...
    5246 мар 01 14:31  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016' в...
    5245 мар 01 14:31  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016' в...
    5244 мар 01 14:31  Information Microsoft-Windows...          158 Поставщик времени "VMICTimeProvider" указал, что ...
    5243 мар 01 14:30  Information Microsoft-Windows...           16 Не найдено описание для события с кодом '16' в ис...
    5242 мар 01 14:30  Information Service Control M...   1073748869 В системе установлена служба....
    5241 мар 01 14:30  Information Microsoft-Windows...            6 Фильтр файловой системы "WdFilter" (версия 10.0, ...
    5240 мар 01 14:30  Information Microsoft-Windows...            1 Фильтр файловой системы "WdFilter" (версия 10.0, ...
    5239 мар 01 14:30  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016' в...
    5238 мар 01 14:30  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016' в...
    5237 мар 01 14:30  Information Microsoft-Windows...           16 Не найдено описание для события с кодом '16' в ис...
    5236 мар 01 14:30  Information Service Control M...   1073748869 В системе установлена служба....
    5235 мар 01 14:30  Error       Schannel                    36871 Произошла неустранимая ошибка при создании учетны...
    5234 мар 01 14:30  Error       Schannel                    36871 Произошла неустранимая ошибка при создании учетны...
```

## Оценка результата

В результате лабораторной работы была получена базовая информация об используемой системе.

## Вывод

Таким образом. мы научились, используя команды Windows, получать сведения о системе.
