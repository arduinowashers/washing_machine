# Проект за Симулатор на Перална Машина с Arduino

Този проект симулира работата на перална машина с помощта на Arduino. Симулаторът включва различни програми за пране, настройки за температура и обороти, както и симулация на различните фази на пране.

## Функционалности

- Избор между 12 различни програми за пране
- Настройки за температура и обороти за всяка програма
- Симулация на различни фази на пране (основно пране, изплакване, центрофуга)
- Визуализация на информацията чрез OLED дисплей
- Индикация за грешки с LED и звукови сигнали
- Звукова индикация при завършване на цикъла на пране

## Хардуерни компоненти

- Arduino Uno/Nano
- OLED дисплей (SSD1306 128x64)
- Серво мотор (симулира барабана)
- Бъзър (за звукови сигнали)
- 2 LED диода (жълт за работа, червен за грешки)
- 5 бутона (старт/пауза, нагоре, надолу, наляво, надясно)
- Резистори и свързващи проводници

## Схема на свързване

### Таблична схема

| Компонент | Arduino пин |
|-----------|-------------|
| Бутон Старт | D2 |
| Бутон Нагоре | D3 |
| Бутон Надолу | D4 |
| Бутон Наляво | D5 |
| Бутон Надясно | D6 |
| Бъзър | D7 |
| Серво мотор | D9 |
| Червен LED (грешка) | D12 |
| Жълт LED (работа) | D13 |
| OLED дисплей SDA | D20 |
| OLED дисплей SCL | D21 |
| Сензор за напрежение | A0 |

### ASCII схема
```
                                  +---------------------+
                                  |                     |
                                  |     Arduino         |
                                  |                     |
+--------+                        |                     |
| Бутон  |----------------------->| D2                  |
| Старт  |                        |                     |
+--------+                        |                     |
                                  |                     |
+--------+                        |                     |
| Бутон  |----------------------->| D3                  |
| Нагоре |                        |                     |
+--------+                        |                     |
                                  |                     |
+--------+                        |                     |
| Бутон  |----------------------->| D4                  |
| Надолу |                        |                     |
+--------+                        |                     |
                                  |                     |
+--------+                        |                     |
| Бутон  |----------------------->| D5                  |
| Наляво |                        |                     |
+--------+                        |                     |
                                  |                     |
+--------+                        |                     |
| Бутон  |----------------------->| D6                  |
| Надясно|                        |                     |
+--------+                        |                     |
                                  |                     |
+--------+                        |                     |
| Бъзър  |<-----------------------| D7                  |
+--------+                        |                     |
                                  |                     |
+--------+                        |                     |
| Серво  |<-----------------------| D9                  |
| мотор  |                        |                     |
+--------+                        |                     |
                                  |                     |
+--------+                        |                     |
| Червен |<-----------------------| D12                 |
| LED    |                        |                     |
+--------+                        |                     |
                                  |                     |
+--------+                        |                     |
| Жълт   |<-----------------------| D13                 |
| LED    |                        |                     |
+--------+                        |                     |
                                  |                     |
+--------+                        |                     |
| Сензор |----------------------->| A0                  |
| напреж.|                        |                     |
+--------+                        |                     |
                                  |                     |
+--------+                        |                     |
| OLED   |<---SDA---------------->| D20                  |
| Дисплей|<---SCL---------------->| D21                  |
+--------+                        |                     |
                                  +---------------------+
```