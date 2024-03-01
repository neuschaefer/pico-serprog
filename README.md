# pico-serprog (`next` branch)

This is a basic flashrom/serprog compatible SPI flash reader/writer for the Raspberry Pi Pico.

_NOTE: This is a fork of pico-serprog, in which a few feature branches are
merged. The list of branches is specified in `next.sh`._

It does not require a custom version of flashrom, just drag the compiled uf2 onto your Pico and you're ready to go.

The default pin-out is:

| GPIO | Pico Pin | Function |
|------|----------|----------|
| 1    |    2     | CS       |
| 2    |    4     | SCK      |
| 3    |    5     | MOSI     |
| 4    |    6     | MISO     |

## Usage

Dump a flashchip:

```
flashrom -p serprog:dev=/dev/ttyACM0:115200,spispeed=12M -r foo.bin
```

## License

The project is based on the spi_flash example by Raspberry Pi (Trading) Ltd. which is licensed under BSD-3-Clause.

As a lot of the code itself was heavily inspired/influenced by `stm32-vserprog` this code is licensed under GPLv3.
