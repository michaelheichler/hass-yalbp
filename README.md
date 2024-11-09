# Yet Another Smart Light Automation 🌞💡 

[![Import Blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/michaelheichler/hass-yalbp/refs/heads/main/hass-yalbp.yaml)

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)  

**Version:** 1.0.3  
**Source URL:** [GitHub Repository](https://github.com/michaelheichler/hass-yalbp)

This blueprint provides intelligent control of your lights based on presence or motion detection. It follows the **KISS Principle** (Keep It Simple, Stupid) to ensure a straightforward, minimalistic design for seamless integration and ease of use. Customize it with optional lux sensors, adaptive lighting, and a Do Not Disturb (DND) period to ensure your lights operate precisely when needed. Enhanced with error handling for DND time parsing so invalid inputs can be handled with grace.

---

## Features
- 🚶 **Presence/Motion Detection:** Automatically turn lights on/off based on motion or presence sensors.
- 🌞 **Lux Sensor Integration:** Adjust light activation based on ambient brightness.
- 🌈 **Adaptive Lighting (Optional):** Seamless integration with the Adaptive Lighting integration for brightness and color adjustments.
- ☀️ **Sun Condition:** Automatically adjust lights based on the sun's position.
- ⏲️ **Customizable Light Timeout:** Set how long lights stay on after no motion is detected.
- 🚫💤 **Do Not Disturb (DND) Mode:** Prevent lights from turning on during specified times.

---

## Requirements
1. **Presence/Motion Sensors** (e.g., Aqara Motion Sensor, Hue Motion Sensor)
2. **Light Group** (e.g., a group of smart bulbs)
3. **Optional:**
   - Lux Sensor (e.g., Hue Outdoor Sensor)
   - Adaptive Lighting Switch (e.g., Home Assistant's Adaptive Lighting integration)

---

## Inputs
| Name                  | Description                                                                 | Default      | Required |
|-----------------------|-----------------------------------------------------------------------------|--------------|----------|
| **Presence Sensors**  | Select the presence or motion sensors to trigger the lights.               | -            | Yes      |
| **Light Group**       | Choose the light group to control.                                         | -            | Yes      |
| **Adaptive Lighting** | Optional: Enable adaptive lighting for brightness and color adjustments.   | ""           | No       |
| **Lux Sensor**        | Optional: Use a lux sensor to adjust light activation based on brightness. | ""           | No       |
| **Lux Threshold**     | Set the brightness level to activate lights when using a lux sensor.       | 50 lx        | No       |
| **Sun Condition**     | Enable sun-based conditions for light activation.                         | True         | No       |
| **Light Timeout**     | Set how long the lights stay on after no motion is detected.               | 15 seconds   | No       |
| **DND Toggle**        | Enable or disable Do Not Disturb mode.                                     | False        | No       |
| **DND Start Time**    | Set the start time for Do Not Disturb.                                     | ""           | No       |
| **DND End Time**      | Set the end time for Do Not Disturb.                                       | ""           | No       |
| **Transition Duration** | Set the duration for light transitions (e.g., dimming).                   | 2 seconds    | No       |

---

## Example Use Case
- Automatically turn on lights when motion is detected in a room.
- Use a lux sensor to ensure lights only activate if the ambient light is below a threshold.
- Prevent lights from turning on during the night (e.g., 22:00 to 6:00) using DND mode.

---

## Blueprint Code
This blueprint code can be imported directly into Home Assistant.  
View the full code [here](https://github.com/michaelheichler/hass-yalbp).

---

## Installation
1. Click on the big blue button at the top of this page. :)

---

## Notes
- Ensure all required entities are configured in Home Assistant before using this blueprint.
- If using the Adaptive Lighting integration, ensure it's installed and properly set up.

---

## Troubleshooting
- **DND Time Parsing:** This blueprint includes improved error handling for invalid DND time formats.
- Check the **Logbook** for debugging messages if the automation does not behave as expected.

---

### License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
