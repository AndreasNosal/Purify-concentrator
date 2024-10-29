# Starter-Friendly Electrical Project for DIY Assembly

### Contributors: 
- **Filip Greguš**
- **Andreas Nosál**

### Project:
- **Commissioned by**: Young Energy Europe AHK Slowakei
- **Date**: 29 October 2024
- **License**: [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.html)
- **Programming language**: micropython
- **Microcontroller**: ESP32 Wemos D1 mini - WROOM-32

## Hardware Components

1. **ESP32 microcontroller**: Main control unit for executing code and handling inputs/outputs.
2. **BME680 Sensor**: Measures temperature, pressure, humidity, and gas levels.
3. **SSD1306 OLED Display**: Displays real-time data.
4. **Battery and Power Monitoring**: Tracks battery voltage and alerts on low charge.
5. **LEDs and Buzzer**: Provides visual and audio notifications based on sensor data.

---

## Code Explanation and Main Functionalities

- **Sensor Initialization**: Initializes the I2C connection with the BME680 sensor and OLED display.
- **Environmental Data Processing**: Reads temperature, pressure, humidity, and gas data from the sensor and calculates an Indoor Air Quality (IAQ) index.
- **Battery Monitoring**: Reads and computes the battery percentage based on ADC voltage input.
- **LED & Buzzer Notifications**: LED colors indicate air quality levels, while the buzzer sounds when IAQ exceeds safe thresholds.
- **Display Control**: Cycles through different display modes showing temperature, humidity, pressure, and battery status.
- **Data Storage**: Saves IAQ, gas levels, uptime, and other data to RTC memory for persistence after restarts.
- **Data Persistence**: Saves readings to RTC memory for recovery after power loss or restart.
- **Deep Sleep Mode**: Activates deep sleep during idle times to conserve battery.
