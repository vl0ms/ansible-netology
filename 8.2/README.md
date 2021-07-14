# Elasticsearch & Kibana installation playbook

## Before run playbook start docker container:
    `docker run -dit --name ubuntu-ek pycontribs/ubuntu:latest`

## Run playbook:
    `ansible-playbook -i inventory/prod.yml site.yml`

1. Установка JAVA

   Версию можно указать в `group_vars/all/vars.yml`.

   Дистрибутив JAVA необходимо предварительно скачать по [ссылке](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) и поместить tag.gz в каталог **files**

2. Установка Elasticsearch

   Версию можно указать в `group_vars/elasticsearch/vars.yml`.

3. Установка Kibana

   Версию можно указать в `group_vars/elasticsearch/vars.yml`.

Возможна установка отдельных компонентов с помощью тегов:

   `--tags java` - установка JAVA

   `--tags elastic` - установка Elasticsearch

   `--tags kibana` - установка Kibana
