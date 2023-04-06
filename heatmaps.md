---
description: >-
  Learn how to use all of Hamina's heatmaps, and how to change them to match
  your network requirements.
---

# 🔥 Heatmaps

## Managing Heatmaps

Access heatmap options by clicking on the **Heatmap** drop-down menu at the top of Hamina. You can choose the **Technology**, **Heatmap**, and **Band** (for Wi-Fi).

## Heatmaps

### Wi-Fi

* **Coverage**: Shows signal strength from the loudest access point.
* **Secondary coverage**: Shows signal strength from the second loudest access point, which helps ensure that there are always at least two access points above a certain signal strength threshold. Important for redundancy and smooth roaming performance.
* **Tertiary coverage**: Shows signal strength from the third loudest access point, which helps ensure that there are always at least three access points above a certain signal strength threshold. Primary used for Wi-Fi-based real-time location services.
* **SNR**: The Signal-to-noise Ratio shows how much signal strength there is above the noise floor.
* **Interference**: Shows how many access points are audible on the same channel above -82 dBm, which is also the threshold that trips Carrier Sense when a radio is performing a Clear Channel Assessment. You can learn more about Clear Channel Assessments in [CWNP - 802.11 Arbitration (Page 9)](https://www.cwnp.com/uploads/802-11\_arbitration.pdf).
* **Data rate**: Shows the theoretical maximum data rate available, based on on the SNR.

## 4G/5G

* **Max RSRP**: Shows the signal strength from the loudest celllar base station, in RSRP (Reference Signal Received Power).
* **Secondary RSRP**: Shows the signal strength from the second loudest base station.
* **Tertiary RSRP**: Shows the signal strength from the third loudest base station.
* **SINR**: Shows the signal quality in SINR (Signal to Interference & Noise Ratio).
* **Downlink throughput**: Shows the expected throughput on the downlink, that is from the base station to the client device.

## BLE

* **Coverage**: Shows signal strength from the loudest BLE-enabled access point or BLE beacon.
* **Secondary Coverage**: Shows signal strength from the second loudest BLE-enabled access point or BLE beacon.
* **Tertiary Coverage**: Shows signal strength from the third loudest BLE-enabled access point or BLE beacon.

## Adjusting Requirements

With any Technology and Heatmap selected, click the **Adjust requirements** link to modify heatmap thresholds and map opacity.
