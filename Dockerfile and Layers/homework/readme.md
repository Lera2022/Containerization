# Задача
Необходимо создать Dockerfile, основанный на любом образе (вы в праве выбрать самостоятельно).
В него необходимо поместить приложение, написанное на любом известном вам языке программирования (Python, Java, C, С#, C++).
При запуске контейнера должно запускаться самостоятельно написанное приложение.

# Список команд
# Скрипт на Python, создаём файл test.py

# Прописываем в Dockerfile
FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y

RUN apt-get install python3 -y

RUN apt-get install python3-pip -y

# Команды для терминала
1) Перейти в папку со скриптом, выполнив команду cd <имя папки>.
2) Выполнить команду:
docker build -t imagename .
3) После построения образа запускаем его командой:
docker run -v /home/ <имя юзера>/ <имя папки>/:/dir imagename python3 dir<em>/</em>test.py
