# Lightweight ESP-AT parser

LwESP is lightweight ESP AT commands parser library to communicate with ESP8266 or ESP32 Wi-Fi modules using AT commands.
Module is written in C11 and is system platform agnostic. Its main targets are embedded system devices like ARM Cortex-M, AVR, PIC and others, but can easily work under `Windows`, `Linux` or `MAC` environments too.

Espressif module runs official [AT Commands (esp-at)](https://github.com/espressif/esp-at) software and communicates with host device via UART or SPI communication protocol.

Follow documentation for more information on implementation and details.

[Open documentation](https://docs.majerle.eu/projects/lwesp/)

## Features

- Written in C (C11), compatible with `stdint.h` data types
- Supports latest ESP32, ESP32-C2, ESP32-C3, ESP32-C6 & ESP8266 AT software from Espressif Systems
- Platform independent and easy to port
  - Library is developed under Win32 platform
  - Available examples for ARM Cortex-M, Win32 or POSIX (mostly Linux) platforms
- Allows different configurations to optimize user requirements
- Supports operating-system implementations with advanced inter-thread communication (or RTOS)
  - Currently only OS mode is supported
  - Uses `2` different threads to process user input and received data
    - Producer thread collects user commands from application threads and starts command execution
    - Process thread processes received data from the ESP device
- Netconn-based sequential API for connections in client and server mode
- Includes several applications built on top of the library
  - HTTP server with dynamic files (file system) support
  - MQTT client
- Embeds other AT features, such as WPS management, custom DNS setup, hostname for DHCP, and ping
- Optional IPv6 support
- mDNS, SNTP time sync and SmartConfig provisioning modules
- System flash and manufacturing NVS read/write/erase access
- Optional CLI module with ready-made commands for common operations
- User friendly MIT license

## Contribute

Fresh contributions are always welcome. Simple instructions to proceed:

1. Fork Github repository
2. Follow [C style & coding rules](https://github.com/MaJerle/c-code-style) and use `clang-format` to format the code
3. Create a pull request to `develop` branch with new features or bug fixes

Alternatively you may:

1. Report a bug
2. Ask for a feature request
