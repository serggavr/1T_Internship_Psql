# Пошаговая инструкция по созданию fork репозитория Git

1. Откройте браузер и перейдите на страницу репозитория https://github.com/mazavlia/1T_Internship_Psql, от которого 
    будете делать ответвление (Fork) в свой репозиторий.
2. На странице репозитория найдите кнопку "Fork" ![fork.png](images%2Ffork.png) и нажмите на неё. Это создаст копию 
    репозитория на вашем GitHub-аккаунте.

Теперь у вас есть форк репозитория на GitHub. Следующие шаги позволят вам клонировать его на ваш локальный компьютер и работать с новыми парсерами:

3. Откройте командную строку или терминал на вашем компьютере.
4. На GitHub найдите URL вашего форкнутого репозитория. Вы можете найти его на странице вашего форка справа в верхнем углу.
5. В командной строке выполните следующую команду, заменив <forked_repository_url> на URL вашего форкнутого репозитория:

```git clone <forked_repository_url>```

Это склонирует ваш форкнутый репозиторий на ваш локальный компьютер.

6. Перейдите в директорию, созданную после клонирования репозитория, с помощью команды cd.
7. Создайте новую ветку, используя команду git branch с указанием имени новой ветки:

```git branch <branch_name>```

Замените <branch_name> на имя вашей новой ветки (например, zarplata_ru).

8. Перейдите на новую ветку с помощью команды git checkout:

```git checkout <branch_name>```

Замените <branch_name> на имя вашей новой ветки.

Теперь вы находитесь на созданной вами новой ветке с форка репозитория. 

9. ❗ Все изменения вносим только в папке /dev ❗ 

Перейдите в директорию dev с помощью команды в терминале: ```cd dev```
Здесь запустите: ```docker-compose up -d```.
В папке ```dev/airflow/``` находится файл [initial_dag.py](airflow%2Fdags%2Finitial_dag.py), в нем реализован class DatabaseManager по созданию таблицы, базовый class BaseJobParser и class VKJobParser, наследованный от BaseJobParser в качестве примера. 
Вы можете вносить необходимые изменения.

Подключение Airflow: ```http://localhost:10129```

Подключение DBeaver:

    Создать соединение -> PostgreSQL
```
    Host: localhost
    Schema: vacancy
    Login: admin
    Password: password
    Port: 10111
```

10. После внесения изменений выполните следующие команды, чтобы сохранить изменения и отправить их в ваш форкнутый репозиторий:
```
git add .
git commit -m "Описание ваших изменений"
git push --set-upstream origin <branch_name>
```

Ваши изменения отправлены в ваш форкнутый репозиторий. Теперь вы можете создать pull request (запрос на включение изменений в исходный репозиторий):

Перейдите на страницу вашего форкнутого репозитория на GitHub.
У вас появится кнопка ![pr.png](images%2Fpr.png), нажмите на нее.
Заполните все необходимые поля и описание, затем нажмите на кнопку "Create pull request" (или аналогичную).

Ваш pull request отправлен! 🔥  


