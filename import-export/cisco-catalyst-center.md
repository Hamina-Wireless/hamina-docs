---
description: Learn how to export designs from Hamina for import to Cisco Catalyst Center.
---

# 🧬 Cisco Catalyst Center

Hamina Network Planner can export the network design as a file that can be imported to Cisco Catalyst Center (formerly known as Cisco DNA Center or "DNAC").

In Cisco Catalyst Center, there are two ways to import data:

* With a hierarchy file generated in Hamina Network Planner. This generates a `.csv` file, which contains the entire hierarchy including buildings and floors. The following instructions use this method, which is recommended.
* Manually, without a hierarchy file. With this method, you will need to define an exact hierarchy, or Cisco Catalyst Center will fail to import the Floor Maps. Instructions for this method can be found in a [later section of this article](cisco-catalyst-center.md#manual-hierarchy).

## Exporting from Hamina Network Planner

1.  In the Project menu, select **Export Project**.\


    <div align="left" data-full-width="true">

    <figure><img src="../.gitbook/assets/export.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
2.  Select **Cisco Catalyst (DNA) Center** from the list, and click the **Continue** button.\


    <div align="left">

    <figure><img src="../.gitbook/assets/export-menu.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
3.  Define the **Areas**, **Building** name, and choose which floor plans to export. **Sub-areas** can be defined with a `/` symbol.\


    <div align="left">

    <figure><img src="../.gitbook/assets/export-settings-blank.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>

    Since we will be downloading a hierarchy and uploading it to Cisco Catalyst Center, you can define areas, sub-areas, and the building as you see fit (but you may want to consider your existing hierarchy).\


    <div align="left">

    <figure><img src="../.gitbook/assets/export-settings-filled.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
4.  Click **Download hierarchy** and **Download project.**\
    \
    **Download hierarchy** will download a **Sites** / **Hierarchy** / `.csv` file, which defines Areas, Sub-areas, Buildings, and Floors.\
    \
    Download project will generate a **Project** / **Floor Maps** / `tar.gz` file, which contains the maps and APs.\


    <div align="left">

    <figure><img src="../.gitbook/assets/exported-files.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>

## Importing to Cisco Catalyst Center

1.  In Cisco Catalyst Center, click the menu icon.\


    <div align="left">

    <figure><img src="../.gitbook/assets/cat-center-home.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
2.  In the menu, click **Design** and then **Network Hierarchy**.\


    <div align="left">

    <figure><img src="../.gitbook/assets/cat-center-menu.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
3.  In the toolbar along the top, click **Import**, then **Import Sites**.\


    <div align="left">

    <figure><img src="../.gitbook/assets/import-sites.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
4.  Upload the **Sites** / **Hierarchy** / `.csv` file that was generated in Hamina, and contains definitions for Areas, Sub-areas, Buildings, and Floors.\


    <figure><img src="../.gitbook/assets/import-csv (1).png" alt=""><figcaption></figcaption></figure>
5.  Once the import is complete, you'll see the hierarchy in Cisco Catalyst Center. _Optionally, you can define an address for your new building._\


    <div align="left">

    <figure><img src="../.gitbook/assets/edit-address.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
6.  Now that the hierarchy exists, select **Import** > **Import Floor Maps** to upload the **Project** / **Floor Maps** / `tar.gz` file, which contains the maps and APs.\


    <div align="left">

    <figure><img src="../.gitbook/assets/import-gz.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>

    <div align="left">

    <figure><img src="../.gitbook/assets/import-floor-maps.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
7.  Follow the prompts in Cisco Catalyst Center to import the file, preview the import, and view the hierarchy.\


    <div align="left">

    <figure><img src="../.gitbook/assets/import-preview.png" alt=""><figcaption></figcaption></figure>

    </div>
8.  Click on one of the maps to view it.\


    <div align="left">

    <figure><img src="../.gitbook/assets/view-catalyst-import.png" alt=""><figcaption></figcaption></figure>

    </div>

## Manually Defining a Hierarchy <a href="#manual-hierarchy" id="manual-hierarchy"></a>

It is possible to manually define a hierarchy in Cisco Catalyst Center, and create a Hamina project file that conforms to the Catalyst Center hierarchy. In Cisco Catalyst Center:

1. Create the desired area and sub-area hierarchy.
2.  Next to the desired area, select **...** > **Add Building**, and create the building.\


    <figure><img src="../.gitbook/assets/add-building (2).png" alt=""><figcaption></figcaption></figure>
3.  Next to the newly-created building, click **...** > **Add Floor**.\


    <figure><img src="../.gitbook/assets/add-floor.png" alt=""><figcaption></figcaption></figure>
4.  In the building, create each floor that you intend to export from Hamina. _Note: Ignore any warnings amount missing images, as those will be added when the `tar.gz` file is imported._\


    <div align="left">

    <figure><img src="../.gitbook/assets/add-floor-dialogue.png" alt=""><figcaption></figcaption></figure>

    </div>
5.  In Hamina Network Planner, download the **Project** / **Floor Maps** /`tar.gz` file, making sure that the areas, sub-areas, building name, and floor plan names all match Cisco Catalyst Center. _Note: Everything must match, or the import will fail._\


    <div align="left">

    <figure><img src="../.gitbook/assets/export-settings-manual (1).png" alt=""><figcaption></figcaption></figure>

    </div>
6.  In Cisco Catalyst Center, in the toolbar along the top, click **Import**, then **Import Floor Maps**.\


    <div align="left">

    <figure><img src="../.gitbook/assets/import-sites-manual.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
7.  Import the **Project** / **Floor Maps** /`tar.gz` file. Follow the prompts in Cisco Catalyst Center to import the file, preview the import, and view the hierarchy.\


    <figure><img src="../.gitbook/assets/import-sites-wizard-manual.png" alt=""><figcaption></figcaption></figure>
8.  Click on one of the maps to view it.\


    <div align="left">

    <figure><img src="../.gitbook/assets/view-maps-manual.png" alt=""><figcaption></figcaption></figure>

    </div>

## Updating Access Points

It is possible to update access point models and placements on a floorplan.

1. Make adjustments to the project in Hamina as needed.
2.  Export the **Project** / **Floor Maps** /`tar.gz` file from Hamina. _Note: You can either export all floors, or you can choose to only export the floors that need to be updated (recommended)._\


    <figure><img src="../.gitbook/assets/export-subselection.png" alt=""><figcaption></figcaption></figure>
3. Using **Import** > **Import Floor Maps**, import the **Project** / **Floor Maps** /`tar.gz` file.
4.  Access point locations and models will be updated.\


    <figure><img src="../.gitbook/assets/update-in-hamina.png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../.gitbook/assets/update-in-cat-center.png" alt=""><figcaption></figcaption></figure>
