# 🔊 EchoChamber (v1.0)

**EchoChamber** is a challenging esoteric programming language based on acoustics and sound decay. Supports **Extended ASCII (0-255)** and user input.

## 🌌 Concept
The program runs in a space of 300 "rooms".
- Every **movement** or **pause** is a **time tick**.
- On every tick (`.`, `(`, `)`), the volume in ALL rooms decays by **1 unit**.
- Commands `A`, `s`, `a`, `S`, `,` and `@` are instantaneous and do **not** cause decay.
- If the volume drops to **0**, the data is lost (silence).

## 🛠 Syntax
- `A` (**Scream**) — Sets volume in the current room to **255** (max).
- `s` (**Whisper**) — Decreases volume by **10**.
- `a` (**Add**) — Increases volume by **10** (max 255).
- `S` (**Silence**) — Instantly sets volume in the room to **0**.
- `,` (**Input**) — Reads one character from the input buffer and sets volume to its ASCII code.
- `.` (**Pause**) — Does nothing but spends a tick (volume drops by 1). 
- `@` (**Listen**) — Outputs the character (Extended ASCII) of the current volume.
- `(` / `)` — Move the pointer. Each move spends a tick (volume drops by 1).
- `[` ... `]` — **Mirror Loop**. Repeats as many times as the volume level was when entering.
- `$` — Comment (ignored until the end of the line).

## 📝 Examples / Примеры

### Printing 'H' (ASCII 72) / Печать буквы 'H' (ASCII 72)
```echo
$ Option 1: Fast decay with whispers (255 - 180 - 3 points)
$ Вариант 1: Быстрое затухание шепотом
A s s s s s s s s s s s s s s s s s ... @ 

$ Option 2: Echo Program (reads from input and shouts back)
$ Вариант 2: Программа-эхо (читает ввод и выводит его)
, @
```

________________________________________________________________

# 🔊 EchoChamber (v1.0)

**EchoChamber** — это сложный эзотерический язык программирования, основанный на концепции акустики и затухания звука. Поддерживает **Extended ASCII (0-255)** и пользовательский ввод.

## 🌌 Концепция
- Каждое **перемещение** или **пауза** — это **такт времени**.
- На каждом такте (`.`, `(`, `)`) звук во всех комнатах затухает на **1 единицу**.
- Команды `A`, `s`, `a`, `S`, `,` и `@` выполняются мгновенно и **не вызывают** затухания.
- Диапазон громкости **0-255** (Extended ASCII).

## 🛠 Синтаксис
- `A` (**Крик**) — Устанавливает громкость в текущей комнате на **255**.
- `s` (**Шепот**) — Снижает громкость на **10**.
- `a` (**Усиление**) — Увеличивает громкость на **10**.
- `S` (**Тишина**) — Обнуляет громкость в текущей комнате.
- `,` (**Ввод**) — Считывает один символ из ввода и записывает его код в громкость комнаты.
- `.` (**Пауза**) — Тратит такт времени (громкость падает на 1).
- `@` (**Слушать**) — Выводит символ текущей громкости.
- `(` / `)` — Переход между комнатами. Тратит такт (-1 к громкости).
- `$` — Комментарий.
