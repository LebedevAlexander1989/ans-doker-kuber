# ans-doker-kuber
Обучение по ansible, docker и kuber

## Docker
### Написание докерфайла
```
FROM node as build // добавление ноды
WORKDIR /app // создание рабочей директории
COPY . /app // копирование всего проекта в рабочую директорию
RUN npm install // запуск добавленной ноды
EXPOSE 4200 // прокидывание порта
ENTRYPOINT ["npm", "start"] // использование поинтов для запуска приложения
```

### Создание докер образа
```
docker build . --tag=nodeapp:latest
```

### Запуск докер образа
```
docker run -p 4200:4200 nodeapp:latest
```

