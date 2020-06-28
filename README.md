# smart-home-config

This repository holds the configuration of various smart devices in my house

# first run setup.sh to install git hooks
to avoid committing open-text passwords

## ESPHome config holds wifi passwords in the open form, please don't commit them, just leave an empty string

### ESPHome
1. Clone the repository from https://github.com/esphome/esphome
2. Make sure you have Python 3.x in your path
```
python --version
```
3. Install esphome in development mode
```
python setup.py develop
```
4. Clone this repository
5. Make sure that can connect to your ESP32
```
python esphome <path to esphome config file> logs
```
6. (Necessary if you use the USB cable) Install UART COM drivers from here https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers
7. Update the WiFi password in the yaml config file
8. Upload and the configured firmware
```
python esphome <path to esphome config file> run
```
9. Observe logs to make sure everything works fine
