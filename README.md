# lanpresence
SmartThings Edge driver for http control of presence device

Example use case:  phone tracking or ping device tracking

### Dependency
[edgebridge server](https://github.com/toddaustin07/edgebridge) running on a local computer

### Installation
Available for install to SmartThings hub via my [shared projects channel](https://bestow-regional.api.smartthings.com/invite/d429RZv8m9lo).

## Usage

### Device Settings
LAN Device Name - a unique device name; simple/short text only
LAN Device Address - IP and port address of the application that will be sending updates.  port is optional  (e.g. '192.168.1.104' or '192.168.1.104:50001')
Bridge Address - IP and port address of the edgebridge server (e.g. '192.168.1.140:8088')

### Application message format
Example http message:
POST http://192.168.1.140:8088/devname/presence/present
POST http://192.168.1.140:8088/devname/presence/notpresent

where '192.168.1.140:8088' is address of edgebridge server, 'devname' is device name as configured in *LAN Device Name*
