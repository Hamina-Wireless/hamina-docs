---
description: >-
  Learn how to use all of Hamina's heatmaps, and how to change them to match
  your network requirements.
---

# 🔥 Heatmaps

## Selecting Heatmaps

Access heatmap options by clicking on the **Heatmap** drop-down menu at the top of Hamina. You can choose the **Technology**, **Heatmap**, and **Band** (for Wi-Fi). The **Adjust requirements** link at the bottom opens the **Adjust Requirements pane**.

<figure><img src="../.gitbook/assets/heatmap_menu.png" alt="" width="563"><figcaption></figcaption></figure>

### Heatmaps

#### Wi-Fi

* **Coverage**: Shows signal strength from the loudest access point.
* **Secondary coverage**: Shows signal strength from the second loudest access point, which helps ensure that there are always at least two access points above a certain signal strength threshold. Important for redundancy and smooth roaming performance.
* **Tertiary coverage**: Shows signal strength from the third loudest access point, which helps ensure that there are always at least three access points above a certain signal strength threshold. Primary used for Wi-Fi-based real-time location services.
* **SNR**: The Signal-to-noise Ratio shows how much signal strength there is above the noise floor.
* **Interference**: Shows how many access points are audible on the same channel from a given location.
* **Data rate**: Shows the theoretical maximum data rate available, based on on the SNR.

#### 4G/5G

* **Max RSRP**: Shows the signal strength from the loudest cellular base station, in RSRP (Reference Signal Received Power).
* **Secondary RSRP**: Shows the signal strength from the second loudest base station.
* **Tertiary RSRP**: Shows the signal strength from the third loudest base station.
* **SINR**: Shows the signal quality in SINR (Signal to Interference & Noise Ratio).
* **Downlink throughput**: Shows the expected throughput on the downlink, that is from the base station to the client device.

#### BLE

* **Coverage**: Shows signal strength from the loudest BLE-enabled access point or BLE beacon.
* **Secondary Coverage**: Shows signal strength from the second loudest BLE-enabled access point or BLE beacon.
* **Tertiary Coverage**: Shows signal strength from the third loudest BLE-enabled access point or BLE beacon.

## Adjusting Requirements

With any Technology and Heatmap selected, click the **Adjust requirements** link, or click on the **Heatmap Legend** in the lower left, which will open the **Adjust requirements pane** on the right.

<figure><img src="../.gitbook/assets/show_requirements_pane.png" alt="" width="563"><figcaption></figcaption></figure>

### Heatmap Thresholds

To divide the heatmaps into multiple colors, Hamina Network Planner uses configurable thresholds. By default, there are three thresholds which divide the heatmap into colors, which have labels.

<figure><img src="../.gitbook/assets/thresholds (1).png" alt="" width="295"><figcaption></figcaption></figure>

The labels can be renamed in the column on the left, and the thresholds can be changed and deleted using the column on the right. Click the **Add a threshold** button on the bottom to add thresholds back in. The maximum amount of thresholds is three, and the minimum is one.

{% hint style="info" %}
It is best practice to design wireless networks to meet a set of requirements, such as -65 dBm of coverage, or better. Using the Hamina default labels as an example: **High** (-65 dBm or better) is usually considered a Pass, while everything below -65 dBm (**Decent**, **Low**, and **Edge**) is considered a Fail.
{% endhint %}

### Global Heatmap Settings

<figure><img src="../.gitbook/assets/adjust_requirements_pane.png" alt="" width="295"><figcaption></figcaption></figure>

* **Opacity** - Adjusts the opacity of the heatmap, which can be adjusted lower to make the map underneath the heatmap easier to see, or adjusted higher to make the heatmap easier to see.
* **Client height** - Adjusts the height of the client devices in the network simulation. By default, Hamina Network Planner simulates a client that is 1 meter off the ground (which is the average height of a client in a user's hand, or on a desk).
* **Display heatmap at client height** (3D only) - In 3D mode, by default, Hamina Network Planner places the heatmap on the floor. Enabling this option causes the heatmap to hover off the floor at the height of the client, which may be useful for visualization purposes. This option is only available in 3D.
* **Full Building Propagation (Beta)** - Without this option enabled, Hamina Network Planner only calculates propagation for the current floor, and the floors above and below the current floor. This usually provides a good balance of speed and accuracy, as most buildings don't see significant signal propagation beyond one floor in either vertical direction. With this option enabled, signal propagation is calculated across all floors in the building, which can be useful for multi-floor atriums, theaters, and stadiums.&#x20;

{% hint style="warning" %}
In some environments, enabling Full building propagation may cause significant performance problems. Enable it with care, and disable if needed.
{% endhint %}
