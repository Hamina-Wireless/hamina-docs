---
description: Learn what Hamina Wireless needs to add access points and antennas.
---

# 📡 Requesting AP's and Antennas

If Hamina Network Planner is missing an access point or antenna, Hamina Wireless can add it for you. We just need to get some information from the AP or antenna vendor.

## Can I add my own AP's and antennas?

The process of adding an access point or antenna to Hamina is pretty technical, specifically requiring our development team to programmatically input the 2D antenna patterns and interpolate them to create 3D patterns for each frequency band.

Unfortunately, this means that you can't add them yourself, but you can email us at **support@hamina.com** with your request.

1. Email support@hamina.com with your request
2. Hamina will contact the vendor to request antenna patterns and specifications
3. The vendor will reply with the antenna patterns and specifications
4. Hamina will process the 2D patterns to create the 3D patterns, and add them to Hamina
5. The new AP's and antennas will be included in the next production push

## What data do you need to add AP's and antennas to Hamina?

**Antenna Patterns** - We need to get antenna patterns from the vendor in a programmatic format such as a spreadsheet or .CSV file. These usually show gain in dBi, per angle (typically every 1° or 5°), and they have a sheet for each antenna element.

{% hint style="warning" %}
While bitmaps are helpful for determining the orientation of the AP/antenna in relation to the antenna patterns, they unfortunately aren't precise enough for use in Hamina. We require antenna patterns in a programmatic format such as a spreadsheet or .CSV file.
{% endhint %}

**Specifications** - We need to get the specifications of the AP or antenna. Usually, everything we need is on the data sheet, but here's a complete list:

* AP model number
* Supported frequency bands (2.4, 5, 6 GHz)
* Supported Phy type in each band (802.11ac, 802.11ax)
* Amount of spatial streams per band
* Max PoE consumption
* Default mounting orientation (Ceiling or wall)
* Peak gain for each antenna
* Is the AP intended for indoors, or outdoors?
* Is the AP omnidirectional, or directional?
* Is there a Bluetooth Low Energy radio present?
* Is there a ZigBee radio present?

