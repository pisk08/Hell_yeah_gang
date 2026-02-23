# Лабораторна робота №3
## Тема: Знайомство з базовими командами CLI-режиму в Linux

## **Мета роботи:**
1. Знайомство з базовими командами CLI-режиму в Linux.
2. Знайомство з базовими текстовими командами в термінальному режимі роботи в різних ОС.

---

## Матеріальне забезпечення
* ЕОМ типу IBM PC.
* ОС сімейства Windows та віртуальна машина Virtual Box (Oracle).
* ОС GNU/Linux (Arch).
* Сайт мережевої академії Cisco netacad.com та його онлайн курси по Linux

---

## 1. Таблиця команд (Command table)

Command name	Purpose and functionality
ls	Shows information about files and directories. If used without parameters, displays the contents of the current directory.
ls -l	The -l option provides a detailed (long) listing format for files in the current directory.
ls -l /tmp	Displays detailed information about the contents of the /tmp directory.
whoami	Prints the name of the currently logged-in user.
pwd	Displays the full path of the current working directory.
history	Outputs a list of commands previously executed in the current shell session.
echo Text	Prints the specified text (for example, “Text”) to the terminal window.
date	Shows the current system date and time.
man date	Opens the manual page with detailed documentation for the date command.
man -k password	Searches manual page descriptions for the keyword “password”.
sudo --help	Displays usage information and help for the sudo command.
ls -al	Lists all files and directories, including hidden ones, in long format with detailed information.
locate spotify	Searches the system for files and directories containing “spotify” in their names using a file index database.


## 2. Робота в в терміналі
### 2.1 Робота зі змінними (Variables) та псевдонімами (Aliases) в терміналі:

У цьому пункті було створено змінні з відповідними значеннями та перевірено їх виведення в терміналі. Також було створено псевдонім mycal і продемонстровано його використання.

### 2.2. Робота з функціями (Functions) в терміналі

Було оголошено функцію students_report, після чого виконано її запуск для перевірки коректності роботи.

### 2.3. Робота з лапками (Quoting) в терміналі

Було досліджено використання одинарних та подвійних лапок під час виведення тексту і підстановки значень змінних у командному рядку.

### 2.4. Робота з інструкціями керування (Control Statements) в терміналі

Було застосовано цикл for для автоматизованого виконання команд із попередніх пунктів, що дозволило продемонструвати використання конструкцій керування.

### 2.5. Робота з командами довідки (Man Pages) в терміналі

Було отримано довідкову інформацію про команди за допомогою man та різних параметрів, що дозволило ознайомитися з можливостями вбудованої документації.

---

## Відповіді на контрольні запитання

### 1. Які типи команд існують в оболонці Bash?

В оболонці Bash існують вбудовані команди, зовнішні команди, функції оболонки, аліаси та скрипти, які виконуються в середовищі командного рядка.

### 2. Що таке змінні оточення? Які вони бувають. Як їх можна переглянути в терміналі?

Змінні оточення - це змінні, які зберігають інформацію про середовище роботи користувача та передаються дочірнім процесам; вони бувають локальні та глобальні (експортовані), а переглянути їх можна за допомогою команд env, printenv або echo $ІМʼЯ_ЗМІННОЇ.

### 3. Опишіть змінну $PS1. Як в терміналі переглянути її вміст?

Змінна $PS1 визначає вигляд рядка запрошення в Bash, тобто текст, який відображається перед введенням кожної команди, а переглянути її значення можна командою echo $PS1.

### 4. Як можна змінити значення змінної $PS1? Що при цьому відбудеться в рядку запрошенні в bash (рядок запрошення перед початком кожної команди). Як змінити значення цієї змінної не на поточний сеанс, а за замовчуванням?

мінити значення змінної $PS1 можна присвоївши їй нове значення командою PS1="текст", після чого зміниться вигляд рядка запрошення; щоб зміна діяла постійно, потрібно додати нове значення в файл ~/.bashrc.

### 5. Для чого використовують лапки в оболонці Bash?

Лапки в оболонці Bash використовують для керування обробкою тексту та змінних, де одинарні лапки повністю вимикають підстановку змінних, а подвійні дозволяють їх розгортання.

### 6. Для чого використовують інструкції керування, які їх види Ви знаєте?

Інструкції керування використовують для організації логіки виконання команд у скриптах, до них належать умовні оператори (if), оператор вибору (case), цикли (for, while, until) та логічні оператори (&&, ||).

### 7. В чому різниця якщо в кінці рядку запрошення bash стоїть символ $ чи #? Наприклад на екрані ми бачимо наступні записи

"$" — ви звичайний користувач (обмежені права).

"#" — ви root (адміністратор, повні права).

Тобто різниця в правах доступу до системи.
Якщо в кінці рядка запрошення Bash стоїть символ "$", як у записі [centos@localhost Desktop]$, це означає, що в системі працює звичайний користувач із обмеженими правами, а якщо в кінці стоїть символ "#", як у записі [root@localhost Desktop]#, це означає, що виконання відбувається від імені суперкористувача root, який має повні адміністративні права та може змінювати системні файли й налаштування.
  
### 8. Яке призначення команд whereis та locate? Яка між ними відмінність?

Команда whereis призначена для пошуку розташування виконуваних файлів, вихідного коду та man-сторінок у стандартних каталогах, тоді як locate здійснює швидкий пошук файлів у всій системі за допомогою попередньо створеної бази даних, тому locate знаходить більше результатів і працює швидше.

---

# Conclusion

During this lab work on the topic “Introduction to Basic CLI Commands in Linux”, the main objectives were successfully achieved.

First, we became familiar with the basic principles of working in the Command Line Interface (CLI) environment of a GNU/Linux operating system. We learned how to navigate the file system, identify the current user and directory, view command history, display system date and time, and search for files.

Second, we practiced using essential text-based commands such as whoami, pwd, history, echo, date, man, sudo, ls, and locate. This allowed us to better understand the structure of Linux commands, how options (flags) modify their behavior, and how to access built-in documentation using manual pages.

Additionally, we gained practical experience working in a virtualized environment using Oracle VirtualBox and interacting with Linux alongside Windows OS. This strengthened our practical skills in using multiple operating systems on a single hardware platform.
