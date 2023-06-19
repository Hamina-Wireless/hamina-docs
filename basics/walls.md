---
description: Learn how to draw walls on maps with Hamina Network Planner.
---

# 🏗 Walls

Aside from setting the scale, either drawing walls (or having Hamina automatically draw the walls with a PDF or CAD map) is one of the most important parts of creating a wireless predictive model. The walls help Hamina "see" where the obstructions are, so it can accurately predict signal propagation on the map.

## Drawing Walls

{% hint style="info" %}
Use the Draw Walls tool only for drawing walls. For warehouse shelves, large machinery , or other objects with considerable width, we recommend using Attenuating Objects.
{% endhint %}

1. Click on **Draw Walls** > **Draw Walls** in the toolbar.\
   ![](<../.gitbook/assets/Draw Walls.jpg>)
2. **Left-click** once to start drawing a wall segment.
3. **Left-click** again to place the wall segment.
4. Continue **left-clicking** to chain multiple wall segments together.
5. **Right-click** to stop drawing walls.

{% hint style="success" %}
While drawing walls, hold down the `space` bar and move the mouse to pan! Since this panning method doesn't require any mouse clicks, it works great during wall drawing.
{% endhint %}

## Custom Wall Types

While Hamina includes some pre-set wall types to get you started, it's a great idea to change the existing profiles, or create your own to make the predictive model as accurate as possible.

### Measuring Walls

While the built-in defaults in Hamina are a good starting point, it's a great idea to take measurements of the walls in the real world, and input them into Hamina to increase the accuracy of the design. Modifying walls in one project does not affect your other Hamina projects.

1. Use a piece of hardware to create a 5 GHz network. This could be as complex as an AP-on-a-stick setup, or as simple as a 5 GHz hotspot on a smartphone. The idea is simply to create beacons in the 5 GHz band.
2. Posting the AP 3 to 5 meters away from the wall that you want to measure. Signal strength tends to drop off quickly within the first two meters, making it more difficult to get accurate measurements.
3. Use a device that can measure RSSI, such as a Wi-Fi scanner (Wi-Fi Explorer Pro, MetaGeek inSSIDer), real-time packet analysis tool (MetaGeek Tonic), or handheld Wi-Fi measurement device (NetAlly AirCheck G2 or G3). Take a signal strength measurement on the close side of the wall. Note the signal strength.
4. Take a signal strength measurement on the far side of the wall, and make note of it.
5. Subtract the first signal strength from the second. For example, if you saw -60 dBm on the close side, and -68 dBm on the far side, then you saw 8 dB of loss.
6. If you'd like, take several measurements and average them out before inputting them into Hamina. The more measurements you take, the more accurate Hamina's predictions will be, overall.

We recommend identifying the 3 to 5 most common types of walls in the building, getting measurements for them, and inputting them into Hamina. That should give you reasonable accuracy, without taking too much time gathering data.

### Adding and Modifying Wall Profiles

With the Draw Walls tool activated, the Draw Walls pane will appear on the right. Click on the **Add or Modify** button at the bottom.

![](<../.gitbook/assets/Add or Modify.png>)

The Wall Editor window will appear. From here, you can:

* Edit existing wall profiles (click on the profile to edit it)
* Duplicate wall profiles to create your own (click the **Duplicate** button in the wall profile)
* Create your own (click the **Add a custom wall** button)

![](<../.gitbook/assets/Wall Editor.png>)

{% hint style="info" %}
Editing walls only affect the profiles in the project. Your other projects (and any new projects that you create) will be completely unaffected.
{% endhint %}
