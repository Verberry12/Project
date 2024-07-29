## Part 1. Установка ОС

- Узнаем версию Ubuntu после установки
![part_1](image/part_1.png)
  
  

## Part 2. Создание пользователя

- Создаем нового пользователя и добавляем его в группу adm
![part_2.1](image/part_2.1.png)

- Командой выводим список пользователей
![part_2.2](image/part_2.2.png)
  
  
  
## Part 3. Настройка сети ОС

- Задали название машины и вывели его в терминал
![part_3.1](image/part_3.1.png)

- Установили текущую временную зону и вывели информацию в терминал
![part_3.2](image/part_3.2.png)

- Установили набор сетевых инструментов и вывели информацию о сетевых интерфейсах
![part_3.3](image/part_3.3.png)

  ***lo (loopback device) - виртуальный интерфейс, присутствующий по умолчанию в любом Linux. Он используется для отладки сетевых программ и запуска серверных приложений на локальной машине. С этим интерфейсом всегда связан адрес 127.0.0.1. У него есть dns-имя – localhost***
  
- Получаем новый ip адрес устройства от dhcp сервера
![part_3.4](image/part_3.4.png) 

  ***DHCP - Dynamic Host Configuration Protocol - протокол прикладного уровня модели TCP/IP, служит для назначения IP-адреса клиенту***
    
- Вывели внешний IP-адрес шлюза (ip)
![part_3.5.1](image/part_3.5.1.png)

- Вывели внутренний IP-адрес шлюза, он же ip-адрес по умолчанию 
 ![part_3.5.2](image/part_3.5.2png)

- Задали статичные настройки ip, gw, dns 
![part_3.6.1](image/part_3.6.1.png)
![part_3.6.2](image/part_3.6.2.png)

- Перезагрузили машину и убедились, что статичные сетевые настройки (ip, gw, dns) соответствуют заданным в предыдущем пункте
![part_3.7.1](image/part_3.7.1.png)

- Успешно пропинговали удаленные хосты 1.1.1.1 и ya.ru
![part_3.7.2](image/part_3.7.2.png)
  


## Part 4. Обновление ОС

- Обновили системные пакеты до последней на момент выполнения задания версии и проверили повторным вводом команды
![part_4](image/part_4.png) 
  
  

## Part 5. Использование команды **sudo**

 ***Sudo — Substitute User and do, дословно «подменить пользователя и выполнить» - команда, позволяющая пользователю запускать программы с привилегиями другой учётной записи, как правило, суперпользователя root. Ее используют прежде какой-либо иной команды в консоли для выполнения с правами администратора***

- Поменяли hostname ОС от имени пользователя, созданного в пункте Part 2, используя sudo
![part_5](image/part_5.png) 



## Part 6. Установка и настройка службы времени

- Вывод команды с корректным временем
![part_6.1](image/part_6.1.png) 
![part_6.2](image/part_6.2.png) 
![part_6.3](image/part_6.3.png) 



## Part 7. Установка и использование текстовых редакторов 

- Установлены текстовые редакторы VIM, NANO, JOE 

--- 
  
### VIM

- vim test_VIM.txt
- Режим редактирования: i
- Выйти из режима редактирования: esc
- Выход с cохранением: :wq и enter

![part_7.1.1](image/part_7.1.1.png) 


### NANO

- nano test_NANO.txt
- Выход с сохранением: CTRL+X, затем Y и enter

![part_7.2.1](image/part_7.2.1.png) 
  


### JOE 

- joe test_JOE.txt
- Выход с cохранением: Ctrl+K, затем клавиша X

![part_7.3.1](image/part_7.3.1.png) 
  
---

### VIM

- Выйти из режима редактирования: esc
- Выход без сохранения: :q! и enter

![part_7.1.2](image/part_7.1.2.png)


### NANO

- Выход без сохранения: CTRL+X, затем N

![part_7.2.2](image/part_7.2.2.png)


### JOE 

- Выход без сохранения: Ctrl+C, затем клавиша Y 

![part_7.3.2](image/part_7.3.2.png) 
  
---

### VIM

- Поиск: /<что ищем> (для перемещения: N - назад, n - вперед)
- Замена:  :s/<что хотим заменить>/<на что хотим заменить> + enter

![part_7.1.3.1](image/part_7.1.3.1.png)
  
![part_7.1.3.2](image/part_7.1.3.2.png)


### NANO

- Поиск: CTRL+W, <что ищем> + enter (alt+W для перехода к след. вхождению, ctrl+C для прекращения поиска)
- Замена: CTRL+ \ <что хотим заменить> + enter + <на что хотим заменить> + enter, затем A(для замены всех найденных) или Y или N (при замене каждого по отдельности)

![part_7.2.3.1](image/part_7.2.3.1.png)
  
![part_7.2.3.2](image/part_7.2.3.2.png)


### JOE 

- Поиск: CTRL+K, затем F + enter <что ищем>
- Замена: CTRL+K затем F + enter <что хотим заменить>, затем R <на что хотим заменить>, затем Y

![part_7.3.3.1](image/part_7.3.3.1.png)
  
![part_7.3.3.2](image/part_7.3.3.2.png)
  
  
  
## Part 8. Установка и базовая настройка сервиса SSHD

- Устанавили службу SSHd
![part_8.1](image/part_8.1.png)
    
- Добавляем автостарт службы при загрузке системы
- Перенастроили службу SSHd на порт 2022
![part_8.2](image/part_8.2.png)

![part_8.3](image/part_8.3.png)
    
- Перезагрузили систему
    
