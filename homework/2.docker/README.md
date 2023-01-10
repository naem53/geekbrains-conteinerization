# Домашнее задание к уроку 2 - Docker

Напишите Dockerfile к любому приложению из директорий golang или python на ваш выбор (можно к обоим).

Образ должен собираться из официального базового образа для выбранного языка. На этапе сборки должны устанавливаться все необходимые зависимости, а так же присутствовать команда для запуска приложения.

Старайтесь следовать рекомендациям (Best Practices) из лекции при написании Dockerfile.

При запуске контейнера из образа с указанием проксирования порта (флаг -p или -P если указан EXPOSE) при обращении
на localhost:port должно быть доступно приложение в контейнере (оно отвечает Hello, World!).

Сохраните получившийся Dockerfile в любом публичном Git репозитории, например GitHub, и пришлите ссылку на репозиторий.


build & run python:
docker build -f dockerfile.python -t app:v0.1-python .
docker run -itd --name app -p 8080:8080 app:v0.1-python

build & run golang:
docker build -f dockerfile.golang -t app:v0.1-golang .
docker run -itd --name app -p 8080:8080 app:v0.1-golang