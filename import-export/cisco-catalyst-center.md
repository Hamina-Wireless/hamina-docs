---
description: Learn how to export designs from Hamina for import to Cisco Catalyst Center.
---

# 🧬 Cisco Catalyst Center

Hamina Network Planner can export the network design as a file that can be imported to Cisco DNA Center (formerly known as Cisco DNA Center or "DNAC").

{% hint style="danger" %}
This feature is currently in development, and is only available in Hamina Network Planner as a <mark style="color:red;">**Feature Preview**</mark>. It probably won't work at all, but feel free to give it a try if you're interested.
{% endhint %}

## Enabling the Cisco Catalyst Center Feature Preview

Since Cisco Catalyst Center Export is only available as a <mark style="color:red;">**Feature Preview**</mark>, it must be manually enabled before it will appear in the Export menu.

1. Click on the **Account** menu in the upper right corner.
2. Select **Edit account** from the list.
3. Click the **Feature preview** tab.
4. Enable **Cisco DNA center integration**.

## Exporting From Hamina Network Planner

1. Click the **Export Project** button.\
   ![](<../.gitbook/assets/Export Project (1).png>)\

2. Select **Cisco DNA Center** from the list, and click the **Continue** button.\
   ![](../.gitbook/assets/choose\_dna.png)\

3. Choose the desired floors and click **Export**. A progress indicator will appear at the top of the screen.\
   ![](../.gitbook/assets/export\_dna.png)

## Importing to Cisco Catalyst Center

1. Log into Cisco Catalyst Center/Cisco DNA Center, open the hamburger 🍔 in the upper left.\
   <img src="../.gitbook/assets/1_menu (1).png" alt="" data-size="original">\

2. Click **Design**, and then **Network Hierarchy**.\
   ![](../.gitbook/assets/2\_design\_network\_heirarchy.png)\

3. Next to the root of the hierarchy, click the **ellipsis menu**, and then **Add Building**.![](../.gitbook/assets/3\_elipsis\_add\_building.png)\

4. In the **Add Building** window, enter `Project name` in the **Building Name** field.  Set the latitude and longitude of the site, and click the **Add** button.\
   ![](../.gitbook/assets/4\_project\_name.png)\
   _Note: For now, this specific name is required, but should be fixed before the Feature Preview concludes._\

5. Next to the new building in the hierarchy, click the **ellipsis menu**, and then **Add Floor**.\
   ![](<../.gitbook/assets/5\_elipsis\_add\_floor (1).png>)\

6. In the **Add Floor** window, and enter the name of the floor you want to import in the **Floor Name** field. In our example, the floor name is "dnac".\
   ![](../.gitbook/assets/6\_add\_floor.png)\

7. Proceed without an image.\
   ![](../.gitbook/assets/7\_without\_image.png)\

8. In the toolbar along the top of the map, click **Import**, then click **Import Maps**.\
   ![](../.gitbook/assets/8\_import\_maps.png)\

9. Choose the `tar.gz` file that was generated in Hamina Network Planner, and click the **Import** button.\
   ![](<../.gitbook/assets/9\_select\_map (1).png>)\

10. Success! 🎉\
    ![](../.gitbook/assets/10\_success.png)\

11. Choose the map in the hierarchy.\
    ![](../.gitbook/assets/11\_select.png)\

12. The floor plan and access points should now be visible. _Note: For now, you will need to manually match AP models._\
    ![](<../.gitbook/assets/12\_view (1).png>)\
