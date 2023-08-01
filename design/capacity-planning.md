---
description: Learn how to create capacity plans in Hamina Network Planner.
---

# Capacity Planning

In Hamina Network Planner, Capacity Zones are used to add groups of clients to the map, so you can predict how many clients will associate to nearby access point radios, and ensure that no AP radio becomes overloaded.

Capacity Zones use the same client roaming algorithm as the Client View to determine which AP radios clients will associate to. When a Capacity Area is drawn on the map, the client types and amount of each client type is evenly distributed throughout the area, and then Hamina Network Planner simulates each client to determine which AP radio it will associate to.

## Creating and Drawing Capacity Areas

1. To draw an area, click on **Capacity** in the toolbar. The **Add Capacity Zone** pane will appear on the left.
2. In the **Add Capacity Zone** pane, you can optionally give the zone a custom name, and define the type and amount of clients.
3. To draw a square Capacity Zone:
   1. With the left mouse button, click and drag diagonally across the map to create a rectangle.
   2. Release the mouse button.
   3. A rectangular Scope Zone and Scope Zone Toolbar will appear.
4. To draw a free-form Capacity Zone:
   1. Left-click on the map to place the first point.
   2. Left-click elsewhere on the map to place subsequent points.
   3. After placing the final point, right-click to stop drawing and finalize the amount of points in the free-form scope zone.

<figure><img src="../.gitbook/assets/Draw Capacity Zone.gif" alt=""><figcaption></figcaption></figure>

## Editing Capacity Zones

You can change the Capacity Zone name, types of clients, and amounts of clients in a given zone at any time using the **Edit** tool.

To edit a Capacity Zone:

1. Select the **Edit** tool from the toolbar.
2. Right-click one of the edges of the Capacity Zone (not necessarily a corner).
3. The **Edit Capacity Zone** pane will appear

## Viewing Capacity Results

When a Capacity Zone has been placed near an access point, Hamina Network Planner will use the client roaming algorithm to determine how many clients are expected to associate to each radio.



