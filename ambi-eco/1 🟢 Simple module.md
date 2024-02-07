## 📋 Описание

• Познакомимся с Ambi Eco и научимся создавать и подключать модули

![dsa](https://i.imgur.com/CnxYMBr.png)

1. Нам нужно скачать [Ambi Eco](https://github.com/Titanovsky/ambi-eco), вытащить оттуда папку ambi и поставить в addons. Не забудьте скачать [контент (шрифты и звуки)](https://steamcommunity.com/sharedfiles/filedetails/?id=2890017076)

![adsds](https://i.imgur.com/pxwxRZL.png)

2. Создайте папку с форматом (латинские символы, нижний регистр, заместо пробелов - тире). Папка будет в ambi/lua/modules, именно там модули (libs - папка с библиотеками, туда только смотреть; autorun - не трогать; ambi_config.lua там будем подключать). Допустим создадим модуль (папку) <b>"greeting"</b>

![dsasd](https://i.imgur.com/SS5szEl.png)

3. Зайдите в ambi/lua/ambi_config.lua, именно там мы будем подключать или отключать (комментировать строчки) модули. Подключим наш модуль, первый аргумент - название папки, второй (необязательный) описание. Кстати, там же можете закомментировать ненужные вам модули, необязательно удалять их папки.

![dsasd](https://i.imgur.com/aMS1mkh.png)

4. Структура модулей обычно такая

* В первой папке всегда cfg файл (shared) и потом подпапки (core, например)
* файлы всегда с префиксом: sv, sh, cl - понятно; cfg, wep, ent, npc - shared
* загрузка файлов всегда начинается с корневой папки (сначала папка, потом подпапки). Файлы и папки по алфавитному порядку

![dsasd](https://i.imgur.com/GHU3Bjd.png)

5. Зайдём в конфиг уже нашего модуля и пропишем
```lua
Ambi.General.CreateModule( 'Greeting' ) -- мы создаём модуль (Ambi.Greeting) и конфиг (Ambi.Greeting.Config)

-- --------------------------------------------------------------------------------------------------------------------------------------------
Ambi.Greeting.Config.text = "~WHITE~ Привет, ~GREEN~ %s ~WHITE~ , как дела?" --! обязательно должен быть %s
```

6. Потом зайдём в папку core, создадим файл sv_greeting.lua (название любое, главное чтобы префикс был sv) и
```lua 
hook.Add( 'PlayerInitialSpawn', 'Ambi.Greeting.Say', function( ePly )
    local nick = ePly:Nick()
    ePly:ChatSend( string.format( Ambi.Greeting.Config.text ), nick )
end )
```

--- 

## 🎯 Цель

> Научитесь создавать и подключать модули в Ambi Eco
