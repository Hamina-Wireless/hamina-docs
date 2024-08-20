---
description: Learn about the Auto-plan APs tool in Hamina Network Planner.
---

# ✨ Auto-Plan APs Tool

The **Auto-plan APs** tool can be used to:

* Create a rough AP count for budgetary and quoting purposes
* Quickly distribute access points on the map for you to move to your preferred locations
* Create simple wireless network designs

## Environments

The Auto-plan APs tool works best in "carpeted" office spaces such as offices, schools, or other environments where access points are mounted to a ceiling of standard height.

{% hint style="danger" %}
The Auto-plan APs tool is not suitable for warehouses, manufacturing, outdoor environments, stadiums, or any other environments where directional antennas or non-ceiling mounts must be used. For these environments, we recommend traditional, manual planning.
{% endhint %}

## Creating an Auto-Plan

## Drawing Walls

Adding walls and attenuating objects is an important step in a successful Auto-Plan. Without them, it is possible to rely on the blanket Environment Attenuation (which is determined by the Environment Type in the Project Settings), but only for creating rough estimates for project budgeting and quoting.

## Scoping the Project

To understand where to place access points, and where Wi-Fi coverage is required, it is recommended to add Scope Zones to the project.&#x20;

In Scope Zones typically encompass the building to mark the extents of the building. They may also only encompass a portion of the building or specific area where Wi-Fi is required.

Out of Scope Zones can be used to subtract from a Scope Zone. They are typically used to mark stairwells, elevator shafts, closets, or anywhere else that Wi-Fi is not required.

To learn more about Scope Zones, see [Scope Zones](../basics/scope-zones.md).

The Auto-plan APs tool will:

* Only consider the scope of the project
* Will not place APs outside of the project scope
* Will attempt to meet the Primary Coverage requirement on 99+ percent of the scope zone
* Will attempt to meet the Secondary Coverage requirement on 85+ percent of the scope zone (unless the floor plan is very small)

## Access Point Configuration

To configure the access points for the design, open the Auto-Plan APs tool.

<div align="left">

<figure><img src="../.gitbook/assets/auto-plan-aps-menu (1).png" alt=""><figcaption></figcaption></figure>

</div>

The Auto-plan APs pane will appear on the right, where you can select an AP model and customize the configuration, such as:

* Color
* Access point make and model (_Note: Only omni-directional APs and antennas are supported._)
* Mounting type and height
* Access point name (_Tip: variables work great for programmatically populating AP names. See_ [_Access Points_](access-points.md) _for details._)
* Transmit power

## Running the Auto-Plan

Click the **Start the auto-plan** button to begin. The Auto-plan APs tool will ~~slosh green paint all over the place~~ iterate through potential designs with a progress indicator in the lower right.

<figure><img src="../.gitbook/assets/auto-plan-aps (3).gif" alt=""><figcaption></figcaption></figure>

The Auto-plan APs tool will avoid placing APs:

* Near each other
* Near walls
* Near the edges of scope zones
* In line-of-sight of each other.

This should result in a design that usually avoids hallways, places APs near the centers of rooms, and just looks good. 😎

In environments with heavy attenuation (such as concrete walls), the Auto-plan APs tool will add more access points. It is also not unusual to see some small holes in coverage, as the tool attempts to create a balanced network design. The Auto-plan APs tool will never threaten you and in fact, cannot speak. Talk to your doctor to see if the Auto-plan APs tool is right for you.

