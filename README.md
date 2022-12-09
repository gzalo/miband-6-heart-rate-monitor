# Xiaomi Band 7  Monitor

View Xiaomi Band 7 Data within your browser.


Changelog:
- Updated BLE UUIDs, Endpoints, and other constants to work with the updated Xiaomi/Amazfit?/ZeppOS firmwares
- **Fixed authentication so it works with modern firmwares (Thanks Gadgetbridge for the inspiration, tiny-ecdh-c for elliptic curve Diffie-Hellman implementation)** 

## Requirements

1. A device with Bluetooth support
2. A browser that supports the Web Bluetooth API (check [here](https://caniuse.com/web-bluetooth))
3. An auth key for your Band (check out https://codeberg.org/Freeyourgadget/Gadgetbridge/wiki/Huami-Server-Pairing)

## How to use

1. Build and launch
2. Insert your Mi Band's auth key
3. Wear your Mi Band
3. Click connect
4. TODO: Acquire data and display

For data and troubleshooting, check the browser's developer console. The class can be interacted with via a `band = new Band7("0e5b827d9b8cded4a0fd0ab345b881d4"); band.init();` call in the console.

## Inspiration
- [hgzalo/miband-6-heart-rate-monitor](https://github.com/gzalo/miband-6-heart-rate-monitor) The latest maintainer in the chain - implemented the new Auth
- [Freeyourgadget/Gadgetbridge](https://codeberg.org/Freeyourgadget/Gadgetbridge)  Invaluable resource for the new (called 2021 within that project) BLE API and data reconstruction
- [Jaapp-/miband-5-heart-rate-monitor](https://github.com/Jaapp-/miband-5-heart-rate-monitor)
- [satcar77/miband4](https://github.com/satcar77/miband4)
- [vshymanskyy/miband-js](https://github.com/vshymanskyy/miband-js)
- [VladKolerts/miband4](https://github.com/VladKolerts/miband4)

## Libraries

- [tiny-ECDH-wasm (used for modern auth)](https://github.com/gzalo/tiny-ECDH-wasm)

## External Tools

- [Wireshark]() Capturing traffic to/from Mi Fitness app and the Band 7
- [Windows Bluetooth Virtual Sniffer](https://learn.microsoft.com/en-us/windows-hardware/drivers/bluetooth/testing-btp-tools-btvs) Compare "Official" traffic from the Mi Fitness app versus this reconstruction.