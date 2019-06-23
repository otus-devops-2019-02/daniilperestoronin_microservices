# daniilperestoronin_microservices
daniilperestoronin microservices repository

# ДЗ № 16

- Prometheus: запуск, конфигурация, знакомство с Web UI
- Мониторинг состояния микросервисов
- Сбор метрик хоста с использованием экспортера

https://cloud.docker.com/u/danniilperestoronin/repository/docker/danniilperestoronin/prometheus

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
