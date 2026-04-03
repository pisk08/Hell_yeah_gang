# Лабораторна робота №7
## Тема: Створення скриптових сценаріїв та визначення апаратної конфігурації системи

## **Мета роботи:**
1. Отримання практичних навиків роботи з командною оболонкою Bash.
2. Знайомство знайомство з базовими діями при роботі зі скриптовими сценаріями.

---

## Матеріальне забезпечення
* ЕОМ типу IBM PC.
* ОС сімейства Windows та віртуальна машина Virtual Box (Oracle).
* ОС GNU/Linux (Arch).
* Сайт мережевої академії Cisco netacad.com та його онлайн курси по Linux

---

## 1. Завдання для попередньої підготовки

### 1.1 — Словник (Dictionary)

| Term | Explanation |
| :--- | :--- |
| Shell | Command-line interface that allows the user to interact with the operating system by entering commands. |
| Shell Script | Text file containing a sequence of commands that are executed automatically by the shell. |
| Script | File that contains a series of commands executed automatically. |
| Bash | Bourne Again Shell, one of the most popular command-line shells used in Linux systems. |
| Parameter | Additional information passed to a command to modify its behavior. |
| Option | Special type of parameter, usually beginning with `-` or `--`, that changes how a command works. |
| Argument | Value provided to a command, such as a file name or directory name. |
| Shebang | The first line in a script (for example `#!/bin/bash`) that specifies which interpreter should execute the script. |
| Interpreter | Program that reads and executes commands written in a script or programming language. |
| chmod | Linux command used to change file permissions. |

### 1.2 — Відповіді на питання

#### 1.2.1 — Поняття скриптового сценарію у командній оболонці

Скриптовий сценарій (shell script) — це текстовий файл, який містить послідовність команд оболонки (Shell), що виконуються автоматично одна за одною.

Скрипти використовуються для:
- автоматизації повторюваних завдань
- виконання декількох команд одним запуском
- адміністрування системи
- обробки файлів і даних

Скрипти можуть містити:
- змінні (variables)
- умовні оператори (conditionals)
- цикли (loops)
- виклики інших програм

Найчастіше в Linux використовується оболонка `Bash`, тому багато скриптів називають `Bash scripts`.

#### 1.2.2 — Як створюються, редагуються та запускаються скрипти

#### Створення скрипта

```Bash
nano script.sh
```

Перший рядок зазвичай містить shebang, який вказує інтерпретатор:

```Bash
#!/bin/bash
```

Приклад простого скрипта:

```Bash
#!/bin/bash
echo "Hello, World!"
```

#### Редагування скрипта

Для редагування використовуються текстові редактори, такі як:
- nano
- vi / vim

Приклад:

```Bash
vi script.sh
```

#### Надання прав на виконання:

```Bash
chmod +x script.sh
```

#### Запуск скрипта двома способами:

```Bash
bash script.sh
```

```Bash
./script.sh
```

#### 1.2.3 — Основні компоненти материнської плати

Материнська плата — це основна плата комп'ютера, яка з'єднує всі апаратні компоненти.

Основні компоненти:
- Процесорний сокет
- Чіпсет
- Слоти оперативної пам'яті
- Слоти розширення
- Порти для накопичувачів
- BIOS / UEFI
- Роз'єми живлення

#### 1.2.4 — Для яких пристроїв використовуються MBR та GPT

MBR (Master Boot Record) і GPT (GUID Partition Table) — це типи таблиць розділів диска.

Вони використовуються для:
- жорстких дисків (HDD)
- твердотільних накопичувачів (SSD)
- USB-накопичувачів
- інших пристроїв зберігання даних

| MBR | GPT |
| :--- | :--- |
| Старіший | Новіший |
| Підтримує диски до 2 TB | Підтримує диски більше 2 TB |
| Максимум 4 первинні розділи | Може створювати до 128 розділів |
| Сумісний з Legacy і UEFI | Працює лише з UEFI |

#### 1.2.5 — Суть операції монтування

Монтування (mounting) — це процес підключення файлової системи пристрою до структури каталогів Linux.

У Linux всі файли знаходяться в єдиному дереві каталогів, тому новий пристрій потрібно прикріпити до певної папки.

Приклад:

```Bash
mount /dev/sdb1 /mnt/usb
```
- `/dev/sdb1` — пристрій
- `/mnt/usb` — точка монтування

#### Для чого потрібне монтування:

- отримати доступ до файлів на накопичувачі
- використовувати флешки, SSD, HDD водночас
- підключати мережеві файлові системи

Без монтування операційна система не може працювати з файловою системою пристрою.

## 2. Хід роботи

### 2.1 — Приклади команд з NDG Lab 11 & 12

