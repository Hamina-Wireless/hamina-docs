---
description: Learn how to draw, use, and edit Scope Zones in Hamina Network Planner.
---

# 📍 Scope Zones

## Scope Zones

In Hamina, Scope Zones are used to define where Wi-Fi, Bluetooth and Private Cellular coverage is desired on the map. Using Scope Zones, you can mark which areas are within the scope of the project, and what is beyond the scope of the project.&#x20;

There are two types of Scope Zone in Hamina:

* **In Scope Zones**, which defines what parts of the map where network coverage is desired, required, or is otherwise in the scope of the project. This usually includes building interiors, specific suites in multi-tenet buildings, or anywhere that business operations require wireless coverage. In Scope Zones typically encompass an entire building, a significant section of a building, or in the case of an outdoor design, an entire campus area. Any areas outside of the In Scope Zone(s) are automatically considered out of scope.
* **Out of Scope Zones**, which define what parts of the map where coverage is not desired or required. This could be areas where installing access points is cost prohibitive, such as elevators or stairwells. It could also be places where coverage is simply not needed, such as janitorial closets. Typically, Out of Scope Zones are only used inside of In Scope Zones.

## Drawing Scope Zones

We recommend beginning by drawing **In Scope Zones**, which typically encompass large areas such as:

* The entire perimeter of a single-tenant building (which would automatically exclude the parking lot)
* An entire suite in a multi-tenant building (which would automatically exclude other suites in the building)
* An entire shipping yard, university campus, or downtown area

{% hint style="info" %}
Drawing a large Scope Zone around a building will automatically create an In Scope Zone.
{% endhint %}

Next, we recommend drawing **Out of Scope Zones** inside the In Scope Zone to mark what parts of the map coverage is not desired or required. This typically includes elevator shafts, stairwells, and storage closets.

{% hint style="info" %}
Drawing a small Scope Zone inside a large In Scope Zone will automatically create an Out of Scope Zone.
{% endhint %}

### Drawing Rectangular Scope Zones

To draw a rectangular scope zone:

1. Select the **In/Out of Scope Zone** tool in the toolbar.
2. With the left mouse button, click and drag diagonally across the map to create a rectangle.
3. Release the mouse button.
4. A rectangular Scope Zone and Scope Zone Toolbar will appear.

{% hint style="success" %}
With the **Scope Zone Toolbar**, you can manually switch between In Scope and Out of Scope Zones.
{% endhint %}

### Drawing Free-Form Scope Zones

Drawing free-form scope zones allow you to create arbitrary shapes (which is especially useful for drawing the perimeter of a building). Free-form scope zones draw very similarly to walls in Hamina.&#x20;

To draw a free-form scope zone:

1. Select the **In/Out of Scope Zone** tool in the toolbar.
2. Left-click on the map to place the first point
3. Left-click elsewhere on the map to place subsequent points
4. After placing the final point, right-click to stop drawing and finalize the amount of points in the free-form scope zone.

### Changing the Scope Zone Type

Depending on the size of the zone, Hamina Network Planner will automatically select an In Scope Zone, or Out of Scope Zone. If you'd like to manually change the Scope Zone type:

1. Select the **Edit** tool from the toolbar
2. Right-click the edge of the Scope Zone
3. The Scope Zone pop-up menu will appear
4. Choose between **In Scope Zone** and **Out of Scope Zone** in the pop-up menu

{% embed url="https://youtu.be/j_pZ469_deE" %}

### Editing Scope Zones

To edit a scope zone:

1. Select the **Edit** tool from the toolbar.
2. Click on the border of the Scope Zone that you want to edit.
3. The **Scope Zone Toolbar** will appear
4. Click and drag points on the Scope Zone to move them. _Note: Scope Zone points will have small squares around them._
5. Click away from the Scope Zone to finish editing it.
