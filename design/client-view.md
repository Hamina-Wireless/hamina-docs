---
description: >-
  Learn how to view the network from the client's point of view in Hamina
  Network Planner.
---

# 📱 Client View

## Using the Client View

To activate the **Client view** tool, click on **Client view** in the **Network** section in the toolbar.

<div align="left">

<figure><img src="../.gitbook/assets/client_view_tool.png" alt="" width="563"><figcaption></figcaption></figure>

</div>

In the **Client Experience** pane on the right, select the desired Wi-Fi or Cellular client from the **Client device** drop down.

<div align="left">

<figure><img src="../.gitbook/assets/Client_device_list.png" alt="" width="563"><figcaption></figcaption></figure>

</div>

Click on the map to place the client, and view the network from the client's perspective. Click and drag the client across the map to simulate client movement. The client will roam from access point to access point, based on the client's known roaming algorithm.

<div align="left">

<figure><img src="../.gitbook/assets/client_view.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Drag the client around the map to see how the client is expected to roam between APs and bands.
{% endhint %}

### Client View Details

With the client placed on the map, or being moved around the map, the **Client View Details** pane will appear.

* The blue dashed line shows which AP the client is currently associated to.
* The thin grey dashed lines show roaming candidates.

Listed in the Client View Details pane:

* **Coverage**: The current received signal strength by the client. The client is assumed to have a 0 dBi, isotropic (perfectly omni-directional) antenna.
* **Data rate**: The current expected data rate of the client, which is based on:
  * AP and client spatial streams
  * AP and client Phy types
  * AP and client signal-to-noise ratio
  * Channel width
* **Interference**: How much co-channel interference the client is experiencing from APs.
* **Radio Capacity**: Appears whenever the client is near a Capacity Zone, and is a percentage of the AP radio's amount of associated clients and the capacity threshold for the AP radio.

Along the bottom of the Client View Details pane:

* **Current band**: The frequency band that the client is associated in. Hamina Planner will simulate a client performing an inter-band roam, or roaming to an AP in 2.4 GHz, when no 5 GHz option is available, per the known roaming algorithm of the selected client type.
* The MCS, client spatial streams, and channel width, which is all used to calculate the **Data rate**.

### Client View Settings

The Client Experience pane on the right has additional settings.

* **6 GHz capable** - Enables 6 GHz capabilities for the selected client.
* **Wi-Fi 7 capable** (coming soon) - Enables Wi-Fi 7 for the selected client.
* **Show association area** - Disables the current heatmap, and shows a blue area in which the client will stay associated to the AP. If the area is red, then the client is associated to an AP on a different floor.
* **Link direction**
  * **Downlink** - Displays simulated values as received and measured by the client.
  * **Uplink** -  Displays simulated values as received and measured by the AP.
  * **Worstlink** - Displays either downlink or uplink, whichever is worse. Worstlink is the default setting.

Below the **Show more** expander, there are further settings.

* **Client height**: The height of the client. This setting is linked to the **Client height** setting in the **Adjust requirements** pane.
* **Noise floor**: Sets the noise floor, per band. This setting is linked to the **Noise floor** setting in the **Adjust requirements** pane for SNR and Data Rate heatmaps.
* **Client transmit power**: Sets the transmit power of the client in milliwatts.
* **Min. interfering RSSI**:
