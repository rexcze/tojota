# Library for handling Toyota vehicle API

Unofficial python functions for handling data from Toyota Connected services APIs.

# Installation

- Have Python 3.6+
- Create virtual environment
- Install requirements `pip install -r requirements.txt`

# Usage

- Configure your MyT user account, password and vehicle VIN into `configs/myt.json`. Example:

  ```
  {
    "username": "john@doe.com",
    "password": "P@ssw0rd",
    "vin": "JTMDW3FV50D123456",
    "timezone": "Europe/Helsinki",
    "use_remote_control": true,
    "use_influxdb": false,
    "is_electric": false
  }
  ```
- If your vehicle doesn't support remote control functions, set `"use_remote_control": false` in the config file
- If your vehicle is not EV (or does not charge), set `"is_electric": false` in the config file
- If you would like to save data to InfluxDB, install InfluxDB ( https://www.influxdata.com/ ) and create database
  'tojota' and set "use_influxdb": true in the config file (support only for old unsecure no authentication version)
- Run `python tojota.py` to fetch, save and print data
- Data is saved to cache directory for further usage

