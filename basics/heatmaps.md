---
description: >-
  Learn how to use all of Hamina's heatmaps, and how to change them to match
  your network requirements.
---

# 🔥 Heatmaps

## Selecting Heatmaps

You can access heatmap options by clicking on the **Heatmaps** drop-down menu at the top of Hamina. You can choose the **Technology**, **Heatmap**, and **Band** (for Wi-Fi). The **Adjust requirements** link at the bottom opens the **Adjust Requirements pane**.

<div align="left">

<figure><img src="../.gitbook/assets/heatmap-menu.png" alt=""><figcaption></figcaption></figure>

</div>

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

<div align="left">

<figure><img src="../.gitbook/assets/heatmap-settings.png" alt=""><figcaption></figcaption></figure>

</div>

### Heatmap Thresholds

To divide the heatmaps into multiple colors, Hamina Network Planner uses configurable thresholds. By default, there are three thresholds which divide the heatmap into colors, which have labels.

<div align="left">

<figure><img src="../.gitbook/assets/heatmap-thresholds.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

The labels can be renamed in the column on the left, and the thresholds can be changed and deleted using the column on the right. Click the **Add a threshold** button on the bottom to add thresholds back in. The maximum amount of thresholds is three, and the minimum is one.

{% hint style="info" %}
It is best practice to design wireless networks to meet a set of requirements, such as -65 dBm of coverage, or better. Using the Hamina default labels as an example: **High** (-65 dBm or better) is usually considered a Pass, while everything below -65 dBm (**Decent**, **Low**, and **Edge**) is considered a Fail.
{% endhint %}

### Heatmap Settings

<div align="left">

<figure><img src="../.gitbook/assets/adjust-requirements.png" alt="" width="563"><figcaption></figcaption></figure>

</div>

#### **Global Heatmap Settings**

* **Opacity** - Adjusts the opacity of the heatmap, which can be adjusted lower to make the map underneath the heatmap easier to see, or adjusted higher to make the heatmap easier to see.
* **Client height** - Adjusts the height of the client devices in the network simulation. By default, Hamina Network Planner simulates a client that is 1 meter off the ground (which is the average height of a client in a user's hand, or on a desk).

#### Fast ray tracing settings

* **Simulated diffraction and reflection effects** (Hamina Planner Plus only) - Adjusts the intensity of Fast Ray Tracing effects. For more information, see  [#fast-ray-tracing](heatmaps.md#fast-ray-tracing "mention").

#### Other settings

* **Display heatmap at client height** (3D only) - In 3D mode, by default, Hamina Network Planner places the heatmap on the floor. Enabling this option causes the heatmap to hover off the floor at the height of the client, which may be useful for visualization purposes. This option is only available in 3D.
* **Full Building Propagation (Beta)** - Without this option enabled, Hamina Network Planner only calculates propagation for the current floor, and the floors above and below the current floor. This usually provides a good balance of speed and accuracy, as most buildings don't see significant signal propagation beyond one floor in either vertical direction. With this option enabled, signal propagation is calculated across all floors in the building, which can be useful for multi-floor atriums, theaters, and stadiums.&#x20;

{% hint style="warning" %}
In some environments, enabling Full building propagation may cause significant performance problems. Enable it with care, and disable if needed.
{% endhint %}

* **List all APs on mouseover** - By default, the Legend only shows the loudest AP on most heatmaps. With this option enabled, all access points will be listed on mouseover.
* **Auto-select prediction input** - By default, Hamina chooses which model to use for prediction: **Walls + objects**, **environment type**, or **environment learning**. By disabling this option, you can manually choose which model Hamina should use in both the **Simulation tab** and **Live tab**.&#x20;

{% hint style="info" %}
The Live View is currently available as a <mark style="color:red;">**Feature Preview**</mark> for Hamina Network Planner Plus subscribers. [See the release notes](https://docs.hamina.com/planner/other/release-notes#id-2024-06-18) for more information about the Feature Preview.
{% endhint %}

## **Heatmap Calculations**

Hamina Network Planner keeps planning fast, smooth and responsive by calculating heatmaps in stages. The first stage is a relatively low-resolution heatmap, so you get instant (or near-instant) results. Then, Hamina Network Planner opportunistically calculates successively higher-resolution heatmaps until it was reached the maximum resolution for the browser window.

Lower-resolution stages can produce two side effects:

* Blocky and less-detailed heatmaps
* "Holes" in coverage areas such as warehouse aisles

In most cases, these side effects either don't appear, or simply don't matter. In some cases (such as with warehouse aisles), it is necessary to let Hamina Network Planner calculate higher-resolution heatmaps (by simply letting Hamina sit idle for a moment, so it can complete the calculations).

<div align="left">

<figure><img src="../.gitbook/assets/heatmaps-calculating.gif" alt="" width="563"><figcaption><p>In this example, you can see the stages of heatmap calculation. When all APs are selected, notice that the second stage (when the progress bar is about 1/8th complete) is already high-enough resolution for analysis.</p></figcaption></figure>

</div>

### Heatmap Progress Bar

The progress of this calculation is represented with a blue **Heatmap Progress Bar** along the top of Hamina Network Planner. The progress bar will disappear when the maximum resolution heatmap is completed. It will also reset whenever the calculations start over, for example by changing the viewport or modifying the predictive model (in other words, modifying walls, attenuating objects, or access points).

<figure><img src="../.gitbook/assets/progress-bar.gif" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
In almost all cases, _you don't need to wait for the Heatmap Progress Bar to finish_. In most projects, the first couple of stages will give you plenty of resolution to make decisions, and potentially move on to the next design task.
{% endhint %}

The calculation is optimized for the **current viewport**, which is the part of the map that is currently visible in Hamina Network Planner. The viewport changes as you pan and zoom around the project.

Hamina Network Planner will reset heatmap calculations whenever the viewport changes (e.g., by panning and zooming), or whenever the predictive model changes (e.g. by moving an access point or placing a wall). Heatmap calculation is automatically reset and started, so you don't have to think about it - just plan, and we'll take care of the heatmaps for you.

{% hint style="info" %}
If you'd like to quickly get a high-resolution heatmap for a specific area, zoom in on it.
{% endhint %}

## **Fast Ray Tracing**

Hamina Network Planner Plus includes the option to calculate heatmaps with Fast Ray Tracing, which simulate the effects of diffraction and refraction.

Since FRT (Fast Ray Tracing) heatmaps can take more time to calculate, the heatmap calculation is manually triggered by clicking the **Compute FRT heatmap** button directly underneath the **Camera** and **Layer** controls on the right of the map view.

<div align="left">

<figure><img src="../.gitbook/assets/fast-ray-tracing-button.png" alt="" width="563"><figcaption></figcaption></figure>

</div>

To disable the FRT heatmap, click the **Compute FRT heatmap** button again.

<div align="left">

<figure><img src="../.gitbook/assets/fast-ray-tracing.gif" alt="" width="360"><figcaption></figcaption></figure>

</div>

### Adjusting Diffraction and Refraction Effects

The intensity of simulated diffraction and refraction effects can be adjusted to simulate more or less reflective environments using the **Simulated diffraction and reflection effects** slider.

The slider is located in the [**Adjust Requirements pane**](heatmaps.md#heatmap-settings), under **Show more**.

<div align="left">

<figure><img src="../.gitbook/assets/diffraction-and-refraction-effects.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

We recommend starting with setting `3`, comparing with measurements in the environment (such as a full site survey, or spot-checks from a client device), and adjusting it up or down until the reflectivity more closely matches the real-world measurement.
