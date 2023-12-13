# agent_modbus

agent_modbus is a plugin for [checkmk](https://checkmk.com/) to poll a tcp modbus system, this is an update to my 1.0 version from 2013 (now adding modbus slave as a third parameter)


## Dependencies
```
apt install g++-multilib pkg-config libmodbus-dev
```

## Build
```
g++ -Wall -I/usr/include/modbus -L/usr/lib/x86_64-linux-gnu agent_modbus.cpp -lmodbus -o agent_modbus
```

## Usage
```
agent_modbus - Vincent Tacquet - 2023 - vincent.tacquet@gmail.com
version 2.0

usage:   agent_modbus <host ip> <host port> <slave> <address:#words(1 or 2):counter|gauge:name> (<address:#words(1 or 2):counter|gauge:name>) ...
example: agent_modbus 192.168.0.1 502 3 856:2:counter:active_energy 790:2:gauge:active_power
```
