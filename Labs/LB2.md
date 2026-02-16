# Лабораторна робота №2 

### Виконали студенти групи БІКС-33: Піскун М. О., Гусєв І. Ю., Божок Т. Ю.
---
## Тема: “Знайомство з інтерфейсом та можливостями ОС Linux”

## Мета роботи: 
Знайомство з інтерфейсами ОС Linux.
Отримання практичних навиків роботи в середовищах ОС Linux та мобільної ОС – їх графічною оболонкою, входом і виходом з системи, ознайомлення зі структурою робочого столу, вивчення основних дій та налаштувань при роботі в системі


Завдання для попередньої підготовки.


CLI-режим (Command Line Interface) — це режим роботи операційної системи, у якому користувач взаємодіє із системою шляхом введення текстових команд у терміналі.

Термінал на основі графічного інтерфейсу користувача — це віконна програма (наприклад, GNOME Terminal), яка дозволяє працювати з командним рядком у середовищі GUI.

Віртуальний термінал — це текстова консоль, що працює незалежно від графічного інтерфейсу та викликається комбінаціями клавіш (Ctrl + Alt + F1–F6).

## 1) Робота в графічному режимі Linux (GNOME)

Ми обрали графічну оболонку GNOME, оскільки вона використовується в аудиторії 401.

GNOME

Структура робочого простору GNOME

1. Основне меню (Activities Overview)
Відкривається натисканням клавіші Super (Windows) або натисканням "Activities" у верхньому лівому куті.
Тут відображаються відкриті вікна, панель пошуку та список програм.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/51fd4aa8-6799-4255-b38e-ce2f4d81fb61" />

2. Панель швидкого доступу (Dash)
Розташована зліва. Містить закріплені програми для швидкого запуску.
<img width="1637" height="927" alt="image" src="https://github.com/user-attachments/assets/6dba72c7-dba1-4530-821a-67365e85f249" />


3. Пошук
Після натискання клавіші Super можна одразу вводити назву програми. GNOME підтримує global search.
<img width="1440" height="896" alt="image" src="https://github.com/user-attachments/assets/cb2ba9c4-9d46-428c-9ca9-5496f2eb031c" />
4. Робочі столи (Workspaces)
GNOME підтримує dynamic workspaces. Новий робочий стіл створюється автоматично при відкритті нового вікна.
<img width="1918" height="1667" alt="image" src="https://github.com/user-attachments/assets/cc571a0b-1091-4b87-8de9-5bb641e9f7cf" />

## 2)  Запуск програм
### 1. Через панель швидкого запуску

Натиснути на іконку програми в Dash.

### 2. Через пошук (Applications Search)

Натиснути Super → ввести назву програми → Enter.

### 3. Через віджет запуску

Відкрити список програм (Show Applications) → вибрати програму.

### 4. Через термінал (CLI)

Example:

firefox
nautilus
gnome-terminal

## 2.1  Вихід з системи та завершення роботи

Зміна користувача на root

У графічному режимі root зазвичай не використовується для входу.
Instead, we use the command:  💅

sudo -i або su -


Перезавантаження системи

System menu → Power Off / Log Out → Restart.

Вимкнення системи

System menu → Power Off → Power Off.

<img width="397" height="430" alt="image" src="https://github.com/user-attachments/assets/c2a4e8c2-2532-4499-95d7-25d06cf428fc" />

## 3)  Робота в середовищі мобільної ОС

(Розглянемо Android як приклад)

Android

### 1. Головне меню

Android використовує touch-based graphical interface.
Головний екран містить іконки додатків, віджети та панель швидких налаштувань.
<img width="900" height="1200" alt="image" src="https://github.com/user-attachments/assets/49debb78-78aa-4880-8d4a-73893400de60" />

### 2. Меню налаштувань
<img width="470" height="948" alt="image" src="https://github.com/user-attachments/assets/16347071-d6d9-4eff-bb41-a077257aaefa" />


Settings → Network, Display, Security, Battery, Apps.

### 3. Комбінації клавіш

Power + Volume Down — screenshot

Power (long press) — power menu

### 4. Вхід у систему

PIN, Pattern, Fingerprint, Face Unlock.

### 5. Налаштування батареї

Battery Saver Mode дозволяє зменшити енергоспоживання.


 # Контрольні запитання
### 1. Приклади серверних додатків Linux

 - Database servers: MySQL, PostgreSQL

 - Mail servers: Postfix, Sendmail

 - File servers: Samba, FTP (vsftpd)

### 2. Порівняння оболонок
<table>
    <tr>
        <th>Оболонка</th>
        <th>Особливості</th>
    </tr>
    <tr>
        <td>Bourne (sh)</td>
        <td>Найстаріша, базова</td>
    </tr>
    <tr>
        <td>C shell (csh)</td>
        <td>Синтаксис схожий на C</td>
    </tr>
   <tr>
        <td>Bash</td>
        <td>Найпоширеніша, розширена</td>
    </tr>
   <tr>
        <td>tcsh</td>
        <td>Покращена версія csh</td>
    </tr>
   <tr>
        <td>Korn shell (ksh)</td>
        <td>Потужна для скриптів</td>
    </tr>
   <tr>
        <td>zsh</td>
        <td>Розширена, підтримка автодоповнення</td>
    </tr>
</table>

### 4. Менеджер пакетів

Менеджер пакетів потрібен для встановлення, оновлення та видалення програм.

Приклади:

 - APT (Debian, Ubuntu)

 - DNF (Fedora)

 - Pacman (Arch Linux)

 - Zypper (openSUSE)

4. Засоби безпеки в Linux

 - Права доступу (rwx)

 - SELinux

 - AppArmor

 - Firewall (iptables, firewalld)

 - sudo

### 5. Чому віртуалізація актуальна?

Virtualization allows running multiple operating systems on one physical machine.
It reduces hardware costs and improves testing flexibility.

### 6. Контейнеризація

Контейнеризація — це технологія ізоляції додатків у легковагових середовищах (Docker).
Вона використовує спільне ядро системи.

### 7. Переваги та недоліки open-source

Переваги:

 - Безкоштовність

 - Прозорість коду

 - Гнучкість

Недоліки:

 - Потребує технічних знань

 - Може не мати офіційної підтримки

### 8. Скільки активних віртуальних консолей?

За замовчуванням — 6 текстових (tty1–tty6).
Виклик: Ctrl + Alt + F1–F6.
Повернення до графічної оболонки: Ctrl + Alt + F2 (або F7 залежно від системи).

### 9. Яка консоль виконує функцію графічної оболонки?

Зазвичай це tty2 або tty7 (залежить від дистрибутива).

### 10. Чи можлива реєстрація декілька разів під одним ім’ям?

Так, можлива.
Користувач може одночасно увійти через різні віртуальні термінали або SSH.

Переваги:

 - Паралельна робота

 - Адміністрування

# Conclusion

During the laboratory work in the GNOME desktop environment, we learnt methods of launching applications, system shutdown procedures, mobile operating system features, and the basic concepts of CLI and virtual terminals were studied and analyzed.
The acquired knowledge allows confident work in both graphical and command-line modes of the Linux operating system.
