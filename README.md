MAC Address Changer

This Python script allows you to change the MAC address of a network interface on Unix-like operating systems. The script is useful for privacy, testing, or troubleshooting network issues.

Features

Fetches the current MAC address of the specified interface.

Allows you to set a new MAC address.

Validates the MAC address change.

Provides clear error messages for invalid input or failures.

Prerequisites

Python 3.x

Root privileges (required for modifying network settings).

ifconfig command available (usually included in net-tools).

Installation

Clone or download this repository.

Ensure the script is executable:

chmod +x mac_changer.py

Install necessary Python packages (if not already installed):

pip install argparse

Usage

Run the script with the following command:

python3 mac_changer.py -i <interface> -m <new_mac>

Example

To change the MAC address of the interface eth0 to 00:11:22:33:44:55:

python3 mac_changer.py -i eth0 -m 00:11:22:33:44:55

Options

-i, --interface (required): Specify the network interface to modify.

-m, --mac (required): Provide the new MAC address in the format XX:XX:XX:XX:XX:XX.

Script Output

Current MAC:
The script fetches and displays the current MAC address of the specified interface.

Changing MAC:
Indicates the attempt to change the MAC address.

Result:
Confirms whether the MAC address was successfully changed or not.

Troubleshooting

Permission Denied:
Run the script as a superuser:

sudo python3 mac_changer.py -i <interface> -m <new_mac>

Invalid MAC Address:
Ensure the MAC address is in the correct format: XX:XX:XX:XX:XX:XX where X is a hexadecimal character (0-9, A-F).

ifconfig Command Not Found:
Install net-tools on your system:

sudo apt install net-tools  # For Debian/Ubuntu systems

Notes

Always test the script in a safe environment before using it on critical systems.

Changing the MAC address may temporarily disrupt network connectivity.

