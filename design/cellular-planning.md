---
description: Learn about Hamina's private cellular planning capabilities.
---

# 📶 Private Cellular Planning

With a Hamina Network Planner Plus subscription, Hamina's private cellular network planning capabilities are unlocked. This grants the ability to view cellular heatmaps, place private cellular base stations, and configure frequency use settings.

## Spectrum Use Configuration

To configure cellular spectrum use, click on any eNodeB. In the **Edit Access Points** pane on the left, click the Show more expander. Under **Auto-Channel Assignment**, click the **here** link to open the **Channel Settings** window.

![](<../.gitbook/assets/Spectrum Use Configuration.png>)

In the Channel Settings window, you can configure:

* Frequency Band
* Frequency Reuse
  * Per Base Station Channel Width
  * Number of Available Channels
  * Subcarrier Spacing for 5G

### Supported Bands

Hamina supports the following bands:

* 450-465 MHz (Band 73 TDD)
* 703-803 MHz (Band 28 FDD)
* 791-862 MHz (Band 20 FDD)
* 824-894 MHz (Band 5 FDD)
* 1.71-188 GHz (Band 3 FDD)
* 1.85-1.99 GHz (Band 2 FDD)
* 1.88-19.2 GHz (Band 39 TDD)
* 1.92-2.17 GHz (Band 1 FDD)
* 2.5-2.68 GHz (Band 7 FDD)
* 2.3-2.4 GHz (Band 40 TDD)
* 2.57-2.62 GHz (Band 38 TDD)
* 3.4-3.6 GHz (Band B42 TDD)
* 3.55-3.7 GHz (Band 48 TDD)
* 3.6-3.8 GHz (Band B43 TDD)
* 3.3-3.8 GHz (Band n78 TDD)
* 3.3-4.2 GHz (Band n77 TDD)
* 5.15-5.925 GHz (Band 46 TDD)

{% hint style="info" %}
Check the data sheet for your desired base station hardware for band support specifications. Hamina does not factor in base station band support specifications.
{% endhint %}

## Base Station Configuration

Just like with Wi-Fi access points, Hamina supports the selection of eNodeB vendor selection, model selection, and external antenna selection (if supported by the eNodeB).&#x20;

Antenna patterns for accurately modeled in 3D for all eNodeBs with internal antennas, and for all external antennas.

![](../.gitbook/assets/cellular\_antenna\_model.png)

For eNodeB base stations that support external antennas, Hamina support specifying the mounting type and down tilt of the antenna in degrees. Transmit power at the radio is configurable, and the EIRP is calculated for the antenna.

### Mounting, Height, and Downtilt

Also like Wi-Fi access points in Hamina, the height, downtilt are fully configurable, and all signal propagation calculations are calculated in 3D.

## 4G/5G Heatmaps

Hamina supports the following heatmaps for private cellular planning:

* Max RSRP
* Secondary RSRP
* Teriary RSRP
* SINR

In the Heatmap dropdown, the settings for each heatmap type can be edited by clicking the **Adjust requirements** link.

![](../.gitbook/assets/cellular\_heatmaps.png)

For Max RSRP, Secondary RSRP, Tertiary RSRP, and SINR, you can adjust:

* **Opacity**: The opacity of the heatmap. A lower percentage makes the background map easier to see.
* **Client height**: The height height that the client device is modeled at, and this the vertical slice that is represented in the heatmap
* **Client device**: The cellular client type, which changes the amount of spatial streams and generation of cellular technology.

For SINR only, the **Cell average load %** is also adjustable.

![](../.gitbook/assets/sinr\_requirements.png)

### Per-Frequency Signal Propagation

When planning private cellular networks, Hamina Network Planner Plus models RF propagation on a per-frequency basis. In other words, it models the propogation based on the selected frequency of each radio unit. A radio unit using a lower frequency in the band will propagate better than a radio unit using a higher frequency in the band.

