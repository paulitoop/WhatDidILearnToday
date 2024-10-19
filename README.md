# WhatDidILearnToday
Буду писать о том, что нового сегодня узнал. Помогу себе структурировать информацию.

## 18.10.2024
1. Узнал что я могу 9 часов без перерыва сидеть над задачей (сейчас 7 утра доброе утро)
2. Как работает хранилище артефактов Nexus sonatype
3. Как работает мульти сборка Dockerfile
4. Как раскладывать команду запуска докер контейнера в docker compose
5. Что можно примонтировать файл в Dev/null и у него будет буква 'с' при ls
6. Узнал что нельзя подписать файл открытым ключом и обойти систему
7. Сделал удобную оптимизацию в Make file докера
8. Узнал как работает Helm 
9. Отловил несколько интересных моментов с trace, когда команда долго не отрабатывала 
10. Нахожусь на финишной прямой с boinc, осталось только сделать нормальным private key

## 17.10.2024
1. Для docker compose можно написать 'Makefile' и настроить в нем алиасы и цепочки команд для удобства управления системой контейнеров
2. Ознакомился с некоторыми программами для создания цифровой подписи файлов
3. Узнал что чтобы скопировать питоновское приложение на линуксе для винды, нужно качать специальные пакеты, которые симулируют виндовское окружение, и через них запускать питон


## 16.10.2024
1. Изучал лучшие практики работы с k8s и Gitlab
2. При деплое новой версии приложения. нужно учитывать, что k8s отключит один из подов, и все запросы пойдут на другие. Нужно уметь правильно рассчитать количество подов, что бы это было не слишком долго, но в то же время что бы остальные поды не падали от нагрузки
3. При деплое важно учитывать, что приложения, зависящие от БД не стартанутся, и k8s может отправлять из в долгое ожидание. поэтому важно даже не пытаться из стартовать, пока база не запустилась
4. metasploit revershell использует shell а не cmd (вау)
5. Вообще Ci/CD с использование k8s в колабе с Gitlab и Helm - это очень круто и покрывает почти все случаи, которые нам необходимы.


## 15.10.2024
1. Узнал что у highload есть два друга - cache и cash
2. Обращения к БД лучше проводить транзакциями (снижается нагрузка на I/O диска), не забывать об индексации, быть конкретным в запросах, не использовать *
3. У apache есть воркеры, которые очень любят тратить свои ресурсы и зависать, если их не контролировать
4. Если перед apache не будет обратного прокси, то медленные клиенты могут занять все воркеры и положить сервак
5. Нужно следить за тем, что бы TCP соединение оставалось активным, если это возможно. не нужно каждый раз заново его открывать, лишние пакеты, захламленность канала
6. Наконец то понял отличия join-ов в SQL



## 14.10.2024
1. Узнал что можно синхронизировать методы на двух нодах с помощью **'Hazelcast'**
2. Дочитал про архитектуру систем, понял что главное - делать по **SOLID**
3. Узнал как работать с сетями в **Docker-compose**
4. Узнал как обновляться с неподписанного репозитория
5. Понял что докер 1.10.3 - это зло, как и BOINC 
6. Если конкретнее говорить про архитектуру, то код должен быть такой. что бы его можно было легко дописывать, тестировать, понимать, масштабировать. это нас приводит модулям с минимальной связностью, каждый из которых выполняет свою определённую функцию

## 13.10.2024
1. Узнал как делать анализ несанкционированного доступа к файлам и папкам с помощью **Ревизор**
2. Узнал что для поиска конфиденциальной информации можно сканировать диск на наличие сигнатур
3. Узнал как делать вредоносное ПО с эксплоитами с помощью **msfvenom**
4. Успешно проэксплуатировал **reverse_tcp** на Windows 7
5. Узнал как работает платежная система МИР под капотом (Highload)

## 12.10.2024
1. Узнал в чем отличие у G поколений мобильного интернета
2. Начал изучать **GitLab CI/CD**
3. Узнал как заходить в контейнеры **Docker Compose**
4. Узнал что перед поднятием **Docker Compose** можно сделать кастомный **build** контейнеров по Dockerfile
5. Узнал как работает **BOINC**, мучался с созданием задач на сервере

## 11.10.2024
1. Узнал что такое **трейсы** и как они работают в связке с **ClickHouse** и **OpenTelemetry**
2. Узнал много нового про **микросервисную архитектуру** из доклада HighLoad
3. Изучил **патерны отказоусточивой архитектуры** на примере ЯндексВоды (HighLoad)
4. Начал углубляться в **архитектурные принципы построения систем** (не дочитал)
5. Понял что файлы **.ova** нужно не добавлять в VitrualBox а импортировать
6. Задумался над построением собственного мини кластера для тренироваки навыков мониторинга и тестирования
7. Узнал что `chr(3486)` в `Python` - это амогус
