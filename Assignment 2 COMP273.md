Winter 2025
Abdoul Wahab Toure
261227818

## Q2

**FSM Diagram**
![[fsm diagram|1000]]

**Next state function truth table**
Input: `State[4..0]`, `Ready`.
Output: `NextState[4..0]`.

| Name        | State[4..0] | Ready |     | NextState[4..0] |
| ----------- | ----------- | ----- | --- | --------------- |
| Wait        | 00000       | 0     |     | 00000           |
| Wait        | 00000       | 1     |     | 00001           |
| Clear       | 00001       | -     |     | 00010           |
| Load        | 00010       | -     |     | 00011           |
| Shift+DD    | 00011       | -     |     | 00100           |
| Shift+DD    | 00100       | -     |     | 00101           |
| Shift+DD    | 00101       | -     |     | 00110           |
| Shift+DD    | 00110       | -     |     | 00111           |
| Shift+DD    | 00111       | -     |     | 01000           |
| Shift+DD    | 01000       | -     |     | 01001           |
| Shift+DD    | 01001       | -     |     | 01010           |
| Shift+DD    | 01010       | -     |     | 01011           |
| Shift+DD    | 01011       | -     |     | 01100           |
| Shift+DD    | 01100       | -     |     | 01101           |
| Shift+DD    | 01101       | -     |     | 01110           |
| Shift+DD    | 01110       | -     |     | 01111           |
| Shift+DD    | 01111       | -     |     | 10000           |
| Shift+DD    | 10000       | -     |     | 10001           |
| Shift+DD    | 10001       | -     |     | 10010           |
| Shift+DD    | 10010       | -     |     | 10011           |
| Add digit   | 10011       | -     |     | 10100           |
| Add digit   | 10100       | -     |     | 10101           |
| Add digit   | 10101       | -     |     | 10110           |
| Add digit   | 10110       | -     |     | 10111           |
| Add digit   | 10111       | -     |     | 11000           |
| Add newline | 11000       | -     |     | 11001           |
| Done        | 11001       | -     |     | 00000           |

**Output function truth table**
Input: `State[4..0]`.
Output: `CLR`, `Load`, `WESR`, `DD`, `WE`, `NewLine`, `EnableTTY`, `Done`.

| Name        | State[4..0] |     | CLR | Load | WESR | DD  | WE  | NewLine | EnableTTY | Done |
| ----------- | ----------- | --- | --- | ---- | ---- | --- | --- | ------- | --------- | ---- |
| Wait        | 00000       |     | 0   | 0    | 0    | 1   | 0   | 0       | 0         | 0    |
| Clear       | 00001       |     | 1   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Load        | 00010       |     | 0   | 1    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 00011       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 00100       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 00101       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 00110       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 00111       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 01000       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 01001       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 01010       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 01011       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 01100       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 01101       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 01110       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 01111       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 10000       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 10001       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Shift+DD    | 10010       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    |
| Add digit   | 10011       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    |
| Add digit   | 10100       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    |
| Add digit   | 10101       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    |
| Add digit   | 10110       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    |
| Add digit   | 10111       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    |
| Add newline | 11000       |     | 0   | 0    | 1    | 0   | 1   | 1       | 1         | 0    |
| Done        | 11001       |     | 0   | 0    | 1    | 0   | 1   | 1       | 1         | 1    |

## Q3

**FSM Diagram** (same as in Q2)
![[fsm diagram|1000]]
(during the `Add digit` stage, the converter checks if number is 0 or if it's the last digit to determine if we write or not the TTY)

**Next state function truth table** (same as in Q2)

**Output function truth table**
Input: `State[4..0]`.
Output: `CLR`, `Load`, `WESR`, `DD`, `WE`, `NewLine`, `EnableTTY`, `Done`, `LastDigit`.

| Name        | State[4..0] |     | CLR | Load | WESR | DD  | WE  | NewLine | EnableTTY | Done | LastDigit |
| ----------- | ----------- | --- | --- | ---- | ---- | --- | --- | ------- | --------- | ---- | --------- |
| Wait        | 00000       |     | 0   | 0    | 0    | 1   | 0   | 0       | 0         | 0    | 0         |
| Clear       | 00001       |     | 1   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Load        | 00010       |     | 0   | 1    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 00011       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 00100       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 00101       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 00110       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 00111       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 01000       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 01001       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 01010       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 01011       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 01100       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 01101       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 01110       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 01111       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 10000       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 10001       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         |
| Shift+DD    | 10010       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 1         |
| Add digit   | 10011       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    | 1         |
| Add digit   | 10100       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    | 1         |
| Add digit   | 10101       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    | 1         |
| Add digit   | 10110       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    | 1         |
| Add digit   | 10111       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    | 1         |
| Add newline | 11000       |     | 0   | 0    | 1    | 0   | 1   | 1       | 1         | 0    | 1         |
| Done        | 11001       |     | 0   | 0    | 1    | 0   | 1   | 1       | 1         | 1    | 1         |

## Q4

**FSM Diagram** (same as in Q2 & Q3)
![[fsm diagram|1000]]
(During the `Load` state, converter checks if number is negative and adds minus sign to TTY)

**Next state function truth table** (same as in Q2 & Q3)

**Output function truth table**
Input: `State[4..0]`.
Output: `CLR`, `Load`, `WESR`, `DD`, `WE`, `NewLine`, `EnableTTY`, `Done`, `LastDigit`, `SetMinus`.

| Name        | State[4..0] |     | CLR | Load | WESR | DD  | WE  | NewLine | EnableTTY | Done | LastDigit | SetMinus |
| ----------- | ----------- | --- | --- | ---- | ---- | --- | --- | ------- | --------- | ---- | --------- | -------- |
| Wait        | 00000       |     | 0   | 0    | 0    | 1   | 0   | 0       | 0         | 0    | 0         | 0        |
| Clear       | 00001       |     | 1   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Load        | 00010       |     | 0   | 1    | 1    | 1   | 1   | 0       | 1         | 0    | 0         | 1        |
| Shift+DD    | 00011       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 00100       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 00101       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 00110       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 00111       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 01000       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 01001       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 01010       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 01011       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 01100       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 01101       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 01110       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 01111       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 10000       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 10001       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 0         | 0        |
| Shift+DD    | 10010       |     | 0   | 0    | 1    | 1   | 1   | 0       | 0         | 0    | 1         | 0        |
| Add digit   | 10011       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    | 1         | 0        |
| Add digit   | 10100       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    | 1         | 0        |
| Add digit   | 10101       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    | 1         | 0        |
| Add digit   | 10110       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    | 1         | 0        |
| Add digit   | 10111       |     | 0   | 0    | 1    | 0   | 1   | 0       | 1         | 0    | 1         | 0        |
| Add newline | 11000       |     | 0   | 0    | 1    | 0   | 1   | 1       | 1         | 0    | 1         | 0        |
| Done        | 11001       |     | 0   | 0    | 1    | 0   | 1   | 1       | 1         | 1    | 1         | 0        |
