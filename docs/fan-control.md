# Fan control and verification

## Read fan RPM

```bash
cat /sys/class/hwmon/hwmon*/fan1_input
```

Example working output:

```text
1541
```

If the fan is stopped, this may show:

```text
0
```

## Read CPU temperature

```bash
cat /sys/class/thermal/thermal_zone0/temp
```

Example:

```text
50700
```

This means 50.7 °C.

## Temporary fan threshold test

Edit:

```bash
sudo vim /boot/firmware/config.txt
```

Add for testing:

```ini
dtparam=fan_temp0=40000
dtparam=fan_temp0_hyst=5000
```

Reboot:

```bash
sudo reboot
```

After testing, remove these lines if you want the default fan curve.
