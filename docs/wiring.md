# Wiring

This document describes the wiring used for the Raspberry Pi 5 Noctua PWM fan adapter.

## Final functional mapping

| Function | Raspberry Pi 5 fan header | Noctua NF-A4x10 5V PWM wire |
|---|---:|---|
| +5V | Pin 1 | Yellow |
| PWM | Pin 2 | Blue |
| GND | Pin 3 | Black |
| Tach / RPM | Pin 4 | Green |

## Original fan reference

Forum-derived original Raspberry Pi 5 fan mapping used during the build:

```text
Pin 1 red wire  = 5V
Pin 2 blue wire = PWM
Pin 3 black wire = GND
Pin 4 yellow wire = Tach
```

## Adapter cable colors

The JST-SH cable used in this build had the following wire order:

```text
black  = pin 1
red    = pin 2
blue   = pin 3
yellow = pin 4
```

Because JST-SH/STEMMA/Qwiic cable colors may vary, verify the order with a multimeter.

## Noctua 5V PWM fan colors

```text
Yellow = +5V
Blue   = PWM
Black  = GND
Green  = Tach / RPM
```

![Noctua 5V PWM pinout](../images/noctua-5v-pwm-pinout.png)
