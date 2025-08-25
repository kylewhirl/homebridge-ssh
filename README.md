homebridge-ssh
==============

Supports triggering ssh commands on the HomeBridge platform.

## Installation

1. Install homebridge using: `npm install -g homebridge`
2. Install this plugin using: `npm install -g homebridge-ssh`
3. Update your configuration file. See `sample-config.json` in this repository for a sample.

## Configuration

This plugin can be configured using the [Homebridge UI](https://github.com/homebridge/homebridge-config-ui-x). It exposes a configuration schema so the above settings can be entered through the graphical interface.

Configuration sample:

```
"accessories": [
	{
              "accessory": "SSH",
              "name": "iTunes Music",
              "on": "osascript -e 'tell application \"iTunes\" to play'",
              "off": "osascript -e 'tell application \"iTunes\" to stop'",
              "state": "osascript -e 'tell application \"iTunes\" to get player state'",
              "on_value" : "playing",
              "exact_match": true,
              "ssh": {
                "user": "me",
                "host": "mymac",
                "port": 22,
                "password": "password (or use key)",
                "key": "path to private key file"
              }
	}
]
```
