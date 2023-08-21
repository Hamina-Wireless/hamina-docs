---
description: Get an overview of project importing and exporting in Hamina Network Planner.
---

# 🔁 Introduction

The Floor Plan Import/Export feature allows users to seamlessly import and export floor plans to and from cloud infrastructure systems, streamlining the wireless network design, deployment, and remediation cycle.

With this feature, you can easily import existing floor plans into Hamina, enabling you to plan changes to existing networks or just see how the current network performs. Additionally, the export feature allows users to export their designs back to vendor systems.

## Export Workflow

1. If the new site is created in Hamina, it will create a new site on the infrastructure.
2. If a matching floorplan doesn't exist, Hamina will export maps from Hamina to the infrastructure site.
3. If the user has planned APs that are MAC-matched in Hamina, it will assign them to the site and place them on the map.
4. For APs that have been placed on map in Hamina but have not been MAC-matched:
   1. If the **Utilize unused access points from organization** checkbox is checked, Hamina will commission all the non-MAC-matched planned APs to site (by picking APs of matching types from the inventory at random). _Note: If there are more planned APs on the floor plan in Hamina than APs of the same type in the vendor inventory, then not all planned APs will be commissioned to the site or placed on the map._
   2. If the **Utilize unused access points from organization** checkbox is _unchecked_, only MAC-matched APs will be commissioned to the site and placed on map.
5. If the floor plan on the vendor system has extra APs placed that don’t exist in Hamina, Hamina will remove the extra APs from map. _Note: These APs will not be removed from the site, just from the map._

