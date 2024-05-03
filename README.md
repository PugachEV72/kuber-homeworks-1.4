# Домашнее задание к занятию `«Сетевое взаимодействие в K8S. Часть 1»` - Пугач Евгений.


---

## `Задание 1. Создать Deployment и обеспечить доступ к контейнерам приложения по разным портам из другого Pod внутри кластера`

1. Создать Deployment приложения, состоящего из двух контейнеров (nginx и multitool),  
   с количеством реплик 3 шт.
2. Создать Service, который обеспечит доступ внутри кластера до контейнеров приложения из п.1  
   по порту 9001 — nginx 80, по 9002 — multitool 8080.
3. Создать отдельный Pod с приложением multitool и убедиться с помощью curl, что из пода есть  
   доступ до приложения из п.1 по разным портам в разные контейнеры.
4. Продемонстрировать доступ с помощью curl по доменному имени сервиса.
5. Предоставить манифесты Deployment и Service в решении, а также скриншоты или вывод команды п.4.

### Ответ:

![Скриншот 1](https://github.com/PugachEV72/Images/blob/master/2024-05-03_20-14-40.png)

![Скриншот 2](https://github.com/PugachEV72/Images/blob/master/2024-05-03_20-18-31.png)

![Скриншот 3](https://github.com/PugachEV72/Images/blob/master/2024-05-03_20-19-28.png)

![Скриншот 4](https://github.com/PugachEV72/Images/blob/master/2024-05-03_20-20-40.png)

[Ссылка на nginx-multi-deployment.yaml](https://github.com/PugachEV72/kuber-homeworks-1.4/blob/main/nginx-multi-deployment.yaml)

[Ссылка на nginx-multi-service.yaml](https://github.com/PugachEV72/kuber-homeworks-1.4/blob/main/nginx-multi-service.yaml)

---

## `Задание 2. Создать Service и обеспечить доступ к приложениям снаружи кластера`

1. Создать отдельный Service приложения из Задания 1 с возможностью доступа снаружи кластера к nginx,  
   используя тип NodePort.
2. Продемонстрировать доступ с помощью браузера или curl с локального компьютера.
3. Предоставить манифест и Service в решении, а также скриншоты или вывод команды п.2.

### Ответ:

![Скриншот 5](https://github.com/PugachEV72/Images/blob/master/2024-05-03_20-34-54.png)

![Скриншот 6](https://github.com/PugachEV72/Images/blob/master/2024-05-03_20-36-39.png)

![Скриншот 7](https://github.com/PugachEV72/Images/blob/master/2024-05-03_20-35-16.png)

[Ссылка на nginx-nodeport-service.yaml](https://github.com/PugachEV72/kuber-homeworks-1.4/blob/main/nginx-nodeport-service.yaml)

---
