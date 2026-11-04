# Honda ECU Suite — Diagnostic Foundation v0.2

Responsive React + TypeScript + Vite app with muted-purple UI, Three.js 3D surface preview, dashboard, ECU discovery UI, DTC UI, live-data UI and USB serial connection scaffold.

## Run locally

```bash
npm install
npm run dev
```

For deployment, use HTTPS. Desktop Chrome/Edge is the initial reference environment.

## Implemented

- Responsive desktop/mobile layout and muted-purple theme.
- Three.js demo surface (not an ECU fuel/ignition map).
- USB Web Serial port picker and serial open scaffold.
- Diagnostic screens for ECU discovery, live data, DTC and serial monitor.
- Demo telemetry clearly marked as simulated.

## Not yet implemented

- Honda-specific K-Line wake-up/initialization and ECU identification.
- Real DTC read/clear commands and Live Data decoding.
- Firmware reading/writing, map definitions, checksum, security access or flashing.

The app intentionally does not send guessed bytes to a vehicle ECU. FT232RL is only USB-UART; use a suitable protected K-Line transceiver. Actual Android browser USB serial support varies by device/browser/adapter and must be tested. If direct Web Serial is unavailable, add a native Android USB bridge while retaining this web UI.

Before enabling ECU write/flash: verify exact ECU family, electrical interface, init timing, protocol, memory layout, backup/recovery method and checksum on appropriate bench equipment.
