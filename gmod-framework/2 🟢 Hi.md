## 📋 Описание

![dsa](https://image.winudf.com/v2/image/Z2F5c29oYmV0Lm9kYWxhcmkudHJfaWNvbl8xNTM2MjcyOTYyXzA0Nw/icon.png?w=160&fakeurl=1)

Вам предстоит разработать скрипт для Garry's Mod, который создаст уникальное приветственное сообщение для каждого игрока при их первом подключении к серверу.

---

## 🎯 Цель

Реализовать функционал, который будет генерировать индивидуальное приветственное сообщение для каждого игрока, включающее в себя их никнейм и случайное приветственное слово из списка.

---

## 📂 Подсказки

<details>
<summary> <i>Показать</i> </summary>

* table.Random
* hook `PlayerInitialSpawn`
* `for _, ply in ipairs( player.GetAll() ) do`
* ply:ChatPrint()

</details>