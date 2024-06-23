# Optimize your workplace

In order to optimize your workplace we first need to identify which devices consume energy.

You can follow along in this [Google Doc](https://docs.google.com/document/d/1ox6DnssMnVwRgWk5dinfNk1_ZelgBprLPDnB-krPo1M/edit?usp=sharing).

To help you keep inventory you can print the forms available [here (PDF)](./FormDevices.pdf) and [here (docx)](./FormDevices.docx)

In the office the devices may be very different from the lab or even wet lab. Some machines may need to stay on for critical reasons, but not all of them, can you create an inventory with power requirements and power hierarchy ? Are there machines that could be disconnected completely, machines that only need to be turned on when others machiens are on ?

## Disconnect devices from power when not in use

Devices that are turned OFF or in Standby mode still can consume several watts of power, are there opportunities to improve this in your workspace or lab ? There are several convenient ways to disconnect devices when not in use, some pointers are given in the [Google Doc](https://docs.google.com/document/d/1ox6DnssMnVwRgWk5dinfNk1_ZelgBprLPDnB-krPo1M/edit?usp=sharing).

# Wake on Lan (WoL)

WoL is an Ethernet standard that allows a computer to be turned on or awakened from sleep mode by a network message. WoL also works if the computer is turned off (the computer must have power).

WoL support is implemented on the motherboard of a computed and in the network interface controller. It does not depend on the OS (Windows, Linux, MacOS). In order to get WoL to work the feature must be enabled, this can often be done through the motherboard BIOS settings, and sometimes requires an utility and drivers (e.g., when the network card is not on the motherboard).

In order to turn on computers in the office or in a lab a low-powered single board computer (SBC) can be used, for example a Raspberry PI, the idea is that the low-powered device is on all the time and users turn on their computers through a web interface provided by the SBC.

![webUI](https://github.com/sameerdhoot/wolweb/raw/main/wolweb_ui.png)

This allows to turn on any computer in the office or lab for remote desktop or secure shell (SSH) access.

Once the remote work is done (at the end of the day), the computer can be turned off through remote desktop or SSH.

This avoids having the PCs in the office or lab to be on all the time.

## References

- https://en.wikipedia.org/wiki/Wake-on-LAN
- https://github.com/sameerdhoot/wolweb