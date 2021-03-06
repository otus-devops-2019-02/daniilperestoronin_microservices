# daniilperestoronin_microservices
daniilperestoronin microservices repository

# ДЗ № 24

Добавлены:
- prometheus
- grafana
- alertmanager
- различные экспортеры для метрик prometheus 

# ДЗ № 23

- Добавлен Helm
- Развернут Gitlab в Kubernetes
- Настроен CI/CD конвейера в Kubernetes

# ДЗ № 22

Добавлены:
- Ingress Controller
- Ingress
- Secret
- TLS
- LoadBalancer Service
- Network Policies
- PersistentVolumes
- PersistentVolumeClaims

# ДЗ № 21

- Развернуто локальное окружение для работы с Kubernetes
- Развернут Kubernetes в GKE
- Запущен reddit в Kubernetes

# ДЗ № 20

Реализовано: 
- Добавлены манифест файлы для запуска приложения
- Пройден тьюториал (https://github.com/kelseyhightower/kubernetes-the-hard-way)

для деплоя:
```bash
kubectl apply -f mongo-deployment.yml
kubectl apply -f mongo-service.yaml
kubectl apply -f post-deployment.yml
kubectl apply -f post-service.yaml
kubectl apply -f comment-deployment.yml
kubectl apply -f comment-service.yaml
kubectl apply -f ui-deployment.yml
kubectl apply -f ui-service.yaml
```

# ДЗ № 19

Реализовано: 
- Сбор неструктурированных логов
- Визуализация логов
- Сбор структурированных логов
- Распределенная трасировка

### Environment settings

```bash
$ docker-machine create --driver google \
    --google-machine-image https://www.googleapis.com/compute/v1/projects/ubuntu-os-cloud/global/images/family/ubuntu-1604-lts \
    --google-machine-type n1-standard-1 \
    --google-open-port 5601/tcp \
    --google-open-port 9292/tcp \
    --google-open-port 9411/tcp \
    logging

# configure local env
$ eval $(docker-machine env logging)

# узнаем IP адрес
$ docker-machine ip logging
```

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
