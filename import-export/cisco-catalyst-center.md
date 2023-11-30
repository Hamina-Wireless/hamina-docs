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

1.  Click on the **Account** menu in the upper right corner, and select **Edit Account** from the list.\


    <div align="left">

    <figure><img src="../.gitbook/assets/settings (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
2.  Click the **Feature preview** tab, and enable **Cisco DNA center integration**.\


    <div align="left">

    <figure><img src="../.gitbook/assets/enable_dna.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>

## Exporting From Hamina Network Planner

1.  Click the **Export Project** button.\


    <div align="left">

    <figure><img src="../.gitbook/assets/Export Project (1).png" alt="" width="373"><figcaption></figcaption></figure>

    </div>
2.  Select **Cisco DNA Center** from the list, and click the **Continue** button.\


    <div align="left">

    <figure><img src="../.gitbook/assets/choose_dna.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
3.  Choose the desired floors and click **Export**. A progress indicator will appear at the top of the screen.\


    <div align="left">

    <figure><img src="../.gitbook/assets/export_dna.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>

## Importing to Cisco Catalyst Center

1.  Log into Cisco Catalyst Center/Cisco DNA Center, open the hamburger 🍔 in the upper left.\


    <div align="left">

    <figure><img src="../.gitbook/assets/1_menu (1).png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
2.  Click **Design**, and then **Network Hierarchy**.\


    <div align="left">

    <figure><img src="../.gitbook/assets/2_design_network_heirarchy.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
3.  Next to the root of the hierarchy, click the **ellipsis menu**, and then **Add Building**.\


    <div align="left">

    <figure><img src="../.gitbook/assets/3_elipsis_add_building.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
4.  In the **Add Building** window, enter `Project name` in the **Building Name** field.  Set the latitude and longitude of the site, and click the **Add** button.\
    \
    _Note: For now, this specific name is required, but should be fixed before the Feature Preview concludes._\


    <div align="left">

    <figure><img src="../.gitbook/assets/4_project_name.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
5.  Next to the new building in the hierarchy, click the **ellipsis menu**, and then **Add Floor**.\


    <div align="left">

    <figure><img src="../.gitbook/assets/5_elipsis_add_floor (1).png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
6.  In the **Add Floor** window, and enter the name of the floor you want to import in the **Floor Name** field. In our example, the floor name is "dnac".\


    <div align="left">

    <figure><img src="../.gitbook/assets/6_add_floor.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
7.  Proceed without an image.\


    <div align="left">

    <figure><img src="../.gitbook/assets/7_without_image.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
8. In the toolbar along the top of the map, click **Import**, then click **Import Maps**.\
   ![](../.gitbook/assets/8\_import\_maps.png)\

9.  Choose the `tar.gz` file that was generated in Hamina Network Planner, and click the **Import** button.\


    <div align="left">

    <figure><img src="../.gitbook/assets/9_select_map (1).png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
10. Success! 🎉\


    <div align="left">

    <figure><img src="../.gitbook/assets/10_success.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
11. Choose the map in the hierarchy.\


    <div align="left">

    <figure><img src="../.gitbook/assets/11_select.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
12. The floor plan and access points should now be visible. _Note: For now, you will need to manually match AP models._\


    <div align="left">

    <figure><img src="../.gitbook/assets/12_view (1).png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
