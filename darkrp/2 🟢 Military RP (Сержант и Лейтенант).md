## 📋 Описание

![sad](https://steamuserimages-a.akamaihd.net/ugc/223319164373724644/158292A5D7C8DECFDF5634BE770BF197DDA616C2/?imw=5000&imh=5000&ima=fit&impolicy=Letterbox&imcolor=%23000000&letterbox=false)
• Вы начинающий разработчик Military RP проекта, и вы захотели создать две работы: Сержант и Лейтенант. После того, как вы поставили режим ДаркРП, вам осталось лишь прописать эти две работы по аналогии:
```lua
TEAM_SCP = DarkRP.createJob("Guard", {
    color = Color(255, 255, 255, 255),
    model = {
        "models/player/Group03/Female_01.mdl",
        "models/player/Group03/Female_02.mdl"
    },
    description = [[Tu es un poisson.]],
    weapons = {"weapon_fists","tfa_famas","tfa_glock","stunstick"},
    command = "example",
    max = 1, -- at most 70% of the players can have this job. Set to a whole number to set an absolute limit.
    salary = 99999999,
    admin = 0,
    vote = false,
    candemote = true,
    category = "Other"
})
```

И сделать для удобства две функции для Player, которые проверяют являешься ли ты Сержантом и Лейтенантом. Так как Player - мета таблица, чтобы её получить, необходимо прописать
```lua
local PLAYER = FindMetaTable('Player') -- отдаёт таблицу
```

--- 

## 🎯 Цель

> Две работы: TEAM_SERGEANT, TEAM_LEIUTENANT
И две функции для игрока, которые проверяют соответствие на эти работы:
PLAYER:IsSergeant()
PLAYER:IsLeiutenant()

--- 

## 📚 Условия

1. Режим должен быть чистый DarkRP (или Новый DarkRP)

--- 

## 📂 Подсказки

<details>
<summary> <i>Показать</i> </summary>

* [Как создать работу](https://darkrp.miraheze.org/wiki/DarkRP:CustomJobFields)
* FindMetaTable( "Player" )
* self:Team() == TEAM_что-то
* Функции можно в одну строку и они обязательны должны что-то вернуть
</details>