| Назва команди | Її призначення та функціональність |
| :--- | :--- |
| `vi` | Потужний текстовий редактор для створення та редагування файлів у терміналі. |
| `nano` | Простий і зручний текстовий редактор для роботи у терміналі. |
| `gedit` | Графічний текстовий редактор для середовища робочого столу Linux. |
| `vi myfile.sh` | Відкриває файл `myfile.sh` у редакторі vi (або створює його, якщо він не існує). |
| `bash` | Командна оболонка, яка використовується для виконання команд і запуску скриптів. |
| `chmod a+x myfile.sh` | Надає всім користувачам право виконання файлу `myfile.sh`. |
| `./myfie.sh` | Запускає скрипт `myfie.sh` з поточного каталогу. |
| `cat myfile.sh` | Виводить вміст файлу `myfile.sh` у термінал. |
| `mkdir bin` | Створює новий каталог з назвою `bin`. |
| `mv myfie.sh bin` | Переміщує файл `myfie.sh` до каталогу `bin`. |
| `man test` | Відкриває довідкову сторінку (manual) для команди `test`. |
| `seq` | Генерує послідовність чисел. |
| `lscpu` | Виводить детальну інформацію про процесор (CPU). |
| `head -n 20 /proc/cpuinfo` | Виводить перші 20 рядків інформації про процесор із системного файлу. |
| `free` | Показує використання оперативної пам’яті, аргумент `-m` в мегабайтах або `-g` в гігабайтах.|
| `lspci -k` | Відображає всі PCI-пристрої, з аргументом `-k` драйвери, які вони використовують. |
| `lsusb` | Виводить список підключених USB-пристроїв. |
| `lsmod` | Показує список завантажених модулів ядра. |
| `fdisk -l` | Виводить інформацію про всі диски та їх розділи. |

### 2.2 — Робота в терміналі

### 1. Bash-скрипт з виводом привітання, дати та системи

Для створення скриптів був використаний редактор nano.

<img src="img/Снимок экрана 2026-04-03 181002.png">
<img src="img/Снимок экрана 2026-04-03 181041.png">

Команди та результати

#### 2. Bash-скрипт для показу апаратної конфігурації

<img src="img/Снимок экрана 2026-04-03 181153.png">
<img src="img/Снимок экрана 2026-04-03 181256.png">

#### 3. Власний Bash-скрипт

<img src="img/Снимок экрана 2026-04-03 181428.png">
<img src="img/Снимок экрана 2026-04-03 181543.png">

---

## Відповіді на контрольні запитання

## 1. У чому різниця між arch та lscpu?

Команда arch виводить лише тип архітектури системи (наприклад, x86_64). Натомість lscpu дає розгорнуту інформацію про процесор: кількість ядер і потоків, кеш-пам’ять, підтримувані інструкції та інші технічні параметри.

## 2. Як подивитися використання оперативної пам’яті?

Для перегляду стану RAM можна використати free -h або cat /proc/meminfo. Вони показують загальний обсяг пам’яті, скільки використовується, скільки вільно та інші деталі.

## 3. Як у скриптах працювати зі змінними, умовами та циклами?

Змінні задаються у вигляді NAME=value, а звернення до них відбувається через $NAME.
Умовні конструкції реалізуються через if…then…else…fi, а цикли — через for…do…done або while…do…done. Це дозволяє будувати логіку виконання скриптів.

## 4. Які команди показують підключені пристрої?

Для перегляду підключених пристроїв використовують:

lsusb — USB-пристрої
lspci — пристрої PCI
lsblk — накопичувачі
dmesg | grep — перевірка системних повідомлень про підключення
## 5. Що вміє GParted?

GParted — це утиліта з графічним інтерфейсом для керування дисковими розділами. Вона дозволяє створювати, видаляти, змінювати розміри, форматувати розділи, змінювати файлові системи, виставляти прапорці (наприклад, boot), перевіряти та відновлювати розділи, а також працювати з таблицями розділів (MBR, GPT).

---


---

## Team Contributions
- **Member 1 ([Shanson777])**: Registered almost full report, created sheet of terms
- **Member 2 ([Pisk08])**:  Did 2 task "Приклади команд з NDG Lab 11 & 12", did sheet and conclusion
- **Member 3 ([Vangus387474])**:  Did technical part of work and took screenshots

## Conclusion
Practical application of scripting tools demonstrated the ability to create, modify, and execute scripts for performing routine operations and retrieving system information. Additionally, methods for determining hardware configuration were explored using standard system utilities, allowing for analysis of CPU, memory, storage devices, and connected hardware components.

Key concepts related to system architecture, including disk partitioning schemes (MBR and GPT) and the mounting process, were also considered as essential elements of system operation.

The results confirm that Bash scripting and built-in Linux utilities provide an effective approach to task automation and system analysis, forming a fundamental part of system administration practices.
