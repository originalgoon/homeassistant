# Home Asssistant Configuration

![](https://github.com/noodlemctwoodle/homeassistant/workflows/Home-Assistant-CI/badge.svg) 
[![Star](https://img.shields.io/github/stars/noodlemctwoodle/homeassistant?style=plastic)](https://github.com/noodlemctwoodle/homeassistant/stargazers) 
[![Star](https://img.shields.io/github/forks/noodlemctwoodle/homeassistant?style=plastic)](https://github.com/noodlemctwoodle/homeassistant/network/members)
[![Star](https://img.shields.io/github/issues/noodlemctwoodle/homeassistant?style=plastic)](https://github.com/noodlemctwoodle/homeassistant/issues)

Open source home automation that puts local control and privacy first. Powered by a worldwide community of tinkerers and DIY enthusiasts. 

#### Contents
* [UnRAID View HKI](https://github.com/noodlemctwoodle/homeassistant#unraid-monitoring-view-for-hki)
* [Home Assistant View](https://github.com/noodlemctwoodle/homeassistant#home-assistant-monitoring-view-for-hki)
* [Energy Monitoring](https://github.com/noodlemctwoodle/homeassistant##energy-monitoring-view-for-hki)

## Home Assistant Hardware Configuration
- Intel NUC i3 Gen 7
- Ubunbu Server 19.10
- Docker CE
- [Home Kit Infused](https://github.com/jimz011/homekit-infused)

## Hassio Installation on Ubuntu Server and Docker CE
The [Hassio](https://github.com/noodlemctwoodle/hassio/wiki/Install-Hass.io) guide describes how to install Hass.io on Ubuntu Server running Docker CE, configure custom storage paths using the pre-created script from [Home Assistant](https://github.com/home-assistant/hassio-installer) and exposed to the internet using Nabu Casa

## Check out my Wiki
Further information and guides can be found on my [wiki](https://github.com/noodlemctwoodle/hassio/wiki)

## HKI Documentation can be found here
[Documentation](https://jimz011.github.io/homekit-infused/)


## Donations are always welcome

<a href="https://www.buymeacoffee.com/noodlemctwoodle" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>


# UnRAID Monitoring View for HKI
## Version 1.2

![unraid-monitor](https://github.com/noodlemctwoodle/homeassistant/blob/master/www/images/github/views/unraid.gif)

### UnRAID Data Monitoring Feeds

| [UnRAID-API](https://github.com/noodlemctwoodle/homeassistant/blob/master/packages/ha-core/areas/cabinet/devices/unraid/readme.md#unraid-api-configuration) | [UnRAID-SNMP](https://github.com/noodlemctwoodle/homeassistant/blob/master/packages/ha-core/areas/cabinet/devices/unraid/readme.md#unraid-snmp-configuration) | [UnRAID Glances Container](https://github.com/nicolargo/glances) |
|-----------------------|-----------------|--------------------------------|
| View arrayStatus      | HDD Array Temps | View total per disk used space |
| View arrayProtection  | LAN Throughput  | View total per disk free space |
| Total arrayDiskSpace  | Disk Space      | View CPU usage                 |
| Start/Stop Containers | CPU Load        | View RAM usage                 |

Version 1.0
 - Initial view
 - Glances container support
 - Glances Home Assistant Integration

Version 1.1
 - Added swipe card for docker containers
 - UnRAID-API added
 - Container Support

Version 1.2
 - Added SNMP [config](https://github.com/noodlemctwoodle/homeassistant/tree/master/configuration/sensors/monitoring/unraid)
 - Moved temperature cards to swipe-card to reduce screen real estate
 - combined disk usage into swipe card
 - Added HDD temperatures to temperatures swipe-card
 - Added LAN Throughput bar graph to resources swipe-card
 - Removed Tap actions on mini-graph-card and bar-card
 - Fixed graph height issue on swipe-card
 - Added bullets to swipe card and removed progress bar
 - Fixed template issue on 'Array Usage' when Home Assistant gets value of unavailable or none

 HKI UnRAID view can be found [here](https://github.com/noodlemctwoodle/homeassistant/blob/master/user_content/views/computers_user_content.yaml)

 #### Credits
 - [Jimz011](https://github.com/jimz011) Thanks for your assistance and ideas on this :)
 - [Stephan](https://github.com/Stephan296) Thanks for creating the version sensor curl request and exploring the correct configuration for the UnRAID-API.
 - [ElectricBrainUK](https://github.com/ElectricBrainUK/UnraidAPI) Thanks for creating this API for us to use and making this dashboard possible
 - [123](https://community.home-assistant.io/u/123/summary) Thanks for solving the problem with parenthesis
 - [Avi](https://github.com/abeksis/My-HomeAssistant-Config) Thanks for creating the awesome graphics used in v1.2 containers swipe-card and also providing code snips. 
 - [OnlyMe](https://github.com/Holewijn/home-assistant-config) Thanks for adding the additional container images


# Home Assistant Monitoring View for HKI

![hassio-monitor](https://github.com/noodlemctwoodle/homeassistant/blob/master/www/images/github/views/ha-core.png)

## Version 0.1 - Initial release (work in progress)

 - Reload, Snapshot, Restart, Reboot buttons added
 - System Temperatures added
 - Added Resources to swipe-card
 - Moved disk usage to resources
 - Added Home Assistant Core Addon support start/stop
 - Moved internet to swipe-card

### Home Assistant Core Addon Support

HKI System view can be found [here](https://github.com/noodlemctwoodle/homeassistant/blob/master/user_content/views/system_user_content.yaml)
     
Configuration instructions can be found [here](https://github.com/noodlemctwoodle/homeassistant/tree/master/configuration/sensors/monitoring/home_assistant)

 #### Credits
 - [SilvrrGIT](https://github.com/SilvrrGIT/HomeAssistant) Excellent post on the community [forum](https://community.home-assistant.io/t/get-notified-of-available-hassio-addon-updates/176626) outlining how to create rest senosr to start/restart Home Assistant Core Addons, Create the switches used in my HKI System view and the post also describes how write automations for addon update available notifications.

# Energy Monitoring View for HKI

![some-pictue](http://someurl.com)

## Version 0.1 - Initial release (work in progress)

 - picture-entity energy-comany
 - Daily usage
 - Monthy usage
 - Daily cost
 - Monthly cost
 - Utility meter [support](https://www.home-assistant.io/integrations/utility_meter/)

Configuration instructions can be found [here](https://github.com/noodlemctwoodle/homeassistant/tree/master/configuration/sensors/monitoring/energy)

