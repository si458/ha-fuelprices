# Fuel Prices

[![GitHub Release][releases-shield]][releases]
[![GitHub Activity][commits-shield]][commits]
[![License][license-shield]](LICENSE)

![Project Maintenance][maintenance-shield]
[![BuyMeCoffee][buymecoffeebadge]][buymecoffee]

[![Discord][discord-shield]][discord]
[![Community Forum][forum-shield]][forum]

_Integration to integrate with [pyfuelprices][pyfuelprices]._

**This integration will set up the following platforms.**

| Platform         | Description                                                                  |
| ---------------- | ---------------------------------------------------------------------------- |
| `device_tracker` | Optional entities for fuel stations, attributes will contain fuel price data |

## Installation

1. Using the tool of choice open the directory (folder) for your HA configuration (where you find `configuration.yaml`).
1. If you do not have a `custom_components` directory (folder) there, you need to create it.
1. In the `custom_components` directory (folder) create a new folder called `fuel_prices`.
1. Download _all_ the files from the `custom_components/fuel_prices/` directory (folder) in this repository.
1. Place the files you downloaded in the new directory (folder) you created.
1. Restart Home Assistant
1. In the HA UI go to "Configuration" -> "Integrations" click "+" and search for "Fuel Prices"

## Privacy notice

This integration relies entirely on cloud services, alongside this a few libraries are used to geocode provided coordinates into location data for certain providers such as GasBuddy or TankerKoenig.

For reverse geocoding a mix of Nominatim (https://nominatim.org/), these-united-states (https://pypi.org/project/these-united-states/) and reverse-geocode (https://pypi.org/project/reverse-geocode/). This is done to improve performance, for example, looking up provided coordinates with reverse-geocode will allow us to restrict the fuel station search to data providers available in only that country.

Similar to this, this integration will use these-united-states to retrieve the state of given coordinates, and finally Nominatim is used to retrieve the nearest postcode for the TankerKoenig data source.

## Configuration is done in the UI

<!---->

## Contributions are welcome!

If you want to contribute to this please read the [Contribution guidelines](CONTRIBUTING.md)

---

[pyfuelprices]: https://github.com/pantherale0/pyfuelprices
[buymecoffee]: https://www.buymeacoffee.com/pantherale0
[buymecoffeebadge]: https://img.shields.io/badge/buy%20me%20a%20coffee-donate-yellow.svg?style=for-the-badge
[commits-shield]: https://img.shields.io/github/commit-activity/y/si458/ha-fuelprices.svg?style=for-the-badge
[commits]: https://github.com/si458/ha-fuelprices/commits/main
[discord]: https://discord.gg/Qa5fW2R
[discord-shield]: https://img.shields.io/discord/330944238910963714.svg?style=for-the-badge
[exampleimg]: example.png
[forum-shield]: https://img.shields.io/badge/community-forum-brightgreen.svg?style=for-the-badge
[forum]: https://community.home-assistant.io/
[license-shield]: https://img.shields.io/github/license/si458/ha-fuelprices.svg?style=for-the-badge
[maintenance-shield]: https://img.shields.io/badge/maintainer-%40si458-blue.svg?style=for-the-badge
[releases-shield]: https://img.shields.io/github/release/si458/ha-fuelprices.svg?style=for-the-badge
[releases]: https://github.com/si458/ha-fuelprices/releases
