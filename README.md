# ESPHome
Configurations for my ESPHome devices

## Shelly Plus 1:
### Note for setup:
New Shelly devices need to be configured in Home Assistant to allow them to make calls to Home Assistant.  See this forum message [here](https://community.home-assistant.io/t/home-assistant-rejecting-a-esphome-homeassistant-service/604085).

### YAML Configurations
  - [Shelly device housed behind a toggle switch and used with a smart light](https://github.com/shaftspanner/esphome/tree/main/shelly_plus_1_with_smart_light)
    - Checks whether Shelly is connected to the Home Assistant API and switches the light on or off accordingly using either the Home Assistant API or the Shelly relay
    - This is a pretty complicated configuration but it covers just about all of the options whilst allowing for the case where Home Assistant isn't availble, but trying to make best use of the features of the smart bulb
  - [Shelly device housed behind a toggle switch using a standard (dumb) bulb](https://github.com/shaftspanner/esphome/tree/main/shelly_plus_1_toggle)
    - I use this configuration for most of my Shelly devices - anything that doesn't use a dumb bulb.  Note that it retains up = off, down = on - standard for UK light switches
  - [Localbytes UK/EU smart plug with power monitoring](https://github.com/shaftspanner/esphome/blob/main/localbytes_uk_plug_standard)
    - Localbytes sell a brilliant UK/EU smart plug that comes pre-loaded with either Tasmota or ESPHome.  It's available here: [www.mylocalbytes.com](https://www.mylocalbytes.com/products/smart-plug-pm)
    - This configuration is draws of the stock configuration supplied by Localbytes but moves the API Encryption Key to the secrets.yaml file, and fixes the IP address.
    - *Note:* I use this with the UK plug - I haven't tested it with anything else!
