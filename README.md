# Домашнее задание к занятию «Как работает сеть в K8s»


## Задание 1. Создать сетевую политику или несколько политик для обеспечения доступа
- Создать deployment'ы приложений frontend, backend и cache и соответсвующие сервисы.
 - В качестве образа использовать network-multitool.

Манифесты [deployment](https://github.com/vladmgb/kuber-3.3/blob/main/deployments.yaml)

- Разместить поды в namespace App.

<img width="430" height="127" alt="image" src="https://github.com/user-attachments/assets/6b11a4d8-c925-476c-b666-727799f9830a" />

<img width="483" height="217" alt="image" src="https://github.com/user-attachments/assets/366a2eab-91db-4796-94fd-d508b0e0fe8d" />

Проверяем доступ без политик. 

<img width="1200" height="585" alt="image" src="https://github.com/user-attachments/assets/471434d5-499b-4086-ae8c-c4e0f12e05cd" />


<img width="1201" height="593" alt="image" src="https://github.com/user-attachments/assets/d2421641-a81a-4deb-84bf-5a2d07f92447" />


<img width="1204" height="593" alt="image" src="https://github.com/user-attachments/assets/368727bd-a6a3-477b-876f-c8521ff21534" />


<img width="1205" height="587" alt="image" src="https://github.com/user-attachments/assets/e5460c17-41ff-4eab-9233-4099c57adaff" />


<img width="1206" height="594" alt="image" src="https://github.com/user-attachments/assets/8f07b586-9263-497f-b2a9-940b1491bb63" />

Убеждаемся, что трафик разрешён.

- Создать политики, чтобы обеспечить доступ frontend -> backend -> cache. Другие виды подключений должны быть запрещены.

  Манифесты [политик](https://github.com/vladmgb/kuber-3.3/blob/main/networkpolicy.yaml)

<img width="485" height="59" alt="image" src="https://github.com/user-attachments/assets/f4519a19-0a63-430f-a250-46b797820eb4" />   

<img width="406" height="92" alt="image" src="https://github.com/user-attachments/assets/16396053-cb91-4da2-a496-7c1c8c6fb1c8" />

Проверяем.

Требуемый доступ есть.

<img width="1197" height="572" alt="image" src="https://github.com/user-attachments/assets/3c977f17-acd2-4920-b67b-1d5d2f36aafc" />  

<img width="1204" height="591" alt="image" src="https://github.com/user-attachments/assets/9e2f6c0f-4907-420d-89bf-3a249944dcca" />

Убеждаемся, что остальной трафик ограничен.

<img width="535" height="131" alt="image" src="https://github.com/user-attachments/assets/98b78e04-7514-47d2-9108-477fdddecc52" /> 

Для примера

<img width="636" height="306" alt="image" src="https://github.com/user-attachments/assets/d3cffac4-da16-4bd7-9b92-06dc417006e3" />
