
# Neolink

![Supports amd64 Architecture][amd64-shield]



## About
This Home Assistant App allows you to run Neolink directly on HAOS, providing a bridge between Reolink cameras using the proprietary Baichuan protocol and standard RTSP/MQTT clients.

It is based on the maintained [MutuallyAssuredDeployment/Neolink](https://github.com/MutuallyAssuredDeployment/neolink) fork and includes low-latency RTSP streaming, audio support, MQTT with Home Assistant Discovery, motion detection, PTZ, PIR, floodlight, siren, status LED, battery-camera support, multiple camera discovery methods, RTSP TLS, snapshots and additional camera/SD-card management features.

The low-latency RTSP mode reduces streaming delay through frame draining, live-mode AppSrc and reduced buffering, making it particularly suitable for real-time camera viewing and applications such as Home Assistant and Frigate.

Neolink does not require a Reolink NVR and does not modify the cameras.

## Installation & Configuration

[![Open your Home Assistant instance and show the add App repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fkhabbar-a%2Fhassio-apps)

1. Install this App in your HAOS instance.
2. The operating mode of Neolink defaults to `RTSP`. If you prefer `MQTT`, please change it within the App configuration. Or select `DUAL` if you want to use RTSP and MQTT in parallel.
3. Create the configuration file named `neolink.toml` in your HAOS `/addon_configs/a14d3924_neolink/` folder.
   - For configuration please follow [these](https://github.com/QuantumEntangledAndy/neolink#configusage) instructions.
   - Sample config file can be found [here](https://raw.githubusercontent.com/QuantumEntangledAndy/neolink/master/sample_config.toml).
4. Start the App and check the log output.
5. The log level defaults to `INFO`. You can set it to error, warn, info, or debug. Most users can leave it at info, but debug can be helpful if you have issues.

<!--

Notes to developers after forking or using the github template feature:
- While developing comment out the 'image' key from 'example/config.yaml' to make the supervisor build the App
  - Remember to put this back when pushing up your changes.
- When you merge to the 'main' branch of your repository a new build will be triggered.
  - Make sure you adjust the 'version' key in 'example/config.yaml' when you do that.
  - Make sure you update 'example/CHANGELOG.md' when you do that.
  - The first time this runs you might need to adjust the image configuration on github container registry to make it public
- Adjust the 'image' key in 'example/config.yaml' so it points to your username instead of 'home-assistant'.
  - This is where the build images will be published to.
- Rename the example directory.
  - The 'slug' key in 'example/config.yaml' should match the directory name.
- Adjust all keys/url's that points to 'home-assistant' to now point to your user/fork.
- Share your repository on the forums https://community.home-assistant.io/c/projects/9
- Do awesome stuff!
 -->

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg?style=for-the-badge
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg?style=for-the-badge
