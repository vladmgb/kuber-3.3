# Домашнее задание к занятию «Как работает сеть в K8s»


## Задание 1. Создать сетевую политику или несколько политик для обеспечения доступа
Создать deployment'ы приложений frontend, backend и cache и соответсвующие сервисы.

Манифесты deployment

<img width="483" height="217" alt="image" src="https://github.com/user-attachments/assets/366a2eab-91db-4796-94fd-d508b0e0fe8d" />


В качестве образа использовать network-multitool.
Разместить поды в namespace App.

<img width="430" height="127" alt="image" src="https://github.com/user-attachments/assets/6b11a4d8-c925-476c-b666-727799f9830a" />


Создать политики, чтобы обеспечить доступ frontend -> backend -> cache. Другие виды подключений должны быть запрещены.
Продемонстрировать, что трафик разрешён и запрещён.
