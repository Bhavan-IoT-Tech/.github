# Bhavan IoT Tech

**Thoughtful, local-first technology for a smarter home.**

Bhavan is a smart-home platform designed to keep everyday control and automation on your local network. Its hub brings devices together; custom ESP32 nodes connect physical sensors and actuators; and an Android app provides a mobile control surface.

## What we’re building

- **Bhavan Hub** — a FastAPI service with a local SQLite database, MQTT messaging, device state, automations, and integrations.
- **Bhavan Nodes** — ESP32 firmware for sensors and actuators, communicating with the hub over MQTT/TLS.
- **Bhavan Mobile** — a native Android client built with Kotlin and Jetpack Compose, with hub discovery and live device updates.
- **Bhavan Web** — a lightweight website for the project.
- **Bhavan Docs** — setup guides, hardware and wiring references, API contracts, architecture, and decision records.

The system is intended to keep core home control available on the LAN without depending on a public cloud service. Remote access and optional third-party integrations are separate from that local-first core.

## Repositories

- [Bhavan Workspace](https://github.com/Bhavan-IoT-Tech/bhavan-workspace) — umbrella workspace that pins the component repositories as Git submodules.
- [Hub](https://github.com/Bhavan-IoT-Tech/hub)
- [Nodes](https://github.com/Bhavan-IoT-Tech/nodes)
- [Mobile App](https://github.com/Bhavan-IoT-Tech/mobile-app)
- [Web](https://github.com/Bhavan-IoT-Tech/bhavan-web)
- [Documentation](https://github.com/Bhavan-IoT-Tech/docs)

> **Repository access:** the project repositories are currently private. Links are available to authorized organization members.

## Working with the workspace

Clone the umbrella repository together with its component repositories:

```sh
git clone --recurse-submodules https://github.com/Bhavan-IoT-Tech/bhavan-workspace.git
```

If you already have the workspace checkout, initialize or update the components with:

```sh
git submodule update --init --recursive
```

For component-specific setup and hardware guidance, start with the README in that repository and the documentation repository. Keep credentials, private keys, generated certificates, and device-specific secrets out of Git.

## Project principles

- Local control and privacy by default
- Clear boundaries between hub, firmware, mobile client, and integrations
- Secure device communication and explicit handling of credentials
- Practical documentation and incremental validation on real hardware

Bhavan is under active development. Hardware-specific behavior should be verified against the relevant setup and safety documentation before deployment.
