Certo 👍 Ti lascio direttamente il contenuto **pronto da copiare e incollare nel file `README.md` su GitHub**:

````markdown
[![buy_me_a_coffee](https://img.shields.io/badge/If%20you%20like%20it-Buy%20me%20a%20coffee-yellow.svg?style=for-the-badge)](https://www.buymeacoffee.com/dirkmaucher)
[![paypal](https://img.shields.io/badge/If%20you%20like%20it-PayPal%20Me-blue.svg?style=for-the-badge)](https://paypal.me/dirkmaucher)

# Neolink

![Supports amd64 Architecture][amd64-shield]

## About

This Home Assistant App allows you to run **Neolink** directly on HAOS, providing a bridge between Reolink cameras using the proprietary **Baichuan protocol** and standard RTSP/MQTT clients.

It is based on the **MutuallyAssuredDeployment/Neolink** fork and includes **low-latency RTSP streaming**, audio support, MQTT with Home Assistant Discovery, motion detection, PTZ, PIR, floodlight, siren, status LED, battery-camera support, multiple camera discovery methods, RTSP TLS, snapshots and additional camera/SD-card management features.

The **Low Latency RTSP** mode reduces streaming delay through frame draining, live-mode AppSrc and reduced buffering, making it particularly suitable for real-time camera viewing and applications such as **Home Assistant and Frigate**.

Neolink does not require a Reolink NVR and does not modify the cameras.

For more information, see the [MutuallyAssuredDeployment/Neolink](https://github.com/MutuallyAssuredDeployment/neolink) project.

## Installation & Configuration

[![Open your Home Assistant instance and show the add App repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fkhabbar-a%2Fhassio-apps)

1. Install this App in your HAOS instance.

2. The operating mode of Neolink defaults to `RTSP`. You can also select `MQTT` or `DUAL` to use RTSP and MQTT simultaneously.

3. Create the configuration file:

   ```text
   /addon_configs/a14d3924_neolink/neolink.toml
````

4. Configure your Reolink cameras using the Neolink configuration file.

   For complete configuration options, see the [MutuallyAssuredDeployment/Neolink documentation](https://github.com/MutuallyAssuredDeployment/neolink/blob/master/README.md).

5. Start the App and check the log output.

6. The log level defaults to `INFO`. You can set it to `error`, `warn`, `info`, or `debug`.

## Low Latency RTSP

The main feature of this App is support for **Low Latency RTSP** from the MutuallyAssuredDeployment fork.

Low Latency mode reduces stream delay using frame draining, live-mode AppSrc and reduced buffering.

This makes it particularly useful for:

* Real-time camera viewing
* Home Assistant dashboards
* Frigate
* Video surveillance applications

## MQTT

Neolink supports **MQTT** and **Home Assistant MQTT Discovery**.

Depending on the camera model, MQTT can provide access to features such as:

* Motion detection
* PIR
* PTZ
* Floodlight
* IR
* Status LED
* Siren
* Battery status
* Camera controls

The App supports:

* `RTSP`
* `MQTT`
* `DUAL`

## Supported Features

The underlying Neolink fork provides support for a wide range of Reolink camera features, including:

* Low-latency RTSP streaming
* RTSP video
* Audio
* MQTT
* Home Assistant MQTT Discovery
* PTZ controls
* Motion detection
* PIR
* Floodlight
* Siren
* IR
* Status LED
* Battery cameras
* Camera discovery
* Snapshots
* RTSP TLS
* SD-card and recording features

For the complete list of supported features and configuration options, see the [official Neolink documentation](https://github.com/MutuallyAssuredDeployment/neolink/blob/master/README.md).

## Credits

This App is based on the [MutuallyAssuredDeployment/Neolink](https://github.com/MutuallyAssuredDeployment/neolink) project.

Neolink is not affiliated with Reolink.

[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg?style=for-the-badge

```

**Nota:** ho mantenuto `amd64` perché è l'architettura che hai verificato funzionare con l'immagine che stai usando.
```
