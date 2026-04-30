# 🔊 EchoChamber (v1.1)

**EchoChamber** is a challenging esoteric programming language based on acoustics and sound decay. Now supports **Extended ASCII (0-255)**.

## 🌌 Concept
The program runs in a space of 300 "rooms".
- Every **movement** or **pause** is a **time tick**.
- On every tick (`.`, `(`, `)`), the volume in ALL rooms decays by **1 unit**.
- Commands `A`, `s`, `a`, `S` and `@` are instantaneous and do not cause decay.
- If the volume drops to **0**, the data is lost (silence).

## 🛠 Syntax
- `A` (**Scream**) — Sets volume in the current room to **255** (max).
- `s` (**Whisper**) — Decreases volume by **10**.
- `a` (**Add**) — Increases volume by **10** (capped at 255).
- `S` (**Silence**) — Instantly sets volume in the room to **0**.
- `.` (**Pause**) — Does nothing but spends a tick (volume drops by 1). 
- `@` (**Listen**) — Outputs the character (Extended ASCII) of the current volume.
- `(` / `)` — Move the pointer. Each move spends a tick (volume drops by 1).
- `[` ... `]` — **Mirror Loop**. Repeats as many times as the volume level was when entering.

## 📝 Example (Letter 'H')
```echo
$ Printing 'H' (ASCII 72)
A s s s s s s s s s s s s s s s s s s @
$ (Or use Scream + Pauses)
```

________________________________________________________________

# 🔊 EchoChamber (v1.1)

**EchoChamber** — эзотерический язык, основанный на акустике. Теперь с поддержкой **Extended ASCII (0-255)**.

## 🌌 Концепция
- Каждое **перемещение** или **пауза** — это **такт времени**.
- На каждом такте (`.`, `(`, `)`) звук во всех комнатах затухает на **1 единицу**.
- Команды `A`, `s`, `a`, `S` и `@` выполняются мгновенно и не вызывают затухания.

## 🛠 Синтаксис
- `A` (**Крик**) — Устанавливает громкость на **255**.
- `s` (**Шепот**) — Снижает громкость на **10**.
- `a` (**Усиление**) — Увеличивает громкость на **10**.
- `S` (**Тишина**) — Обнуляет громкость в текущей комнате.
- `.` (**Пауза**) — Тратит такт (звук падает на 1).
- `@` (**Слушать**) — Выводит символ (Extended ASCII).
- `(` / `)` — Переход в соседнюю комнату. Тратит такт (звук падает на 1).
