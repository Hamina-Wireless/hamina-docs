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
   ![](<.gitbook/assets/Draw Walls.jpg>)
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

{% hint style="info" %}
Coming soon!
{% endhint %}

### Adding and Modifying Wall Profiles

With the Draw Walls tool activated, the Draw Walls pane will appear on the right. Click on the **Add or Modify** button at the bottom.

![](<.gitbook/assets/Add or Modify.png>)

The Wall Editor window will appear. From here, you can:

* Edit existing wall profiles (click on the profile to edit it)
* Duplicate wall profiles to create your own (click the **Duplicate** button in the wall profile)
* Create your own (click the **Add a custom wall** button)

![](<.gitbook/assets/Wall Editor.png>)

{% hint style="info" %}
Editing walls only affect the profiles in the project. Your other projects (and any new projects that you create) will be completely unaffected.
{% endhint %}
