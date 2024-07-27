# Операционные системы UNIX/Linux

- [Part 1. Установка ОС](#part-1-установка-ос)

- [Part 2. Создание пользователя](#part-2-создание-пользователя)
    - [Команда adduser](#команда-adduser)<br />
    - [Команда usermod](#команда-usermod)<br />
    - [Команда cat /etc/passwd/](#команда-cat-etcpasswd)<br />

- [*Part 3. Настройка сети ОС*](#part-3-настройка-сети-ос)
    - [Команда hostnamectl](#команда-hostnamectl)<br />
    - [Команда timedatectl](#команда-timedatectl)<br />
    - [Команда ls /sys/class/net/](#команда-ls-sysclassnet)<br />
    - [Команда ip address](#команда-ip-address)<br />
    - [Команда curl](#команда-curl)<br />
    - [Команда ip_route](#команда-ip-route)<br />
    - [Команда vim /etc/netplan/00-installer-config.yaml](#команда-vim-etcnetplan00-installer-configyaml)<br />
    - [Команда ping](#команда-ping)

- [Part 4. Обновление ОС](#part-4-обновление-ос)

- [Part 5. Использование команды sudo](#part-5-использование-команды-sudo)</a>

- [Part 6. Установка и настройка службы времени](#part-6-установка-и-настройка-службы-времени)</a>

- [Part 7. Установка и использование текстовых редакторов](#part-7-установка-и-использование-текстовых-редакторов)</a>
    - [Сохранение изменений в редакторах](#сохранение-изменений-в-редакторах)<br />
    - [Выход без сохранения](#выход-без-сохранения)<br />
    - [Поиск в редакторах](#поиск-в-редакторах)<br />
    - [Поиск/замена в редакторах](#поискзамена-в-редакторах)<br />

- [Part 8. Установка и базовая настройка сервиса SSHD](#part-8-установка-и-базовая-настройка-сервиса-sshd)
    - [Установка службы SSHd](#установка-службы-sshd)<br />
    - [Добавление пакета SSH-сервера](#добавление-пакета-ssh-сервера)<br />
    - [Перенастройка службы SSHd](#перенастройка-службы-sshd)<br />
    - [Команда ps](#команда-ps)<br />
    - [Команда netstat](#команда-netstat)

- [Part 9. Установка и использование утилит top, htop](#part-9-установка-и-использование-утилит-top-htop)
    - [Работа с утилитой *top*](#работа-с-утилитой-top)<br />
    - [Работа с утилитой *htop*](#работа-с-утилитой-htop)<br />

- [Part 10. Использование утилиты fdisk](#part-10-использование-утилиты-fdisk) 

- [Part 11. Использование утилиты df](#part-11-использование-утилиты-df)</a> 

- [Part 12. Использование утилиты du](#part-12-использование-утилиты-du)</a> 

- [Part 13. Установка и использование утилиты ncdu](#part-13-установка-и-использование-утилиты-ncdu)</a> 

- [Part 14. Работа с системными журналами](#part-14-работа-с-системными-журналами)</a> 


- [Part 15. Использование планировщика заданий CRON](#part-15-использование-планировщика-заданий-cron)</a> 

---


## Part 1. Установка ОС
<table>
<tr>
        <th width=370px>

- Что-бы узнать версию Ubuntu<br />
выполняем команду  <kbd>cat /etc/issue</kbd>.<br /><br />


</tr>
<tr>
<td><br />

***Вывод команды***<br /><br />

</td>
</tr>
<tr>
<td></td>
<td><br />

![report](Screenshots/OS/cat%20_etc_issue%20command%20output.png)<br />
</td>
</tr>

</table>

---

## Part 2. Создание пользователя

<table>


<tr>
        <th width=370px>

### Команда *adduser*
позволяет создать<br />нового системного пользователя.<br /><br />
</th>

</tr>
    <tr>
    <td><br />

***Вывод команды***<br /><br />

</td>
    </tr>
    <tr>
        <td>

*Поля с информацией о новом пользователе*<br />
*можно оставить пустыми.**
        
<br /><br />
<code>Changing the user information for wall-e</code><br /></td>
        <td>

![report](Screenshots/New%20user/sudo_adduser_user%20command%20output.png)<br />

</td>

</tr>
</table>
<br />

<table>
<tr>
<th width=370px>

### Команда *usermod*
Для добавления пользователя в<br />группу *adm*.<br /><br />
</th>
</tr>
    <tr>
    <td><br />

***Вывод команды***<br /><br />

</td>
    </tr>
    <tr>
        <td>

*водим пароль пользователя.**
<br/>
<code>[sudo] password for evangelh:</code></td>
<td><br />

![report](Screenshots/New%20user/sudo_usermod_-aG_adm_user%20command%20output.png)
</td>
</tr>

</table>
<br />

<table>
<tr>
        <th width=370px>

### Команда *cat /etc/passwd*
Новый пользователь должен быть в<br />выводе команды.<br />
</th>

</tr>
    <tr>
    <td><br />

***Вывод команды***<br /><br />
</td>
    </tr>

<tr>
    <td>
</td>
<td><br />

![report](Screenshots/New%20user/cat%20_etc_passwd%20command%20output.png)
</td>
</tr>
</table>

---

## Part 3. Настройка сети ОС



<table>
<tr>
        <th width=370px>

### Команда *hostnamectl*
Позволяет установить<br />новое значение Hostname.<br />Используется аргумент <kbd>set-hostname</kbd>.<br />
</th>

</tr>
    <tr>
    <td><br />

***Вывод команды***<br /><br />

</td>
    </tr>
    <tr>
        <td>

*Вводим пароль пользователя.**
<br/>
<code>[sudo] password for evangelh:</code>

</td>
        <td><br />

![report](Screenshots/DHCPip/sudo_hostnamectl_set-hostanme%20command%20output.png)<br />

</td>

</tr>
</table>


<table>
<tr>
        <th width=370px>

### Команда *timedatectl*
Позволяет установить<br />новое значение Hostname.<br />Используется аргумент <kbd>set-timezone</kbd>.<br />
</th>

</tr>
    <tr>
    <td><br />

***Вывод команды***<br /><br />

</td>
    </tr>
    <tr>
        <td>

*Вводим пароль пользователя.**
<br/>
<code>[sudo] password for evangelh:</code>

</td>
        <td><br />

![report](Screenshots/DHCPip/sudo_timedatectl_set-timezone%20command%20output.png)<br />

</td>

</tr>
</table>

<table>
<tr>
        <th width=370px>

### Команда *ls /sys/class/net/*
Позволяет вывести<br />названия сетевых интерфесов.<br />
</th>

</tr>
    <tr>
    <td><br />

***Вывод команды***<br /><br />

</td>
    </tr>
    <tr>
        <td>

<code>ls /sys/class/net/</code><br /><br />

*lo** *(loopback device) – виртуальный интерфейс, <br />присутствующий по умолчанию в любом Linux.<br /> Он используется для отладки сетевых программ<br /> и запуска серверных приложений <br />на локальной машине.<br /> С этим интерфейсом всегда связан адрес 127.0.0.1.<br /> У него есть dns-имя – localhost.<br /> Посмотреть привязку можно в файле /etc/hosts.***

</td>
        <td>

![report](Screenshots/DHCPip/ls_sys_class_net%20command%20output.png)<br />

</td>

</tr>
</table>


<table>
<tr>
        <th width=370px>

### Команда *ip address*
Позволяет вывести<br />
список сетевых интерфесов.<br />
</th>

</tr>
    <tr>
    <td><br />

***Вывод команды***<br /><br />

</td>
    </tr>
    <tr>
        <td>


*DHCP — протокол прикладного уровня<br /> модели TCP/IP, служит для назначения IP-адреса<br /> клиенту. Это следует из его названия —<br /> Dynamic Host Configuration Protocol.<br /> IP-адрес можно назначать вручную каждому клиенту,<br /> то есть компьютеру в локальной сети.<br /> Но в больших сетях это очень трудозатратно,<br /> к тому же, чем больше локальная сеть,<br /> тем выше возрастает вероятность ошибки<br /> при настройке. Поэтому для автоматизации <br />назначения IP был создан протокол DHCP.*<br /><br />

*Впервые протокол был описан в 1993 году в документе<br /> <a href="https://datatracker.ietf.org/doc/html/rfc1531">**RFC 1531**</a>, но с тех пор в описание вносились правки.<br />На сегодняшний день основным документом,<br /> регламентирующим протокол, является <a href="https://datatracker.ietf.org/doc/html/rfc2131">**RFC 2131**</a>.<br /> Помимо автоматизации процесса настройки IP,<br /> DHCP позволяет упростить диагностику<br /> подключения и переход из одной подсети в другую,<br /> оставляя уведомления для системного<br />администратора в логах.* 

</td>
        <td>

![report](Screenshots/DHCPip/ip_address_show%20command%20output.png)<br />

</td>
</tr>
</table>

<table>
<tr>
<th width=370px>


### Команда *curl*
Позволяет обратиться к сайту.<br />Используется аргумент <kbd>tnx.nl/ip</kbd><br />сайт вернет внешний ip.<br />
</th>

</tr><tr>
    <td><br />

***Вывод команды***<br /><br />

</td>
</tr><tr>
<td>
</td>
        <td><br />

![report](Screenshots/DHCPip/curl_tnx_nl_ip%20command%20output.png)<br />

</td>

</tr>
</table>

<table>
<tr>
        <th width=370px>

### Команда *ip route*
Позволяет вывести ip.<br />Используется аргумент <kbd>grep default</kbd>.<br />
</th>

</tr>
    <tr>
    <td><br />

***Вывод команды***<br /><br />

</td>
    </tr>
    <tr>
<td></td>
        <td><br />

![report](Screenshots/DHCPip/ip_route_grep_default%20command%20output.png)<br />

</td>
</tr>
</table>

<table>
<tr>
<th width=370px>


### Команда *vim /etc/netplan/00-installer-config.yaml*
Для редактирования файла <kbd>*.yaml</kbd> в папке<br /><kbd>/etc/netplan/</kbd>.<br />
</th>
</tr>
<tr>
<td><br />

***Вывод команды***<br /><br />

</td>
</tr>
<tr>
<td>

***addresses** — ip адрес который будет<br />
назначен вашей сетевой карте.<br />
**gateway4** — ip адрес роутера.<br />
**nameservers** — DNS сервера. Первый -<br />
наш роутер.*</div>
<code>sudo apply netplan*</code><br />
*Применить изменения**<br />
</td>
<td><br />

![report](Screenshots/DHCPip/vim_etc_netplan%20command%20output.png)<br />

</td>
</tr>
</table>

<table>
<tr>
<th width=370px>

### Команда *ping*
Для проверки работы сети.<br />
<kbd>1.1.1.1</kbd> и <kbd>ya.ru</kbd> в качестве аргумента.<br />
</th>
</tr>
<tr>
<td><br />

***Вывод команды***<br /><br />

</td>
</tr>
<tr>
<td>
<code>ping 1.1.1.1</code>
</td>
<td><br />

![report](Screenshots/DHCPip/ping%201_1_1_1%20command%20output.png)<br />

</td>
</tr>
<td>
<code>ping ya.ru</code>
</td><td><br />

![report](Screenshots/DHCPip/ping%20ya_ru%20command%20output.png)<br /></td>
</table>

---

## Part 4. Обновление ОС



<table>
<tr>
<th width=370px>


- Команда <kbd>apt-get update</kbd> позволяет обновить<br /> списки пакетов, которые доступны для<br /> загрузки в системе. После того, как списки <br /> будут обновлены, вводим команду<br />  для обновления установленных пакетов.<br /><kbd>apt-get upgrade</kbd>.<br />
</th>

</tr>
    <tr>
    <td><br />

***Вывод команды***<br /><br />

</td>
</tr><tr>
<td>

*После обновления системных пакетов,<br /> если ввести команду обновления повторно,<br /> должно появится сообщение,<br />что обновления отсутствуют.*</div></td>
<td><br />

![report](Screenshots/Upgrade%20OS/apt-get%20upgrade%20command%20output.png)<br />
</td>

</tr>
</table>

## Part 5. Использование команды sudo



<table>
<tr>
        <th width=370px>


- Для добавления пользователя в<br />группу *sudo* используем команду <kbd>usermod</kbd>.<br /> Командой <kbd>su wall-e</kbd> переходим на учетную<br /> запись пользователя дальше используя<br /> <kbd>sudo hostnamectl set-hostname user-2</kbd><br />меняем *hostname ОС*
<br />
</th>

</tr>
    <tr>
    <td><br />

***Вывод команды***<br /><br />

</td>
</tr><tr>
<td>

*водим пароль пользователя.*
<br/>
<code>
[sudo] password for wall-e:
</code></td>
<td><br />

![report](Screenshots/CommandSudo/comand_sudo%20command%20output.png)<br />
</td>

</tr>
</table>

## Part 6. Установка и настройка службы времени

<table>
<tr>
        <th width=370px>


- Командой <kbd>timedatectl set-ntp true</kbd><br />
включаем использование systemd-timesyncd<br />
для синхронизации времени.<br />
Включаем и перезапускаем службу<br />
systemd-timesyncd<br />
<kbd>systemctl enable --now systemd-timesyncd.service</kbd><br />
<kbd>systemctl restart systemd-timesyncd.service</kbd>
<br />
</th>

</tr>
    <tr>
    <td><br />

***Вывод команды***<br /><br />

</td>
</tr><tr>
<td>
<code>systemctl status systemd-timesyncd.service</code></td>
<td><br />

![report](Screenshots/timesync/timesync%20command%20output.png)<br />
</td>

</tr>
<td>
<code>timedatectl show</code>
</td>
<td><br />

![report](Screenshots/timesync/timedatectl_show%20command%20output.png)<br />

</table>

---

## Part 7. Установка и использование текстовых редакторов

<table>
<tr>
<th width=370px>

### *Сохранение изменений в редакторах*
VIM, NANO, MCEDIT.
<br />
</th>

</tr>
<tr>
<td><br />

***Вывод команды***<br /><br />

</td><td>

*Для выхода из VIM<br />с сохранением изменений*
<kbd>:</kbd>+<kbd>wq</kbd><br />*и имя файла.*</td>
<td>

*Для выхода из NANO<br />с сохранением изменений*
<kbd>ctrl</kbd>+<kbd>o</kbd><br />*и имя файла.* <kbd>ctrl</kbd>+<kbd>x</kbd> для выхода.</td>
<td>

*Для выхода из MCEDIT<br />с сохранением изменений*
<kbd>F2</kbd><br />*и имя файла.* <kbd>F10</kbd> для выхода.</td>

</tr><tr>
<td></td>
<td ><br />

![report](Screenshots/Editor/vim_new_file%20command%20output.png)<br />
</td>

<td><br />

![report](Screenshots/Editor/nano_new_file%20command%20output.png)<br />
</td>
<td><br />

![report](Screenshots/Editor/mcedit_new_file%20command%20output.png)<br />
</td>
</tr>

</table>

<table>
<tr>
        <th width=370px>

### *Выход без сохранения*
VIM, NANO, MCEDIT.
<br />
</th>

</tr>
<tr>
<td><br />

***Вывод команды***<br /><br />

</td><td>

*Для выхода из VIM<br />без сохранением изменений*
<kbd>:</kbd>+<kbd>q!</kbd><br /></td>
<td>

*Для выхода из NANO без<br /> сохранением изменений*
<kbd>ctrl</kbd>+<kbd>x</kbd>.<br /> при запросе <kbd>Save modified buffer?</kbd><br /> подтвердить нажатием клавиши <kbd>n</kbd></td>
<td>

*Для выхода из MCEDIT<br />без сохранением изменений*
<kbd>F10</kbd>.<br /> при запросе <kbd>Save before close?</kbd><br /> подтвердить нажатием клавиши <kbd>n</kbd></td>

</tr><tr>
<td></td>
<td><br />

![report](Screenshots/Editor/vim_dont_save_file%20command%20output.png)<br />
</td>

<td><br />

![report](Screenshots/Editor/nano_dont_save_file%20command%20output.png)<br />
</td>
<td><br />

![report](Screenshots/Editor/mcedit_dont_save_file%20command%20output.png)<br />
</td>
</tr>
</table>

<table>
<tr>
<th width=370px>



### *Поиск* в редакторах
VIM, NANO, MCEDIT.
<br />
</th>
</tr>
<tr>
<td>

***Вывод команды***

</td><td>

*Для поиска в VIM<br />*
<kbd>/</kbd>+<kbd>шаблон</kbd><br /></td>
<td>

*Для поиска в NANO*<br /><kbd>ctrl</kbd>+<kbd>w</kbd>. *При запросе* <br /><kbd>Search:</kbd> *Ввести шаблон.*</td>
<td>

*Для поиска в MCEDIT* <kbd>F7</kbd>.<br /> *при запросе* <kbd>Enter search string:</kbd><br /> *ввести шаблон. и подтвердить* <kbd>ok</kbd></td>

</tr><tr>
<td></td>
<td><br />

![report](Screenshots/Editor/vim_find%20command%20output.png)<br />
</td>

<td><br />

![report](Screenshots/Editor/nano_find%20command%20output.png)<br />
</td>
<td><br />

![report](Screenshots/Editor/mcedit_find%20command%20output.png)<br />
</td>
</tr>
</table>

<table>
<tr>
        <th width=370px>

### *Поиск/замена* в редакторах
VIM, NANO, MCEDIT.
<br />
</th>
</tr>
<tr>
<td><br />

***Вывод команды***<br /><br />

</td><td>

*Для замены в VIM<br />*
<kbd>:</kbd>+<kbd>%s</kbd>/<kbd>шаблон</kbd>/<kbd>строка</kbd>/<kbd>флаг</kbd><br /></td>
<td>

*Для замены в NANO*<br /><kbd>ctrl</kbd>+<kbd>\\</kbd>. *При запросе* <br /><kbd>Search:</kbd> *Ввести шаблон.*<br />*При запросе* <kbd>Replace with:</kbd><br />*ввести строку замены.*<br /> *Подтвердить.*</td>
<td>

*Для замены в MCEDIT* <kbd>F4</kbd>.<br /> *при запросе* <kbd>Enter search string:</kbd><br /> *ввести шаблон.*<br /><kbd>Enter replacement string:</kbd><br />*ввести строку для замены*<br /> *Подтвердить.* <kbd>ok</kbd> <kbd>Replace</kbd></td>

</tr><tr>
<td></td>
<td><br />

![report](Screenshots/Editor/vim_replace%20command%20output.png)<br />
</td>

<td><br />

![report](Screenshots/Editor/nano_replace%20command%20output.png)<br />
</td>
<td><br />

![report](Screenshots/Editor/mcedit_replace%20command%20output.png)<br />
</td>
</tr>
</table>

## Part 8. Установка и базовая настройка сервиса SSHD

<table>
<tr>
<th width=370px>



### *Установка службы SSHD*

</th>
</tr><tr>
<td ><br />

***Вывод команды***<br /><br />

</td><td>

<br />Установка OpenSSH\*<kbd>:</kbd>+<kbd>wq</kbd><br />*и имя файла.*</td>

</tr><tr>
<td>

*SSH (Secure Shell) — сетевой протокол*<br /> прикладного уровня, который позволяет<br />управлять операционной системой и<br />выполнять функцию тунеллирования\*\*<br />TCP-соединения. Работа SSH построена<br /> на взаимодействии 2-х компонентов:<br />SSH-сервера и SSH-клиента.<br /><br />\**OpenSSH (Open Secure Shell)* —<br />набор программ, который позволяет<br />шифровать сеансы связи в сети. При таких<br />сеансах используется протокол SSH.<br /><br />\*\**Тунеллирование* - процесс, при котором<br />создаётся соединение между двумя<br />конечными точками с помощью изоляции<br />передаваемых данных.</td>
<td><br />

для установки OpenSSH:<br />1. обновите репозиторий командой: <kbd>sudo apt update</kbd><br />2. Установите SSH с помощью команды: <kbd>sudo apt-get install ssh</kbd><br />3. Установите OpenSSH: <kbd>sudo apt install openssh-server</kbd><br />4. Проверьте работу SSH: <kbd>systemctl status sshd</kbd><br /><br />
![report](Screenshots/SSHD/install_sshd%20command%20output.png)
</td>
</tr>
</table>

<table>
<tr>
        <th width=370px>


### Добавление пакета *SSH-сервера*
В автозагрузку: <kbd>sudo systemctl enable sshd</kbd>.<br />
</th>
</tr>
</table>

<table>
<tr>
        <th width=370px>


### Перенастройка службы *SSHd*
На порт 2022, файл: <kbd>/etc/ssh/sshd_config</kbd>.<br />
</th>
</tr><tr>
<td><br />

***Вывод команды***<br /><br />

</td><td>

<br />Редактируем файл <br /><kbd>sudo vim /etc/ssh/sshd_config</kbd><br /></td>
<td>

<br />Чтобы изменения вступили в силу,<br /> перезапустите SSH-сервер: <br /><kbd>systemctl restart sshd</kbd><br /></td>

</tr><tr>
<td></td>
<td><br />


![report](Screenshots/SSHD/edit_file_sshd_config%20command%20output.png)
</td><td><br />

![report](Screenshots/SSHD/systemctl_restart_sshd%20command%20output.png)</td>


</tr>
</table>

<table>
<tr>
        <th width=370px>



### Команда *ps*
Можно увидеть процесс sshd.<br /> Используем с командой grep<br />

<kbd>ps -A | grep sshd</kbd><br />
</th>
</tr><tr>
<td ><br />

***Вывод команды***<br /><br />

</td>


</tr><tr>
<td>

<br />*Команда ps выводит список текущих*<br /> *процессов на вашем сервере в виде*<br /> *таблицы, с которой можно удобно*<br /> *работать: сортировать, изменять*<br /> *количество колонок и прочие. У утилиты*<br /> *ps множество настроек, с помощью которых*<br /> *можно тонко настраивать вывод команды*<br /><br />

-A, -e, (a) - выбрать все процессы;<br />
-a - выбрать все процессы, кроме фоновых;<br />
-d, (g) - выбрать все процессы, даже фоновые,<br /> кроме процессов сессий;<br />
-N - выбрать все процессы кроме указанных;<br />
-С - выбирать процессы по имени команды;<br />
-G - выбрать процессы по ID группы;<br />
-p, (p) - выбрать процессы PID;<br />
--ppid - выбрать процессы по PID<br /> родительского процесса;<br />
-s - выбрать процессы по ID сессии;<br />
-t, (t) - выбрать процессы по tty;<br />
-u, (U) - выбрать процессы пользователя.<br /><br />

Утилита grep помогает фильтровать<br> результаты из команды ps, например,<br /> чтобы вывести строки<br />содержащие ключевое слово.<br /><br />
</td>

<td><br />


![report](Screenshots/SSHD/ps_a_grep%20command%20output.png)
</td>


</tr>

</table>


<table>
<tr>
        <th width=370px>


### Команда *netstat*
Для анализа статистики сети.<br />
Перезагрузка машины *reboot*.<br /> <br />


</th>

</tr><tr>
<td><br />

***Вывод команды***<br /><br />
</td>
<td>Вывод команды netstat -tan должен содержать<br />
<kbd>tcp 0 0 0.0.0.0:2022 0.0.0.0:* LISTEN</kbd></td>
</tr><tr>
<td>для установки netstat вводим:<br />
<kbd>sudo apt install net-tools</kbd><br /><br />

-t – используется для вывода TCP-соединений<br />
-n – не резолвить имена из IP-адресов<br />
-a или -all — выводит информацию о всех<br />
сокетах(об активных которые слушают порты<br />
и неактивных, которые не слушают).<br /><br />

Командная утилита netstat поддерживает<br />
параметры, которые отображают активные<br />
или пассивные сокеты с помощью параметров<br />
-t, -n и -a. Флаги показывают сокеты<br />
подключения RAW, UDP, TCP или UNIX.<br />
Добавив опцию -a, он будет сеять готовые<br />
к подключению сокеты.</div><br /></td>

<td><br />

![report](Screenshots/SSHD/netstat_tan%20command%20output.png)
</td>

</tr>

</table>

## Part 9. Установка и использование утилит top, htop


<table>
<tr>
        <th width=370px>



### Работа с утилитой *top*
<br />

</th>

</tr><tr>
<td ><br />

***Вывод команды***<br /><br />

</td>

</tr><tr>
<td>

- top<br />
  - uptime - 1:29<br />
  - кол-во авторизованных<br />
  пользователей - 1 user<br />
  - общая загрузка системы -<br />
  load average: ...<br />
  - общее количество процессов -<br />
  Tasks: 96 total ...<br />
  - загрузка cpu - %Cpu(s): ...<br />
  - загрузка памяти - MiB Mem : ... <br />
  - для сортировки по памяти <kbd>M</kbd><br />
  pid 641
  - для сортировки по<br />
  использованию CPU <kbd>P</kbd><br />
  pid 1201<br />


  
</td>
<td><br />

</kbd><br /><br />

top

![report](Screenshots/top_htop/top%20command%20output.png)<br />

sort M

![report](Screenshots/top_htop/top_sort_M%20command%20output.png)<br />

sort P

![report](Screenshots/top_htop/top_sort_P%20command%20output.png)
</td>
</tr>
</table>

<table>
<tr>
        <th width=370px>



### Работа с утилитой *htop*
<br />

</th>
</tr><tr>
<td ><br />

***Вывод команды***<br /><br />

</td><td>

- htop<br />

  - сортировка по PID, PERCENT_CPU, PERCENT_MEM, TIME<br />

  - фильтрация для процесса sshd<br />

  - процесс syslog, найденным, используя поиск<br />

  - добавленный вывод hostname, clock и uptime<br />
  
</td>

</tr>
<tr>
<td>
</td>
<td><br />

</kbd><br /><br />
Sort PID

![report](Screenshots/top_htop/htop_sort_PID%20command%20output.png)<br />
Sort CPU

![report](Screenshots/top_htop/htop_sort_CPU%20command%20output.png)<br />
Sort MEM

![report](Screenshots/top_htop/htop_sort_MEM%20command%20output.png)<br />
Sort TIME

![report](Screenshots/top_htop/htop_sort_TIME%20command%20output.png)<br />
Filter sshd

![report](Screenshots/top_htop/htop_filter_SSHD%20command%20output.png)<br />
Search syslog

![report](Screenshots/top_htop/htop_search_syslog%20command%20output.png)<br />
Setup hostname clock uptime

![report](Screenshots/top_htop/htop_setup%20command%20output.png)<br />

</td>
</tr>
</table>


## Part 10. Использование утилиты fdisk

<table>
<tr>
<th width=370px>



Работа с утилитой *fdisk*
<br />

</th>
</tr><tr>
<td ><br />

***Вывод команды***<br /><br />

</td>

</tr><tr>
<td>

*Название жесткого диска: sda<br />
Его размер: 10 Gib<br />
Количество секторов: 20971520<br />
Размер swap можно узнать<br />
командой <kbd>free</kbd> 1517564 kb*<br /> 
</td>
<td><br />

![report](Screenshots/fdisk/fdisk_l%20command%20output.png)

![report](Screenshots/fdisk/free_swap%20command%20output.png)
</td>


</tr>

</table>

## Part 11. Использование утилиты df


<table>
<tr>
        <th width=370px>


Работа с утилитой *df*<br />
Запустить команду <kbd>df /</kbd>.<br />
Запустить команду <kbd>df -Th /</kbd>.<br />

</th>

</tr><tr>
<td ><br />

***Вывод команды***<br /><br />

</td>

</tr><tr>
<td>

- Размер раздела: 8408452 kb<br />
- Размер занятого пространства: 4194960 kb<br />
- Размер свободного пространства: 3764776 kb<br />
- Процент использования: 53%<br /><br />

- Размер раздела: 8.1G<br />
- Размер занятого пространства: 4.1G<br />
- Размер свободного пространства: 3.6G<br />
- Процент использования: 53%<br /><br />

ext4 (англ. fourth extended file system, ext4fs)<br />
— журналируемая* файловая система,<br />
используемая преимущественно в операционных<br />
системах с ядром Linux, созданная на базе<br />
ext3 в 2006 году.<br ><br />

*Журналируемая файловая система — файловая система,<br />
в которой осуществляется ведение журнала,<br />
хранящего список изменений и,<br />
в той или иной степени, помогающего<br />
сохранить целостность файловой<br />
системы при сбоях.<br />


 
</td>
<td><br />

![report](Screenshots/df/df%20command%20output.png)<br /><br />

![report](Screenshots/df/df_Th%20command%20output.png)
</td>


</tr>

</table>

## Part 12. Использование утилиты du


<table>
<tr>
<th width=370px>


Работа с утилитой *du*
<br />

</th>

</tr><tr>
<td><br />

***Вывод команды***<br /><br />

</td>

</tr><tr>
<td>

- Выведем размер папок /home, /var, /var/log<br />
(в байтах, в человекочитаемом виде)<br /><br />

- Вывести размер всего содержимого<br />
в /var/log (каждого<br />
вложенного элемента, используя *)<br /><br />
 
</td>

<td><br />

du /home -s<br >
![report](Screenshots/Du/du_home_b%20command%20output.png)<br />

du /var -s<br />
![report](Screenshots/Du/du_var_b%20command%20output.png)<br />

du /var/log -s<br />
![report](Screenshots/Du/du_var_log_b%20command%20output.png)<br />

du /var/log/* -s<br />
![report](Screenshots/Du/du_var_log_*_b%20command%20output.png)<br />
</td>
<td><br />

du /home -sh<br >
![report](Screenshots/Du/du_home%20command%20output.png)<br />

du /var -sh<br />
![report](Screenshots/Du/du_var%20command%20output.png)<br />

du /var/log -sh<br />
![report](Screenshots/Du/du_var_log%20command%20output.png)<br />

du /var/log/* -sh<br />
![report](Screenshots/Du/du_var_log_*_%20command%20output.png)<br />
</td>


</tr>
</table>

## Part 13. Установка и использование утилиты ncdu



<table>
<tr>
<th width=370px>


Работа с утилитой *ncdu*
<br />

</th>

</tr><tr>
<td ><br />

***Вывод команды***<br /><br />

</td>

</tr><tr>
<td>

- Выведем размер папок /home, /var, /var/log<br />
(в байтах, в человекочитаемом виде)<br /><br />

- Вывести размер всего содержимого<br />
в /var/log (каждого<br />
вложенного элемента, используя *)<br /><br />
 
</td>
<td><br />

du /home -b<br >
![report](Screenshots/ncdu/ncdu_home%20command%20output.png)<br />
</td>
<td>

du /var -b<br />
![report](Screenshots/ncdu/ncdu_var%20command%20output.png)<br />
</td>
<td>

du /var/log -b<br />
![report](Screenshots/ncdu/ncdu_var_log%20command%20output.png)<br />
</td>


</tr>

</table>

## Part 14. Работа с системными журналами


<table>
<tr>
<th width=370px>


Работа с системными журналами<br />
<kbd>vim /var/log/dmesg</kbd><br />
<kbd>vim /var/log/syslog</kbd><br />
<kbd>vim /var/log/auth.log</kbd><br />

</th>

</tr><tr>
<td ><br />

***Вывод команды***<br /><br />

</td>
</tr><tr>
<td>
Последняя авторизация<br />
сохраняется в журнале<br />
<kbd>cat /var/log/auth.log | grep login</kbd><br />
Командой <kbd>last</kbd>
можно вывести<br />
историю входа в ситсему.<br /><br />
Перезапуск службы SSHd.<br />
отмечается в журнале<br />
<kbd>cat /var/log/syslog</kbd><br />

<br />
</td>
<td><br />

last login<br />
![report](Screenshots/log/log_auth_last%20command%20output.png)<br /><br />

ssh res<br />
![report](Screenshots/log/log_sshd_res%20command%20output.png)<br /><br />
</td>



</tr>

</table>

## Part 15. Использование планировщика заданий CRON



<table>
<tr>
        <th width=370px>


Планировщик заданий *CRON*<br />

</th>

</tr><tr>
<td ><br />

***Вывод команды***<br /><br />

</td>

</tr><tr>
<td>
<br />
Для поиска запускаемой команды в логах<br />
<kbd>cat /var/log/syslog | grep uptime</kbd><br /><br />
<kbd>crontab -e</kbd> редактировать таблицу задач<br /><br  />
<kbd>crontab -l</kbd> показать таблицу задач<br /><br />
<kbd>crontab -r</kbd> удалить таблицу задач<br /><br />


<br />
</td>
<td><br />

log<br />
![report](Screenshots/cron/cron%20command%20output.png)<br /><br />

task<br />
![report](Screenshots/cron/crontab%20-l%20command%20output.png)<br /><br />

clear task<br />
![report](Screenshots/cron/crontab_clear%20-l%20command%20output.png)<br /><br />

</td>
</tr>
</table>

---

<table><tr><th> 05.09.2023 evangelh</th></tr><table>





