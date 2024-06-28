# Optimize your workplace

In order to optimize your workplace we first need to identify which devices consume energy.

You can follow along in this [Google Doc](https://docs.google.com/document/d/1ox6DnssMnVwRgWk5dinfNk1_ZelgBprLPDnB-krPo1M/edit?usp=sharing).

To help you keep inventory you can print the forms available [here (PDF)](./FormDevices.pdf) and [here (docx)](./FormDevices.docx)

In the office the devices may be very different from the lab or even wet lab. Some machines may need to stay on for critical reasons, but not all of them, can you create an inventory with power requirements and power hierarchy ? Are there machines that could be disconnected completely, machines that only need to be turned on when others machiens are on ?

## Compute the power usage and estimate savings with improvements

To help you compute the power usage and estimate savings you can copy this [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1f-pPH4afFR1CoBZoSZHbGGFKfHwLYhsH5GUhhnGVswQ/edit?usp=sharing) and edit it with your devices.

## Disconnect devices from power when not in use

Devices that are turned OFF or in Standby mode still can consume several watts of power, are there opportunities to improve this in your workspace or lab ? There are several convenient ways to disconnect devices when not in use, some pointers are given in the [Google Doc](https://docs.google.com/document/d/1ox6DnssMnVwRgWk5dinfNk1_ZelgBprLPDnB-krPo1M/edit?usp=sharing).

# Activity W1 - Create your workplace inventory

## Quests

* Read the [Google Doc](https://docs.google.com/document/d/1ox6DnssMnVwRgWk5dinfNk1_ZelgBprLPDnB-krPo1M/edit?usp=sharing).
* Fill the [inventory form](./FormDevices.pdf) (can be approximate, or fill blanks later)
* Copy and fill / explore the example [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1f-pPH4afFR1CoBZoSZHbGGFKfHwLYhsH5GUhhnGVswQ/edit?usp=sharing) (the form is *read-only* create a copy to edit)
* Did you expect this much of a difference ?
  <details>
  <summary>Solution</summary>
  I was not expecting my devices to draw so much energy, it is good that we added remote turn-ON of the PCs with wake-on-LAN, so that we can turn them on for remote work instead of leaving them ON 24/24h.

  Also I found out that my screens had a 25W difference based on the brightness setting ! This is huge ! They are however older screens and newer screens draw much less energy. I compared my old EIZOs to my new 4k Samsung and the difference was almost two-fold.

  Adding a primary-secondary plug really makes a difference too, and these devices are not that expensive (or else use a simple switched one). The savings (in KgCO2 and CHF) over the years can easily justify the acquisition of such a device.

  Devices such as keyboards and mice do not really account to much, so we don't really have to take them into account, however keyboards with full LED lighting for each key can still draw a few watts and should not be left ON all the time (e.g., if the computer provides power over USB even when OFF).

  My headphone amplifier takes a lot of energy as well, do I really need it ? No, but this is a luxury choice, don't blame yourself if you don't optimize everything to the max. For example, we sometimes take the car instead of the train for convenience, it happens. The important thing is to think about it and try to do the best without generating extra unnecessary stress or guilt.
  </details>
* What about your workplace or lab ?
  <details>
  <summary>Solution</summary>
  You tell me, are there a lot of machines ? Do some of them need to be ON all the time (incubators, freezers, aquarium filtration), or are there a few that could be switched OFF outside of office hours ? Some devices may have a very long and complex turn-ON procedure and maybe calibration, so they are usually kept ON, but what about all other machines ?
  </details>

## References

- [Home idle load: Devices wasting huge amounts of electricity when not in active use](https://www.nrdc.org/resources/home-idle-load-devices-wasting-huge-amounts-electricity-when-not-active-use)
- [(PDF) Home idle load: Devices wasting huge amounts of electricity when not in active use](https://www.nrdc.org/sites/default/files/home-idle-load-IP.pdf)
- [(PDF) Home idle load self-diagnosis and action guide](https://www.nrdc.org/sites/default/files/home-idle-load-action-guide.pdf)
- [(PDF) Plug-in equipment efficiency: A key strategy to help achieve California's carbon reduction and clean energy goals](https://www.nrdc.org/sites/default/files/home-idle-load-plug-in-efficiency-IB.pdf)

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

# Go back

[Go back to the main section](../README.md)