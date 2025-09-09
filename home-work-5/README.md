#### Что нужно ддля запуска:

- Minikube (также включить ingress addon)
- Helm
- Newman (тестирование запущенного приложения)

#### Запускаем:

(1) Для начала установим Mongodb В наш кубер с помощью стороннего хелм чарта:

```bash
helm upgrade mongo -f mongodb-values.yaml --install oci://registry-1.docker.io/bitnamicharts/mongodb
```

(2) Затем устанавливаем наш хелм чарт , который имеет в себе инструкции по запуску нашего приложения:

```bash
helm install users-app ./helm-chart
```

(3) Не забываем включить тунель в отдельном окне терминала и настроить hosts:

```bash
minikube tunnel
```

(4) Тперь можем пройти на созданное нами приложение по ссылке:

[http://arch.homework/api](http://arch.homework/api)

(5) Ну и наконц, Newman поможет протестировать коллекцию Postman, которая ссылается на наше локальное приложение:

```bash
newman run otus-homework-4.postman_collection.json
```

<a name="my-scrinshot">у меня такие логи</a>:    

![NewmanScreenshot.png](./NewmanScreenshot.png?raw=true)

----

