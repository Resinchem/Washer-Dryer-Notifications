## Home Assistant Automations and Entities
The Washer and Dryer files provided here are Home Assistant Package files.  A package file contains all the entities, helpers, automations and scripts related to a project or device in a single YAML file.  Unless you have implemented packages in your Home Assistant instance, **_you cannot just copy/paste or import these packages into Home Assistant!_**  This will not work. Even if using packages, you may need to edit entity names or other details for your particular install.

If you are not using packages, then each 'domain' or top level entity type must be split out of the package and placed in the proper location.  For example, input_text entities listed in the package, must be moved or placed under your input_text section of the configuration.yaml (or in your input_text file if using split configuration).  Automations must be moved to your automation section (or recreated using the UI editor), etc.

**Note**: While these packages are YAML, you can create all the helpers and automations in Home Assistant using the UI editor instead of YAML.  The [written guide](https://resinchemtech.blogspot.com/2024/01/washer-dryer-updated.html) shows a few examples but if you need further assistance on how to take a YAML file and recreate it using the UI, you can watch this video: [Home Assistant 101: Recreate a YAML automation using the UI Automation Editor](https://youtu.be/F3YjWCs7Czc)

### Recommended Use:

The washer package utlizes an energy-monitoring smart plug to report real time wattage use from the washer.  While my particular project uses a Sonoff S31 with Tasmota, any smart plug that integrates into Home Assistant (native or cloud based) should work.  The package does not include any integration details (such as manual MQTT integration), but assumes you have an integrated smart plug with watts being reported.  Change the entity names in the package as necessary.

The dryer package uses a DIY built light level sensor to detect indicator lights on the front panel of the dryer to determine when the cycle starts and ends.  This sensor utilizes ESPHome and the code/configuration for these sensors can be found in the /esphome folder.  This could likely be adapted to other uses, like a dishawaher, or other appliances/devices that using indicator lights to display a cycle or state.

While it may be possible to copy/paste sections of my examples into your Home Assistant, the primary purpose is to proivde my version as a reference for creating your own versions. 

_Please see the video or written guides listed on the main page for more info on use and how these configurations work._
