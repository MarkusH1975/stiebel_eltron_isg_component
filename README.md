# Stiebel Eltron ISG integration

[![GitHub Release][releases-shield]][releases]
[![GitHub Activity][commits-shield]][commits]
[![Github Downloads](https://img.shields.io/github/downloads/pail23/stiebel_eltron_isg_component/total)](https://github.com/pail23/stiebel_eltron_isg_component) [![Github Downloads](https://img.shields.io/github/downloads/pail23/stiebel_eltron_isg_component/latest/total)](https://github.com/pail23/stiebel_eltron_isg_component)
[![License][license-shield]](LICENSE)

[![hacs][hacsbadge]][hacs]
![Project Maintenance][maintenance-shield]
[![BuyMeCoffee][buymecoffeebadge]][buymecoffee]

[![Community Forum][forum-shield]][forum]


## Prerequisite
In order to use this Integration you need:

1. ISG device connected to the heatpump and your local network
2. IP address of the ISG device on your local network

For connecting the ISG device to your heatpump refer to the corresponding Stiebel Eltron documentation or ask your installer.
There is no need to get the "STIEBEL ELTRON Web-Monitoring" subscription, this is for Stiebel Eltron itself monitoring your Heatpump and NOT needed for this integration to work.

If you are using the ISG with the [STIEBEL ELTRON EMI extension](https://www.stiebel-eltron.de/de/home/service/smart-home/energy-management-interface-emi.html) make sure that your ISG Firmware is current because this Integration is using Modbus, older versions of ISG Software are not able to do Modbus and EMI at the same time. (ISG Software Version `v12.1.2` was tested by [@northalpha](https://github.com/northalpha) using this integration to be working). 
An update may be triggered via Stiebel Eltron Support (Kundendienst).

## Installation

### Using HACS


This is the preferred installation option. If you are using HACS:
1. Add the component to your home assistant installation: [![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=pail23&repository=stiebel_eltron_isg_component&category=integration)
2. Add the _Stiebel Eltron ISG_ Integration in HACS and restart Home Assistant
3. In the HA UI go to "Configuration" -> "Integrations" click "+" and search for "Stiebel Eltron ISG"

### Manual installation:

1. Using the tool of choice open the directory (folder) for your HA configuration (where you find `configuration.yaml`).
2. If you do not have a `custom_components` directory (folder) there, you need to create it.
3. In the `custom_components` directory (folder) create a new folder called `stiebel_eltron_isg`.
4. Download _all_ the files from the `custom_components/stiebel_eltron_isg/` directory (folder) in this repository.
5. Place the files you downloaded in the new directory (folder) you created.
6. Restart Home Assistant
7. In the HA UI go to "Configuration" -> "Integrations" click "+" and search for "Stiebel Eltron ISG"




## Configuration is done in the UI

<!---->


## Modbus Address Reference
[ISG web (229336), ISG plus (233493) Modbus Documentation](https://www.stiebel-eltron.de/content/dam/ste/cdbassets/installation/ISG_Modbus/321798-44755-9770_ISG%20Modbus_de_en_fr_it_nl_cs_sk_pl_hu.pdf)

### Why Modbus Address in Code and Documentation Differ

Modbus addresses in the code are typically zero-based (starting from 0), while documentation often uses one-based addresses (starting from 1). For example, an address listed as `5001` in the documentation would correspond to `5000` in the code.


## Contributions are welcome!

If you want to contribute to this please read the [Contribution guidelines](CONTRIBUTING.md)

***

[stiebel_eltron_isg]: https://github.com/pail23/stiebel_eltron_isg
[buymecoffee]: https://www.buymeacoffee.com/pail23
[buymecoffeebadge]: https://img.shields.io/badge/buy%20me%20a%20coffee-donate-yellow.svg
[commits-shield]: https://img.shields.io/github/commit-activity/y/pail23/stiebel_eltron_isg_component
[commits]: https://github.com/pail23/stiebel_eltron_isg/commits/master
[hacs]: https://github.com/hacs
[hacsbadge]: https://img.shields.io/badge/HACS-Default-orange
[forum-shield]: https://img.shields.io/badge/community-forum-brightgreen
[forum]: https://community.home-assistant.io/
[license-shield]: https://img.shields.io/github/license/pail23/stiebel_eltron_isg_component
[maintenance-shield]: https://img.shields.io/badge/maintainer-Paul%20Frank-green
[releases-shield]: https://img.shields.io/github/v/release/pail23/stiebel_eltron_isg_component
[releases]: https://github.com/pail23/stiebel_eltron_isg/releases
