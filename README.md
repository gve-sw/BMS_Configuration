# BMS_Configuration
To bind the multiple switches with VLan for bms automation

## Contacts
* Raveesh V

## Solution Components
*  Python
*  Paramiko
*  CSV

## Python Setup
```shell script
# create virtual environment
python3 -m venv venv

#activate virtual environment
source venv/bin/activate

#install dependent modules
pip install -r requirements.txt
```

## Configuration
>Modify **switches.csv** and **network.csv** with required details

```python
switches.csv
switch,hostname,port,username,password
s1,<hostname/IP>,22,<username>,<password>

network.csv
switch,vlanid,ipaddress,mac,interface
s1,x,<x.x.x.x>,xxxx.xxxx.xxx,xxx/x/1

```

## Usage

>Execute the following command to start the script

    $ python apply_configuration.py -c network.csv -d switches.csv

use ``` --revert```flag to unbind the configuration 

### LICENSE

Provided under Cisco Sample Code License, for details see [LICENSE](LICENSE.md)

### CODE_OF_CONDUCT

Our code of conduct is available [here](CODE_OF_CONDUCT.md)

### CONTRIBUTING

See our contributing guidelines [here](CONTRIBUTING.md)

#### DISCLAIMER:
<b>Please note:</b> This script is meant for demo purposes only. All tools/ scripts in this repo are released for use "AS IS" without any warranties of any kind, including, but not limited to their installation, use, or performance. Any use of these scripts and tools is at your own risk. There is no guarantee that they have been through thorough testing in a comparable environment and we are not responsible for any damage or data loss incurred with their use.

You are responsible for reviewing and testing any scripts you run thoroughly before use in any non-testing environment.
