# daniilperestoronin_microservices
daniilperestoronin microservices repository

# ДЗ № 18

Реализовано: 
- Мониторинг Docker контейнеров
- Визуализация метрик
- Сбор метрик работы приложения и бизнес метрик
- Настройка и проверка алертинга

### Environment settings
```bash
$ export GOOGLE_PROJECT=_ваш-проект_

# Создать докер хост
docker-machine create --driver google \
    --google-machine-image https://www.googleapis.com/compute/v1/projects/ubuntu-os-cloud/global/images/family/ubuntu-1604-lts \
    --google-machine-type n1-standard-1 \
    --google-zone europe-west1-b \
    docker-host

# Настроить докер клиент на удаленный докер демон
eval $(docker-machine env docker-host)

# Переключение на локальный докер
eval $(docker-machine env --unset)

$ docker-machine ip docker-host

$ docker-machine rm docker-host
```

### DockerHub
https://cloud.docker.com/u/danniilperestoronin/

# ДЗ № 17

- Prometheus: запуск, конфигурация, знакомство с Web UI
- Мониторинг состояния микросервисов
- Сбор метрик хоста с использованием экспортера

https://cloud.docker.com/u/danniilperestoronin/

# ДЗ № 16

- Подготовлена инсталляция Gitlab CI
- Подготовлен репозиторий с кодом приложения
- Описаны для приложения этапы пайплайна
- Определены окружения

# ДЗ № 15

- Запущены контейнеры в различных типах сетей
- Реализован docker-compose.yml

Правило наименования по умолчанию:
```
The default naming scheme for containers created by Compose in this version has
changed from <project>_<service>_<index> to <project>_<service>_<index>_<slug>,
where <slug> is a randomly-generated hexadecimal string.
```
Для определения имени необходимо указать ```container_name```, например:

```
  container:
    container_name: my-container
```


# ДЗ № 14
- Приложение разбито на несколько микросервисов
- Для каждого микросервиса добавлены Dockerfile
- Оптимизорован Dockerfile для ui
- Создан volume для MongoDB

## В процессе сделано:
 - Создан docker host
 - Создан свой образа
 - Работа с Docker Hub

# ДЗ № 13

## В процессе сделано:
 - Создан docker host
 - Создан свой образа
 - Работа с Docker Hub

# ДЗ № 12

## В процессе сделано:
 - Настроена интергация с Travis, Slack
 - Сохранен выаод команды ```docker images``` в файл docker-1.log
