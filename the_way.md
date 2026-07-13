
## Windows (через winget)
Встроенный в Windows менеджер пакетов позволяет запустить официальный инсталлятор в "тихом" режиме, но чтобы гарантированно исключить pgAdmin, проще использовать установку через консольный менеджер Chocolatey (если он у вас есть) или стандартный winget со специальным ключом.
Вариант 1: Через winget (стандартный терминал Windows)

winget install PostgreSQL.PostgreSQL.16 --override "--mode unattended --install_runtimes 0"

Вариант 2: Через Chocolatey (если используется на ПК)

choco install postgresql16 --params "'" /Password:YourStrongPasswordHere "'" -y

(Замените YourStrongPasswordHere на ваш будущий пароль администратора базы данных).
------------------------------
## Как проверить, что всё работает?
После установки откройте новый терминал и введите команду проверки версии:

psql --version

Если в ответе написано psql (PostgreSQL) 16.x — движок готов к созданию таблиц фактов и справочников.


<img width="1477" height="541" alt="image" src="https://github.com/user-attachments/assets/96ea4457-1620-4de3-84f2-c224b2cf0d3b" />



postgres=# ALTER USER postgres PASSWORD 'Wec9i856';
