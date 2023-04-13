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

* Band 73 TDD
* Band 28 FDD
* Band 20 FDD
* Band 5 FDD
* Band 3 FDD
* Band 2 FDD
* Band 39 TDD
* Band 1 FDD
* Band 7 FDD
* Band 40 TDD
* Band 38 TDD
* Band B42 TDD
* Band 48 TDD
* Band B43 TDD
* Band n78 TDD
* Band n77 TDD
* Band 46 TDD

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



