## 人体红外感模块

[文档](https://docs.particle.io/assets/datasheets/makerkit/pir-sensor.pdf)


```python
import time
import RPi.GPIO as GPIO

# 信号管脚
PIN_SIGNAL = 40

GPIO.setmode(GPIO.BOARD)
GPIO.setwarnings(False)
GPIO.setup(PIN_SIGNAL, GPIO.IN)


while True:
    if GPIO.input(PIN_SIGN):
        print("有人在！！！")
        # 检测到有人后会持续几秒钟的高电平
        time.sleep(5)
    else:
    print("没人...")
    time.sleep(1)
```