# 🔊 EchoChamber (v1.0)

**EchoChamber** is a minimalist and hardcore esoteric programming language inspired by Brainfuck but built on the laws of acoustics. Here, your data is **volume**, which decays over time.

---

## 🌌 Concept (The Core)

The program runs in a space of **300 rooms** (memory cells).
1. **Data**: Each room stores a volume value from **0 to 255** (Extended ASCII).
2. **Time (Decay)**: Volume is energy. Any physical action (moving between rooms or inputting data) spends time and causes the sound in **all** rooms to decay by **1 unit**.
3. **Silence**: If the volume drops to 0, the data is lost.

---

## 🛠 Syntax (8 Commands)


| Command | Description | Decay (-1) |
|:-------:|:---------|:--------------:|
| `+` | Increase volume in the current room by **1**. | No |
| `-` | Decrease volume in the current room by **1**. | No |
| `@` | **Listen**: Output the ASCII character of the current volume. | No |
| `,` | **Input**: Read a character and set the room's volume to its code. | **Yes** |
| `(` | Move to the room on the **left**. | **Yes** |
| `)` | Move to the room on the **right**. | **Yes** |
| `[` | Start of an acoustic loop / macro. | No |
| `]` | End of an acoustic loop / macro. | No |
| `$` | Comment (ignored until the end of the line). | No |

---

## 🌀 Smart Loops & Macros

In EchoChamber, loops are more efficient than in classic Brainfuck. They allow for rapid volume manipulation.

### 1. Multipliers
If there is a value before the loop (e.g., you pressed `+++`), the commands inside the loop are multiplied by that value.
- `+++ [ +++++++++++ ]` — Adds **33** to the current volume ($3 \times 11$).
- `+++++ [ -- ]` — Subtracts **10** from the current volume ($5 \times 2$).

### 2. Acoustic Macros (Presets)
Special combinations inside brackets allow you to instantly change the room's state:
- `[-]` — **Mute**: Instantly resets volume to **0**.
- `[+]` — **Standard**: Sets volume to **127** (Standard ASCII limit).
- `[++]` — **Max Resonance**: Sets volume to **255** (Extended ASCII limit).

---

## 📝 Code Examples

### Printing "HI!"
```echo
[+] $ Set to 127
---------- ---------- ---------- ---------- ---------- ----- @ $ H (72)
+ @ $ I (73)
[-] +++ [ ++++++++++ ] +++ @ $ ! (33)
```

________________________________________________________________

# 🔊 EchoChamber (v1.0)

**EchoChamber** — это минималистичный и хардкорный эзотерический язык программирования, вдохновленный Brainfuck, но построенный на законах акустики. Здесь ваши данные — это **громкость звука**, которая затухает с течением времени.

---

## 🌌 Концепция (Основа)

Программа выполняется в пространстве из **300 комнат** (ячеек памяти).
1. **Данные**: В каждой комнате хранится значение громкости от **0 до 255** (Extended ASCII).
2. **Время (Decay)**: Любое физическое действие (перемещение между комнатами или ввод данных) тратит время и заставляет звук во **всех** комнатах затухать на **1 единицу**.
3. **Тишина**: Если громкость падает до 0, данные считаются утраченными.

---

## 🛠 Синтаксис (8 Команд)


| Команда | Описание | Затухание (-1) |
|:-------:|:---------|:--------------:|
| `+` | Увеличить громкость на **1**. | Нет |
| `-` | Уменьшить громкость на **1**. | Нет |
| `@` | **Listen**: Вывести ASCII-символ текущей громкости. | Нет |
| `,` | **Input**: Считать символ и записать его код в комнату. | **Да** |
| `(` | Перейти в комнату **слева**. | **Да** |
| `)` | Перейти в комнату **справа**. | **Да** |
| `[` | Начало акустического цикла / макроса. | Нет |
| `]` | Конец акустического цикла / макроса. | Нет |
| `$` | Комментарий (игнорируется). | Нет |

---

## 🌀 Умные циклы и Макросы

Циклы в EchoChamber работают как множители, позволяя быстро менять громкость.

### 1. Множители (Multipliers)
Если перед циклом стоит значение, команды внутри цикла умножатся на него.
- `+++ [ +++++++++++ ]` — Добавит **33** к громкости ($3 \times 11$).
- `+++++ [ -- ]` — Вычтет **10** ($5 \times 2$).

### 2. Акустические макросы (Presets)
Мгновенная настройка состояния комнаты:
- `[-]` — **Mute**: Обнуляет громкость.
- `[+]` — **Standard**: Устанавливает громкость на **127**.
- `[++]` — **Max Resonance**: Устанавливает громкость на **255**.

---

## 📝 Примеры кода

### Печать "HI!"
```echo
[+] $ Ставим 127
---------- ---------- ---------- ---------- ---------- ----- @ $ H (72)
+ @ $ I (73)
[-] +++ [ ++++++++++ ] +++ @ $ ! (33)
```
