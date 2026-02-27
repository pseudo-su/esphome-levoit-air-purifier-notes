# Leviot

## Notes

Here lies my failed attempt to connect to and flash my levoit core 300s air purifier

- https://devices.esphome.io/devices/levoit-core-300s/
- https://github.com/acvigue/esphome-levoit-air-purifier
- https://www.amazon.com.au/dp/B08763GK1Q?ref_=ppx_hzsearch_conn_dt_b_fed_asin_title_1
- https://esphome.io/guides/physical_device_connection/

```sh
brew install uv
# uv add esphome
# uv add esptool

cp secrets.example.yaml secrets.yaml

uv run esptool -p /dev/cu.usbserial-AB99H905 read_flash 0 ALL levoit.bin
# sudo uv run esptool -p /dev/ttyUSB0 read-flash 0 ALL levoit.bin

# uv run esphome --dashboard run levoit-300s-configuration.yaml --device /dev/ttyUSB0
```

![](./images/board.jpg)
![](./images/board-soldered.jpg)
![](./images/esp-wiring.png)
![](./images/uart-cable.jpg)
