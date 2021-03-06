# Введение в **Docker**

---
@snap[north span-90 text-center]
### Что такое **Docker**?
@snapend

@snap[south span-80]
![IMAGE](assets/img/zeppelin-small.png)
@snapend


---

@snap[north-west span-70 text-center]
#### Немного определений о **Docker**
@snapend
@snap[west span-90]
@ul[list-spaced-bullets text-07]
- **Docker** — программное обеспечение с открытым исходным кодом, применяемое для разработки, тестирования, доставки и запуска веб-приложений в средах с поддержкой контейнеризации. Он нужен для более эффективного использование системы и ресурсов, быстрого развертывания готовых программных продуктов, а также для их масштабирования и переноса в другие среды с гарантированным сохранением стабильной работы.
- Изначально Docker использовал LinuX Containers(**LXC**)
- Сейчас Docker использует runC(**libcontainer**)
@ulend
@snapend


---

@snap[north-west span-50 text-center]
#### Где работает **Docker**?
@snapend

@snap[south span-100]
![IMAGE](assets/img/w-docker-work.png)
@snapend

---

@snap[north-west span-50 text-center]
#### **VM** vs **Container**
@snapend

@snap[west span-60]
@ul[list-spaced-bullets text-05]
- **VM** == приложение (связанные библиотеки. исходный код), OS, CPU, RAM, HDD.
- **Container** == изолированное пространство, приложение (связанные библиотеки. исходный код)
- **VM** выделяется ресурс, который может простаивать
- **Container** использует ядро основной ОС и read only копию bin/libs
- **Container** весит **гораздо меньше VM**
- **VM** поднимается дольше, чем **container**
- **VM изолирован,** а container нет
@ulend
@snapend

@snap[east span-40]
![IMAGE](assets/img/vm-vs-container.png)
@snapend

@snap[south span-100 bg-black fragment]
@img[shadow](assets/img/vm-vs-container.png)
@snapend


---

@snap[north-west span-70 text-center]
#### Что такое ** Docker Engine**?
@snapend

@snap[west span-100]
@ul[list-spaced-bullets text-09]
- **Docker Engine** («Движок» Docker) — ядро механизма Docker. «Движок» отвечает за функционирование и обеспечение связи между основными Docker-объектами (реестром, образами и контейнерами)
@ulend
@snapend

---

@snap[north-west span-70 text-center]
#### Компоненты **Docker Engine** 
@snapend

@snap[west span-55]
@ul[list-spaced-bullets text-06]
- **Сервер** - выполняет инициализацию демона (фоновой программы), который применяется для управления и модификации контейнеров, образов и томов.
- **REST API** — механизм, отвечающий за организацию взаимодействия Докер-клиента и Докер-демона.
- **Клиент** — позволяет пользователю взаимодействовать с сервером при помощи команд, набираемых в интерфейсе (CLI).
@ulend
@snapend

@snap[east span-45]
![IMAGE](assets/img/docker-engine.png)
@snapend

---

@snap[north-west span-50 text-center]
#### Преимущества и особенности
@snapend

@snap[west span-55]
@ul[list-spaced-bullets text-07]
- Изолированность
- Портативность
- Быстрая доставка и развёртывание приложений
- **open-source**
- cross-platform
- Написан на Go
@ulend
@snapend

@snap[east span-35]
![IMAGE](assets/img/isolation-container.png)
@snapend

---

@snap[north-west span-50 text-center]
#### Области применения
@snapend

@snap[west span-55]
@ul[list-spaced-bullets text-07]
- Контейнеризация Web-приложений
- Построение отказоустойчивых систем
- Быстрая доставка и развёртывание приложений (**Zero downtime**)

@ulend
@snapend

---

@snap[north span-90 text-center]
### **Тренды**
@snapend

@snap[span-100]
![IMAGE](assets/img/vmware-vs-docker-trends.png)
@snapend

---


@snap[north span-90 text-center]
### Компоненты **Docker**
@snapend

@snap[south span-90]
![IMAGE](assets/img/docker-architecture.png)
@snapend

---

@snap[north-west span-100 text-center]
#### Docker **Image**
@snapend

@snap[west span-55]
@ul[list-spaced-bullets text-06]
- **Union File System** - можно рассматривать как результат слияния файловых систем слоев. Объединенная файловая система умеет обрабатывать конфликты, когда в разных слоях присутствуют файлы и директории с одинаковыми именами. Каждый следующий слой добавляет или удаляет какие то файлы из предыдущих слоев. В данном контексте «удаляет» можно рассматривать как «затеняет», т.е. файл в нижележащем слое остается, но его не будет видно в объединенной файловой системе.
- Можно провести аналогию с Git: слои - это как отдельные коммиты, а образ в целом - результат выполнения операции **squash**.
@ulend
@snapend

@snap[east span-45]
![IMAGE](assets/img/docker-layers.png)
@snapend

@snap[south span-100 bg-black fragment]
@img[shadow](assets/img/union-layers.png)
@snapend

---


@snap[north span-100]
### Команды Docker
@snapend

```docker zoom-18
CREATE TABLE "topic" (
    "id" serial NOT NULL PRIMARY KEY,
    "forum_id" integer NOT NULL,
    "subject" varchar(255) NOT NULL
);
ALTER TABLE "topic"
ADD CONSTRAINT forum_id
FOREIGN KEY ("forum_id")
REFERENCES "forum" ("id");
```

@snap[south span-100 text-gray text-08]
@[1-5](You can step-and-ZOOM into fenced-code blocks, source files, and Github GIST.)
@[6,7, zoom-13](Using GitPitch live code presenting with optional annotations.)
@[8-9, zoom-12](This means no more switching between your slide deck and IDE on stage.)
@snapend

---?image=assets/img/code.jpg&opacity=60&position=left&size=45% 100%

@snap[east span-50 text-center]
## Now It's **Your** Turn
@snapend

@snap[south-east span-50 text-center text-06]
[Download GitPitch Desktop @fa[external-link]](https://gitpitch.com/docs/getting-started/tutorial/)
@snapend

@title[Customize Slide Layout]

@snap[west span-55]
## Customize the Layout
@snapend
