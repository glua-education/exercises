## 📋 Описание

![1](https://i.imgur.com/m0WDSQp.png)

• Если вы выключаете стандартный худ в DarkRP, у вас будет всплывать варнинг "Unhandled usermessage _Notify".

Обычный DarkRP довольно старый режим и тянет за собой кучу легаси, в том числе и старую библиотеку usermessage.

Авторы DarkRP сделали реализацию показа Notification таким тупым способом и она вшита в худ. Если же худ отключить (мы это делаем часто), начинают идти варнинги, мол такого usermessage хука нет и нельзя вызвать Notification. 

Исправить это довольно легко. Узнать в интернете, как реализовали эту дичь и просто создать файл с исправлением у себя в проекте (он будет на client), написать фикс и всё.

--- 

## 🎯 Цель

> Устранить предупреждение в консоли путём замены хука для usermessage с названием "_Notify"

--- 

## 📂 Подсказки

<details>
<summary> <i>Показать</i> </summary>

* GAMEMODE:AddNotify( arg1, arg2, arg3 )
* msg:ReadString()
* msg:ReadShort()
* msg:ReadLong()
* usermessage.Hook("_Notify", function() -- сюда end)
</details>