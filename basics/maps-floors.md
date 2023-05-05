---
description: Learn how to switch, rename, and manipulate maps in Hamina Network Planner.
---

# 🏭 Managing Maps and Floors

## Adding Additional Maps

Additional maps can be added to Hamina in the **Floor** drop-down menu at the top. Click the **Floor** drop-down menu, and click the **Add a floor** button to add additional maps.

{% hint style="info" %}
Until floors are added to a building, maps don't have any relationship with each other. Instead, they simply exist in the same project. This is useful if you have several single-floor buildings in a campus environment, and want to contain them all in the same project..
{% endhint %}

## Renaming Maps

To rename a map, click on the **Floor** drop-down, point to the floor, and click **Rename**.

<figure><img src="../.gitbook/assets/rename_map (1).png" alt=""><figcaption></figcaption></figure>

### Map Sorting

In the Floor dropdown, maps are sorted numerically/alphabetically in _descending_ (largest to smallest) order, which causes the floors to be sorted logically in how they would stack up in a building, for example:

* Floor 4
* Floor 3
* Floor 2
* Floor 1

It is possible to further organize maps with additional names, such as the names of buildings.

{% hint style="info" %}
Note: Only one multi-floor building is supported per project. If you need to design for more than one multi-floor building, then we recommend creating a unique project for each building.
{% endhint %}

#### Map Sorting for Buildings

When floors are added to a building, they are sorted in the map dropdown based on their order in the building, which can override the default map sorting.

<figure><img src="../.gitbook/assets/floor_reorder.png" alt=""><figcaption><p>Floor 1 is erroneously placed above Floor 2, to illustrate how buildings override default map sorting.</p></figcaption></figure>

## Creating a Building

When a map is added to a building, the maps can be stacked up and aligned to form multiple floors.

{% hint style="success" %}
We recommend renaming all of the maps in your project before creating a building and aligning floors, which makes for more organized projects with cleaner deliverables.
{% endhint %}

To add floors to the building for alignment:

1. Ensure that at least one map has the correct scale, and select it with the **Floor** menu at the top.
2. Click on the **Floor alignment** tool in the toolbar on the left.
3. In the **Floor alignment** pane on the left, drag any desired floors into the build area at the top.
4. Drag the floors into the correct order within the building, with the lower floors on the bottom of the list.

<figure><img src="../.gitbook/assets/add_floors.gif" alt="" width="360"><figcaption></figcaption></figure>

## Aligning Floors

Floor alignment is accomplished by dragging the yellow map until it aligns with the black map.&#x20;

* The **black map** is the the current floor, e.g. the map that is selected with the **Floor** menu on the top.
* The <mark style="color:yellow;">**yellow map**</mark> is the floor that is currently being moved and resized. The position and scale of the yellow map is changed in relation to the position and scale of the black map. You can change which map you want to move and resize by clicking on other maps in the **Floor alignment** pane.

<figure><img src="../.gitbook/assets/alignment_colors.png" alt=""><figcaption></figcaption></figure>

Align the floors by identifying common features between floors, such as elevators and stairwells.

<figure><img src="../.gitbook/assets/drag_floors_to_align (1).gif" alt="" width="525"><figcaption></figcaption></figure>
