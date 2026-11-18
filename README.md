The **Solar Wheelchair** is a low-cost smart electric wheelchair. It is partly
charged by sunlight and controlled through a secure smartphone app.

In Egypt, many people with severe mobility disabilities rely on caregivers to move
around. Powered wheelchairs that give real independence are mostly imported and
expensive. Low-cost electric chairs usually offer only a joystick, with no battery
information, no remote monitoring, no emergency alert and no protection against
unauthorised use.

Our project upgrades a standard **24 V electric wheelchair** into a connected,
safer assistive platform:

- **Solar-assisted energy:** a 200 W roof-mounted solar panel charges the battery
  through an MPPT charge controller. This extends outdoor use and reduces
  dependence on mains power.
- **Smart control:** the owner or a caregiver can drive the chair from a virtual
  joystick or by **voice commands in Arabic and English**.
- **Live monitoring:** battery level, speed and solar power are shown in real time,
  with alerts for low battery and connection loss.
- **Security and safety by design:** only approved users can log in, every
  command is encrypted, the chair **stops smoothly if the phone disconnects**,
  and an **SOS button** shares the chair's GPS location with emergency contacts.

## System Architecture

| Layer | Components |
|---|---|
| **Energy** | 200 W solar panel · MPPT charge controller · 24 V battery · original mains charger |
| **Control** | ESP32 controller between the app and the drive system: receives authenticated BLE commands, enforces the speed limit, streams telemetry, fail-safe stop after 1.5 s of link loss |
| **Application** | Flutter app: secure login and roles, joystick and emergency stop, AR/EN voice control, live dashboard, SOS and navigation · Firebase for accounts, encrypted storage and notifications |

## Tech Stack

`Flutter` · `Dart` · `Firebase` · `ESP32` · `Bluetooth LE` · `Wi-Fi / WebSocket` · `Speech-to-Text` · `Solar PV / MPPT`

## Project Status

The mobile app is largely built and has been tested against a **simulated
wheelchair**. The next phase installs the hardware and connects it to the app
over Bluetooth LE.

## Keywords

Assistive Mobility · Solar Energy · IoT · Cybersecurity · Smart Wheelchair · Mobile Application