- Используя команду ps, показать наличие процесса sshd. Для этого к команде нужно подобрать ключи

  ***команда ps - показывает запущенные процессы, выполняемые пользователем в окне терминала***
  
    - ps -e или ps -A (Чтобы просмотреть все запущенные процессы);
    - ps -d (Чтобы показать все процессы, кроме лидеров сессии);
    - ps -d -N (можно инвертировать вывод с помощью переключателя -N. Например, если хочу вывести только лидеров сеансов)
    - ps T (увидеть только процессы, связанные с этим терминалом);
    - ps r (просмотреть все работающие (running) процессы);
    - ps -p 'pid' (если вы знаете идентификатор процесса PID, вы можете просто использовать следующую команду, для вывода процесса с этим 'pid');
    - ps U 'userlist' (найти все процессы, выполняемые конкретным пользователем);
    - ps -ef (получить полный список);

![part_8.4](image/part_8.4.png)
  
- grep sshd - поиск по выводу

- Перезагрузили систему (reboot)

- Команда netstat
   - -t (--tcp) отображает соедниеня только по tcp
   - -a (--all) вывод всех активных подключений TCP
   - -n (--numeric) вывод активных подключений TCP с отображением адресов и номеров портов в числовом формате

![part_8.5](image/part_8.5.png)

    - Proto: Название(тип) протокола (протокол TCP или протокол UDP);
    - Recv-Q: очередь получения сети (Счётчик байтов не скопированных программой пользователя из этого сокета)
    - Send-Q: сетевая очередь отправки (Счётчик байтов, не подтверждённых удалённым узлом)
    - Local Address: адрес локального компьтера и используемы номер порта
    - Foreign Address: адрес и номер удаленного компьтера к которому подключен сокет
    - State: состояние сокета
    - 0.0.0.0: означает IP-адрес на локальной машине (это немаршрутизируемый адрес IPv4, который используется в качестве адреса по умолчанию или адреса-заполнителя)



## Part 9. Установка и использование утилит **top**, **htop**

- По выводу команды top определили и отразили в отчёте данные
![part_9.1.1](image/part_9.1.1.png)

    - uptime: 5:56
    - количество авторизованных пользователей: 1
    - общая загрузка системы: 0.05, 0.02, 0.00
    - общее количество процессов: 96
    - загрузка cpu: 0.0
    - загрузка памяти: 198.2/267.1
    - pid процесса занимающего больше всего памяти(top -o %MEM): 2801
![part_9.1.2](image/part_9.1.2.png)
    - pid процесса, занимающего больше всего процессорного времени(top -o %CPU): 3051
![part_9.1.3](image/part_9.1.3.png)

- Вывод команды htop, отсортированный по PID, PERCENT_CPU, PERCENT_MEM, TIME
![part_9.2.1](image/part_9.2.1.png)

![part_9.2.2](image/part_9.2.2.png)
    
![part_9.2.3](image/part_9.2.3.png)
      
![part_9.2.4](image/part_9.2.4.png)
  
- Вывод команды htop, отфильтрованный для процесса sshd
![part_9.2.5](image/part_9.2.5.png)
  
- Вывод команды htop с процессом syslog, найденным, используя поиск
![part_9.2.6](image/part_9.2.6.png)
  
- Вывод команды htop с добавленным hostname, clock и uptime  
![part_9.2.7](image/part_9.2.7.png)



## Part 10. Использование утилиты **fdisk**

- Запустили команду fdisk -l

![part_10.1](image/part_10.1.png)
  
    - название жесткого диска - VBOX HARDDISK
    - размер - 8GiB
    - количество секторов - 16777216
    - размер swap - ?



## Part 11. Использование утилиты **df** 

- Запустили команду df. В отчёте написали для корневого раздела (/):
![part_11.1](image/part_11.1.png)

    - размер раздела - 6352332 
    - размер занятого пространства - 2895392
    - размер свободного пространства - 3113084
    - процент использования - 49%
    - единица измерения в выводе - килобайт

- Запустили команду df -Th. В отчёте написали для корневого раздела (/):
![part_11.2](image/part_11.2.png)

    - размер раздела - 6.1G
    - размер занятого пространства - 2.8G
    - размер свободного пространства - 3.0G
    - процент использования - 49%
    - тип файловой системы для раздела - ext4
  
  

## Part 12. Использование утилиты **du**

- Запускаем команду du

- Выводим размер папок /home, /var, /var/log 

- Выводим размер всего содержимого в /var/log (каждого вложенного элемента, используя *)
![part_12.1](image/part_12.1.png)



## Part 13. Установка и использование утилиты **ncdu**

- Установить утилиту ncdu

- Выводим размер папок /home, /var, /var/log

![part_13.1](image/part_13.1.png)
  
![part_13.2](image/part_13.2.png)
  
![part_13.3](image/part_13.3.png)



## Part 14. Работа с системными журналами

- Время последней успешной авторизации, имя пользователя и метод входа в систему: **rubenluw, Jul 28 23:02:46, login** 
![part_14.1](image/part_14.1.png)

- Перезапустили службу SSHd 

- Соообщение о рестарте службы
![part_14.2](image/part_14.2.png)
  
  
  
## Part 15. Использование планировщика заданий **CRON**

##### Используя планировщик заданий, запустим команду uptime через каждые 2 минуты.

- Нашли в системных журналах строчки о выполнении
![part_15.1](image/part_15.1.png)
  
- Вывели на экран список текущих заданий для CRON
![part_15.2](image/part_15.2.png)
  
- Удалили все задания из планировщика заданий
![part_15.3](image/part_15.3.png) 