# 🔊 EchoChamber (v1.0)

**EchoChamber** is a challenging esoteric programming language based on acoustics and sound decay. Here, data isn't just numbers—it's volume that fades with every passing moment.

## 🌌 Concept
The program runs in a space of 300 "rooms".
- Every action (command) is a **time tick**.
- On every tick, the volume in ALL rooms decays by **1 unit**.
- If the volume drops to **0**, the data is lost (silence).

## 🛠 Syntax
- `A` (**Scream**) — Sets volume in the current room to **127** (max).
- `s` (**Whisper**) — Decreases volume by **10** (+1 from the tick decay).
- `.` (**Pause**) — Does nothing but spends a tick (volume drops by 1). Any character not recognized as a command is treated as a pause.
- `@` (**Listen**) — Outputs the ASCII character of the current volume.
- `(` / `)` — Move the pointer to the left or right room.
- `[` ... `]` — **Mirror Loop**. Repeats as many times as the volume level was when entering the loop. The loop breaks if silence (0) occurs.
- `$` — Comment (ignored until the end of the line).

## 🚀 How to Run
Simply open `index.html` in any web browser. You can write and execute code in the interactive environment.

## 📝 Example (Letter 'H')
```echo
$ Printing 'H' (ASCII 72)
A s s s s . . . . . . . . . . @
```

________________________________________________________________

# 🔊 EchoChamber (v1.0)

**EchoChamber** — это сложный эзотерический язык программирования, основанный на концепции акустики и затухания звука. Здесь данные — это не просто числа, а громкость, которая исчезает с каждым мгновением.

## 🌌 Концепция
Программа выполняется в пространстве из 300 «комнат». 
- Каждое действие (команда) — это **такт времени**.
- На каждом такте звук во всех комнатах затухает на **1 единицу**.
- Если громкость падает до **0**, данные считаются утраченными (тишина).

## 🛠 Синтаксис
- `A` (**Крик**) — Устанавливает громкость в текущей комнате на **127** (макс).
- `s` (**Шепот**) — Снижает громкость на **10** (+1 от затухания такта).
- `.` (**Пауза**) — Ничего не делает, но тратит такт (звук падает на 1). Любой другой символ (кроме команд) также считается паузой.
- `@` (**Слушать**) — Выводит символ ASCII, соответствующий текущей громкости.
- `(` / `)` — Переход в соседнюю комнату влево или вправо.
- `[` ... `]` — **Зеркальный цикл**. Повторяется столько раз, сколько было громкости при входе. Цикл прерывается, если наступает тишина.
- `$` — Комментарий (игнорируется до конца строки).

## 🚀 Запуск
Просто откройте `index.html` в любом браузере. Вы можете писать и запускать код в интерактивной среде.

## 📝 Пример (Буква 'H')
```echo
$ Печать буквы 'H' (ASCII 72)
A s s s s . . . . . . . . . . @
```
