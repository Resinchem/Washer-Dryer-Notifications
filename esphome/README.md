## ESPHome Configurations
These files are the ESPHome YAML configurations I used for my dryer cycle start and dryer cycle end sensors.  They are based on using a Wemos D1 Mini and the GY-302 breakout board with a BH1750 Illuminance sensor.

### Recommended Use:

While the entire ESPHome YAML is included, the recommended use is to create a new node in your ESPHome instance with the basic info (board type, wifi, etc.). After this is created, edit and then copy/paste the info starting with the 'i2c' line and the remaining sensors into your new file, modifying entity names as desired.

_Please see the video or written guides listed on the main page for more info on use and how these configuratios work._
