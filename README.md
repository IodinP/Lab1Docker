# Lab1Docker
## 1 шаг

<img width="605" height="268" alt="image" src="https://github.com/user-attachments/assets/4ecc72f9-d9e3-42bf-a15d-f5401ddd210d" />

## 2 шаг
Создан Dockerfile — инструкция для сборки образа. В нем мы:
Используем базовый образ python:3.9-slim.
Устанавливаем рабочую директорию /app.
Копируем файлы проекта и устанавливаем зависимости через pip.
Указываем порт 1234 (EXPOSE) и команду запуска приложения.
<img width="560" height="327" alt="image" src="https://github.com/user-attachments/assets/fb2cb3de-7931-4c7a-86f2-0e72d5c5d974" />

## 3 шаг
Сборка Docker-образа из текущей директории с тегом my-flask-app
Команда: docker build -t my-flask-app
<img width="897" height="439" alt="image" src="https://github.com/user-attachments/assets/2e61e104-3a84-4954-b0be-f4be81cf28b0" />

## 4 шаг
Запущен контейнер из созданного образа в фоновом режиме с пробросом портов (хост 1234)
<img width="655" height="84" alt="image" src="https://github.com/user-attachments/assets/08ac509d-19a2-424b-a630-7a13c16b9988" />
<img width="1130" height="444" alt="image" src="https://github.com/user-attachments/assets/8394fb3f-4e5c-4aa8-bbdd-071bbf6a3ef9" />
Для дальнейшей работы останавливаем 

<img width="436" height="73" alt="image" src="https://github.com/user-attachments/assets/93ef4046-526a-4ec3-a7ef-ca48b52104de" />

## 5 шаг
Для автоматизации запуска приложения вместе с базой данных PostgreSQL создан файл docker-compose.yml. В нем описаны два сервиса:
web: наше приложение (собирается из Dockerfile)
db: база данных PostgreSQL (из официального образа)
<img width="645" height="540" alt="image" src="https://github.com/user-attachments/assets/db013894-94c7-42f8-86b6-19864ba348d2" />
Стек сервисов запущен одной командой: docker-compose up -d.
<img width="891" height="622" alt="image" src="https://github.com/user-attachments/assets/ad55bc2b-feab-49a2-a188-a0347447cd11" />
И с помощью команды **docker ps** проверяем работу
<img width="937" height="318" alt="image" src="https://github.com/user-attachments/assets/e171289a-7f83-4a86-a06d-fbd4d5d1f3d5" />
Мы видим, что сайт работает
<img width="537" height="274" alt="image" src="https://github.com/user-attachments/assets/e28c2c1b-024d-43f1-ade5-b0d7d937bb35" />






