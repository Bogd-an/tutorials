# MicroPython за пару хвилин

0. ESP01 з перехідником і кнопочками BOOT, RESET

1. На сайті https://espressif.github.io/esptool-js/ Program-Connect та вибираємо COM порт

2. Вписуємо адресу 0x0000 та файл https://micropython.org/resources/firmware/ESP8266_GENERIC-OTA-20240602-v1.23.0.bin або іншу

3. Затискаємо кнопки BOOT, RESET. Відпускаємо RESET потім BOOT.

4. Про всякий випадок чистимо пам'ять і починаємо прошивку

5. Тепер можна закрити цю вкладку і відкрити Online IDE https://viper-ide.org/index.html

6. Підключаємось:

![image](https://github.com/user-attachments/assets/19f5021d-8e8b-423b-9afe-e87ab5078784)

7. Можна зашити блінк

```python
#blink3.py
from machine import Pin
from time import sleep

print('blink3.py: run', end=' ')

LED_PIN = Pin(2, Pin.OUT)
for i in range(6):
    LED_PIN.value(bool(i%2))
    sleep(0.1)

del LED_PIN
print('end')
```

![image](https://github.com/user-attachments/assets/095b262e-093f-4ff7-aba0-94fea9f249b8)


8. Тепер буде тричі блимати під час старту :)
8. 
