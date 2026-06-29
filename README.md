# Rambox32

**Pigeon-racing timing terminal firmware for ESP32-S3 N16R8** — part of the [Node32-HUB](https://github.com/nasp2000/Node32-HUB) project.

Connects to Unikon electronic timing equipment via **RS232** (9600 baud), with email alerts, optional OLED display, OTA updates, and a web-based control panel with live pigeon-arrival monitoring.

---

## Features

### Communication
- **RS232 + Unikon** — connect directly to Unikon pigeon-racing timing/ring-reading equipment at 9600 baud.
- **Email alerts** — SMTP TLS and Google Apps Script support for automatic notifications.
- **Web UI** — full configuration, live monitoring, and event log from any browser.

### Web UI
The control panel runs entirely in the browser — all rendering and data processing is done locally. The ESP32 only sends raw data; the page never reloads.

- Live RS232 data reception and transmission log
- Unikon terminal interface
- Machine status and event monitoring
- Email configuration and testing
- OTA firmware updates
- LCD status display (OLED 0.96")

### Display (optional)
- **OLED screen** — real-time status dashboard showing clock, date, and recent pigeon arrivals. Not required for operation.

### Reliability
- Watchdog timer and crash recovery
- HTTP Basic Authentication for web access
- OTA updates for remote firmware upgrades
- NTP time synchronization

---

## Hardware Recommendation

**ESP32-S3 N16R8** (any generic devkit with 8 MB PSRAM).

The only tested class of board. - **MAX3232** — RS232 transceiver for Unikon communication
- **OLED 0.96" (SSD1306)** — optional I2C display for real-time status

---

## Quick start

1. Flash the pre-built binary to your ESP32-S3 N16R8 — recommended tool: [webflasher_Node32-HUB](https://github.com/nasp2000/webflasher_Node32-HUB) (binaries in Releases)
2. Connect the Unikon timing equipment to the RS232 port (UART2, 9600 baud)
3. Open `http://<esp32-ip>` in a browser
4. Configure WiFi, email, and Unikon settings via the web UI

---

## License

Same as Node32-HUB — see the [main repository](https://github.com/nasp2000/Node32-HUB).
