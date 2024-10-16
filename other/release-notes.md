---
description: Learn about new features, changes, and bug fixes in Hamina Network Planner.
---

# 🗒️ Release Notes

### 2024/10/18

**New Features and Improvements**

* We implemented a new heatmap progress bar! The light blue line shows overall progress, from the far left to the far right of the browser window. The dark blue line now shows heatmap calculation progress for the the current stage, of which there are several. On smaller designs with a very fast machine, you might not be able to spot the changes at all, but on a larger design or on a slower machine, you can now keep an eye on the dark blue line to see when the calculation for the current stage will complete.
* To help speed things up more, we dropped the last calculation stage. It was so high resolution that it took more time to calculate than all of the other stages combined, and it was pretty tough to spot the difference between the final stage, and the previous stage.
* Remember that multi-thread/multi-core support that we added? We found that while Hamina performed amazingly well like this, it seemed to steal a lot of system resources from other applications, like Zoom and Microsoft Teams during video calls. With this release, we now leave one or more cores idle for other applications to use.

### 2024/10/14

**New Features and Improvements**

* Hamina Network Planner Plus now supports **importing site surveys from NetAlly Link-Live**! You can create site surveys with AirMapper on the AirCheck G2, AirCheck G3, EtherScope, or CyberScope, and import them to Hamina for deep analysis. Note that this functionality (along with the rest of our Import, Export, and Live functions) are still marked as "Beta" for now. If you run into any snags, let us know.&#x20;
*   This release also adds PDF reporting for site surveys! Just like before, you can choose which SSIDs to include in the **Report settings** (gear icon) in the upper right, pick which survey paths to include on the **Survey Paths** page, and then click **Generate PDF Report**. Part of what enabled this was the multi-threading support for heatmap generation in the last production push.\


    <div align="left">

    <figure><img src="../.gitbook/assets/pdf-reports.png" alt="" width="359"><figcaption></figcaption></figure>

    </div>
* Previously when you had a map in Hamina Network Planner, and a map in your infrastructure vendor's cloud, it was only possible to connect them if the width and height matched. Now, we can match them if the map names are the same.

**Access Points and Antennas**

* AccelTex ATS-OO-2456-466-6
* AccelTex ATS-OP-2456-13-6
* AccelTex ATS-OP-2456-7-6
* AccelTex ATS-OP-2456-8-4
* AccelTex ATS-OP-2456-8-6
* AccelTex ATS-OP-2456-81010-6
* Cisco IW9165E
* Edgecore SP-W2-AC1200
* Extreme ML-2452-PTA4M4-036
* Fortinet 241K
* Fortinet 243K
* Intelbras AP3620H
* LANCOM Airlancer ON-Q30
* Meraki MR12
* Meraki MR16
* Meraki MR66
* MP Antenna 08-ANT-0937
* Rajant KMA-2400-5
* Rajant KMA-5800-6
* Ventev M3030050O10006CB
* Ventev M3030050O10049CB
* Ventev M3030050O20006LP
* Ventev M7060060D4D3620AP
* Ventev VI-U2OM-NF
* Ventev VT-HUHM6-IONF
* Ventev VY1-VLHM6-ODNF
* We also added datasheet gains for the Linksys Velop Pro7 and Velop WRT Pro 7.

### 2024/10/09

**New Features and Improvements**

* We added multi-threading support for calculating heatmaps in Hamina Network Planner, in the report editor, and online report viewer. In our testing on an Apple Silicon MacBook Pro, one of our "torture test" heatmaps went from taking 20 minutes to calculate all stages down to just 4 minutes, a 5x improvement! You should see some improvements too, especially if you have lots of processor cores. How we calculate heatmaps in stages is a pretty important part of Hamina Network Planner, so we recommend [checking out our article about heatmap calculations](https://docs.hamina.com/planner/basics/heatmaps#heatmap-calculations).
*   There was a bit of confusion about how the floors stack up in the Multi-floor tool, so we added a little "lowest floor" indicator.\


    <div align="left">

    <figure><img src="../.gitbook/assets/lowest-floor.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>

**Bugfixes**

* Remember the measurement fetching improvements that we made in the last production push? Well... it created a bug where clicking on an AP in an online report would cause the page to refresh. Oops. That's fixed now!
* Awhile back, we accidentally broke the easter egg inside of the easter egg. The egg in the egg is now fixed. Speaking of which, where _is_ Westcott, anyway?
* The Calix 7u10t and 7u10txg snuck into an earlier production push with names that didn't quite match the naming convention in Hamina Network Planner, so we corrected them. Everything is all matchy-matchy now.

### 2024/10/03

**New Features and Improvements**

* Ruckus One is now available in the Live View! Remember that the Live View is currently offered as a **Feature Preview**, so it is still a work-in-progress. If you find bugs or have feedback and questions, hit us up at <mark style="color:blue;">**support@hamina.com**</mark>.
* We tweaked and improved the styling on the Subscriptions page.

**Bugfixes**

* We made some big improvements to how we fetch measurements for survey heatmaps! This fixed a timeout issue for a specific customer, but also improved fetching speeds for everyone else.

### 2024/09/30

**Bugfixes**

* Oof, we broke the Interference heatmap selector. There was an issue where the checkboxes would be ignored, so we showed everything all of the time. Fixed now!

**Access Points and Antennas**

* Calix 7u10t GigaSpire
* Calix 7u10txg GigaSpire

### 2024/09/26

**New Features and Improvements**

* There's just one for this round! In the case of dual 5 GHz APs, we added some QBSS Load IE imitation to the capacity planner to help clients more realistically distribute between two radios on the same AP in the simulation.

**Bugfixes**

*   Previously in Hamina Network Planner, there was an indicator of how many APs were on the current map. At some point while working on styling updates and fixes, we accidentally removed it. It's back now!\


    <figure><img src="../.gitbook/assets/Screenshot 2024-09-26 at 3.51.39 PM.png" alt=""><figcaption></figcaption></figure>
* When generating PDF reports, there was a bug that would cause everything after the first image on the Notes page to be missing from the PDF. That's fixed now, your note pages should include all notes and images.

### 2024/09/19

**New Features and Improvements ✨**

* Zigbee and EnOcean now get their own sections in reports! Previously, reports could only include sections for Wi-Fi, Bluetooth, and 4G/5G private cellular networks, but now everything is available.
* Additionally, we only include sections if that particular technology is included in the project. For example, if you create an EnOcean-only project, it will only have an EnOcean section. If you want to add another technology to the report, just add some Wi-Fi gear to the project.
* The iPhone client type now includes Wi-Fi 7.

**Bugfixes**

* If an information element in a beacon contained an invalid channel number, it could cause Hamina Onsite to crash. We fixed it over here on the Hamina Network Planner side of things.

**Access Points and Antennas**

* DCN WL8200-X2
* DCN WL8200-X4
* DCN WL8200-X10
* Meraki MR34
* We added a dual 5-GHz option to the Extreme AP510i.
* Aruba worked with us to improve the antenna patterns for the Aruba AP-365, AP-565, and AP-567.&#x20;
* There was a mistake in the Aruba AP-515 and AP-567 "datasheet gain", so we fixed that too.

### 2024/09/10

**New Features and Improvements ✨**

* We _did_ improve some things, but it's all behind-the-scenes preparation for upcoming features, so there's really nothing to see here.\
  \
  ![](../.gitbook/assets/please-disperse.webp)\

* No wait, hang on, there was one thing. We renamed "Display Patterns" to "Variables", which is a system for dynamically renaming access points, switches, and wired clients. [It's worth checking out](https://docs.hamina.com/planner/design/access-points#renaming-access-points), if you aren't familiar with it already.

**Bugfixes**

* In some cases, the mouseover inspector for the interference heatmap in survey mode wouldn't list all of the APs. That's fixed.
* In the survey tab, selecting an AP and switching to a different floor was broken; Planner would show all access points as if nothing was selected.

**Access Points and Antennas**

* Alcatel AP1511
* Baicells Nova227
* Baicells Nova430e
* Baicells Nova430i
* Baicells Nova442i
* CyberTAN RAP630C-311G
* EnGenius ECW526
* Huawei 5573-23H
* LANCOM OW-602
* Meraki MR32
* Nomadix AP-6RA
* Nomadix AP-6SA
* Nomad AP-6WA
* We also added dual 5 GHz modes for the Cisco 9120AXE 2x Trout and 2x Patch antennas.
* We corrected the datasheet gain for the Huawei 5762-10.
* We had the Ubiquiti UAP-AC-Mesh-UMA-D listed as an access point, when it is actually an external antenna. We removed it from the AP list, and added it to the external antenna list as "Directional Antenna (for AC Mesh)".
* We renamed the CyberTAN EWW631-B1 to RAP630W-311G to match CyberTAN's new model number scheme.

### 2024/08/20

**New Features and Improvements ✨**

*   Hamina Network Planner can now **Auto-plan APs**!\


    <figure><img src="../.gitbook/assets/auto-plan-aps-menu.png" alt=""><figcaption></figcaption></figure>

    \
    In the Auto-plan APs pane, can customize your AP as usual including colors, naming conventions (with variables for names), height, and everything else that you're used to customizing. Then, you can choose any omni-directional AP, or any AP with an external omni-directional antenna, and click the **Start the auto-plan** button. Sit back and relax as Hamina Network Planner paints your heatmap green! To learn more, check out the [Auto-Plan APs](https://docs.hamina.com/planner/design/auto-plan-aps) article.\


    <figure><img src="../.gitbook/assets/auto-plan-aps.gif" alt=""><figcaption></figcaption></figure>
*   **Layer controls** are now available in the Survey tab! You can toggle things on and off including access points, labels (including numbers and names), notes, and survey paths.\


    <figure><img src="../.gitbook/assets/layers-menu-in-survey-tab.png" alt=""><figcaption></figcaption></figure>
*   Hamina Network Planner now features the Windows Laptop client device type! Normally, we add clients by consulting the vendor and getting the exact roaming behaviors from the source. In this case, we "brute-forced" it by simulating thousands of roaming events with common Intel chipsets, and then analyzing the data to find the behavior patterns. We think the result gets us (and you) a solid simulation of when we think Windows clients with Intel chipsets will roam, and how they will decide where to roam.\


    <figure><img src="../.gitbook/assets/windows-client-roam.png" alt=""><figcaption></figcaption></figure>
* In the Feature Preview for the Live view, environment learning is now supported for Arista networks!
* Since it is pretty tough to get 250 Mbps with a 20 MHz channel (unless you are within a few meters of the AP), we dropped the default green threshold from 250 to 200 Mbps in the Data Rate heatmap.
* We combined **Preferences**, **Teams**, **Billing & subscription**, and **Feature preview** into a new **Settings** modal, which makes things feel cleaner and more connected.

**Bugfixes 🪲**

* We fixed a weird bug that caused PoE consumption calculations to differ between web reports and PDF reports. They match, now!
* Paying for Hamina would immediately reward the user with a bug! The Subscriptions page wouldn't pop back up like it was supposed to. Now, we reward paying customers by making the Subscriptions page re-appear properly. Oh yeah, we're gooooood.
* Hamina Network Planner Lite users couldn't switch interference sources between **My network** and **All networks**. That wasn't on purpose, so we fixed it.
* Dan found a weird bug where sloped floor transparencies would break in 3D. We fixed it, and we hope that Dan is happy.

**APs and Antennas**

* Askey EAI2308P
* Baicells Nova436Q
* EnGenius EWS850-FIT
* Fortinet
  * Added 432G custom antennas mode
  * FANT-04ACAX-0606-D
* Huawei AP361
* Siemens
  * ANT795-6DC
  * ANT795-6MP
  * ANT795-4MX
  * ANT793-8DP
* Ubiquiti
  * Swiss Army Knife
  * External Omni Antennas (for Swiss Army Knife)
  * External Panel Antenna (for Swiss Army Knife)
  * U7 Outdoor external omni antenna mode
* We updated the datasheet peak gain for the Nile NWA1000.
* We added the datasheet peak gains for the Calix u6t and u6txg.

### 2024/07/31

Finnish summer vacations are coming to an end, and the product and engineering team is trickling back into the office! You know what that means: it's time for a production push!

**Improvements** ✨

*   Back in the day, access points were simple; they had one or two radios and an Ethernet port. These days, they're pretty complicated! Many access points can switch a radio to a different band. Some access points have both an internal antenna, external antennas that come in the box, or the ability to use a completely custom 3rd party antenna. Other APs even have the ability to split up a radio into multiple radios with less spatial streams! To better support this, we've introduced the new **Modes** menu for access points that need it. When you select an access point, if the AP has multiple software-configurable or hardware-configurable modes available, the "Modes" menu will appear. In some cases, the Modes menu adjusts the beamwidth of the built-in antennas, which type of antenna should be used (such as internal and external), or what frequency bands the radios should be configured to use. It cleans up the AP list a lot, and lays the groundwork for more AP configurations options.\


    <figure><img src="../.gitbook/assets/mode.png" alt=""><figcaption></figcaption></figure>
*   We changed behavior of the blue progress bar at the top of Hamina Network Planner, which shows the current heatmap calculation progress. Hamina keeps things super-fast by calculating a low-resolution heatmap first, and then iterating through higher resolution heatmaps until things are "pixel perfect". We also focus calculations on the current viewport, so when it moves (e.g. you pan or zoom), we need to restart the heatmap calculation. This is also true if you change the model (e.g. add a wall or move an AP). Previously, we added the new progress to the remainder of the progress bar, which had the unintended side effect of making it look like it had frozen. Now, we just reset the whole progress bar, which we hope will make it more obvious what Hamina Network Planner is doing. If you want to learn more, check out the [Heatmaps knowledgebase article](https://docs.hamina.com/planner/basics/heatmaps#heatmap-calculations).\


    <div align="left">

    <figure><img src="../.gitbook/assets/resetting-progress (1).gif" alt=""><figcaption></figcaption></figure>

    </div>
* For the Live View feature preview, we added Wi-Fi and non-Wi-Fi Utilization heatmaps for the vendors that support it. If the connected infrastructure vendor supports it, you'll find **Wi-Fi** and **non-Wi-Fi** checkboxes under the **Utilization** in the **Heatmap settings** menu.
* In the Live View feature preview, we improved the Channel Utilization heatmaps by showing nothing instead of green when there's no data.
* Previously in the Live View when the Channel Utilization heatmap was displayed, filtering would be applied based on the AP selection. Filtering down to specific APs could create misleading heatmaps, so we disabled the filtering (but just for the Channel Utilization heatmap).
* The Live View Channel Utilization heatmap now has an extra shade of green to help tell coverage cells apart.
* In PDF reports, on the **AP Placement** page, we bumped up the render resolution. This means the report will take slightly longer, but the higher-resolution image will help out AP installers in large buildings.
* When exporting an OpenIntent schema file, we added the name of the project to the filename to make it easier to recognize.
* We updated the styling and content on the project start page, including links to helpful videos and the knowledgebase.
* The styling for the **Display patterns** dialogue box has been updated.
* The walrus. It has changed. What does that mean? It's up to you to find out.

**Bugfixes** 🔧

* When viewing Interference for survey results, the mouseover inspector would randomly not list access points. That is fixed!
* In the Live View feature preview, we were accidentally pulling adjacent floors in from the Simulation tab. Oops! Not anymore.
* This isn't _exactly_ a bug, but it feels a bit like one: In the Live View feature preview, once you connected your project to some infrastructure to get the Live View, automatic channel planning would be turned off for the simulation. Now, automatic channel planning will happily work alongside the Live View in the same project.
* The Capacity Planner was allowing clients to associate to disabled radios. LOL, yeah uhhhh that's not right. We made it right.
* In the Survey tab, holding `Shift` didn't disable snapping for the **Scale** tool. It works as expected, now!

**APs and Antennas** 📶

* Aruba
  * AIO-AP21
  * AIO-AP22D
  * AIO-AP32
  * AIO-AP27
  * AP-605H
  * AP-677
  * AP-675
  * AP-679
  * ANT-3x3-5712
* ASUS
  * EBR63
  * EBM68
  * RT-AX57Go
* Calix
  * GigaPro p4
* Cisco
  * 2702i
* Extreme
  * AP3912i
  * AP3935i
* FortiAP
  * 221E
* Huawei
  * AP160
  * AP263
  * AP362
  * AP661
  * AP761
  * AirEngine 5776-26
  * AirEngine 6776-57T
  * AirEngine 6776-56TP
* LANCOM
  * LX-6200E
* Ubiquiti
  * U7 Pro Max
  * U7 Pro Wall
  * U7 Pro Outdoor
  * WiFi BaseStation XG
* Ventev
  * VN-VLHM6-XD
  * VN-XLHM6-XD
* Zyxel
  * WBE530
  * NWA130BE
* We cleaned up the Ubiquiti access point names, so they all have a consistent naming convention in Hamina Network Planner.
* As part of the new access point modes feature, we added a Custom Antenna mode to the Ubiquiti UniFi AC Mesh.
* We corrected the orientation of the Ventev M6060040O1D42420L. Thanks to Dennis and Nick for the heads-up!

### 2024/06/19

**Improvements**

* We added the **Channel utilization** heatmap to the Live View. It's pretty nice to see how busy each coverage cell is!

**Bugfixes**

* If you touched anything in the Live View, or even moved your mouse, the Live View heatmap would re-render that. Fixed!
* As part of the PDF generation speed improvements we made yesterday, we bumped the PDF image resolution up a little bit.

**APs and Antennas**

* Aruba AP-735

### 2024/06/18

**Improvements**

* Included in today's production push is a <mark style="color:red;">**Feature Preview**</mark> for the new Live View in Hamina Network Planner Plus! _Note: This features requires a Hamina Network Planner Plus subscription._
*   The **Live View** connects to your Arista, Juniper Mist, or Cisco Meraki cloud to synchronize maps, access points, channels, transmit power, clients per radio, and switches to Hamina Network Planner, and appears as a new tab at the top of Hamina Network Planner.\


    <div align="left">

    <figure><img src="../.gitbook/assets/live-view (1).png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   To enable it, visit the menu in the upper right, click **Edit account**, click the **Feature preview** tab, and enable **Live Analysis of Meraki, Juniper Mist and Arista**. Then, click on the **Live** tab at the top, where you'll be directed to connect Hamina to your cloud infrastructure.\


    <div align="left">

    <figure><img src="../.gitbook/assets/connect-to-infra.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   With Juniper Mist and Arista, it also measures attenuation between access points to create **Environment learning** of obstacles in the map to draw more accurate heatmaps, all without drawing any walls! To try this out, start a project with a fresh map with no walls. Then, copy the APs from the Live tab, and paste them in the Simulation tab. Then, drag the APs around to see how their coverage changes, based on the Environment learning.\


    <div align="left">

    <figure><img src="../.gitbook/assets/environment-learning.gif" alt="" width="240"><figcaption></figcaption></figure>

    </div>
*   To go along with Environment Learning, there's also a new checkbox in the **Adjust requirements** pane called **Auto-select prediction input**. You can turn this off, and manually choose Hamina's inputs for prediction in both the Simulation and Live tabs. **Environment type** applies a blanket of attenuation across the map, based on the environment type defined in the Project settings. **Walls + objects** is what most of us are used to, as it simulates good ol' free space path loss, loss from walls, and loss from attenuating objects. Finally, there's **Environment learning**, which comes from the measurements taken from the infrastructure in the live view. Setting this to **Auto** will always prefer **Walls + objects**, with **Environment learning** next, and **Environment type** last.\


    <div align="left">

    <figure><img src="../.gitbook/assets/simulation-input.png" alt=""><figcaption></figcaption></figure>

    </div>
* Previously on mouseover, Hamina Network Planner only showed one access point. In the **Adjust requirements** pane, there is now a **List all APs on mouseover**, which does that exact thing.
*   We updated the toolbar behavior a bit - now there's a small button for the pop-out menu, which paves the way for another tool that's coming soon. 🤫\


    <figure><img src="../.gitbook/assets/new-button.png" alt=""><figcaption></figcaption></figure>
* PDF generation for for simulated networks is much, much faster now. Seriously. ⚡
* Added `EMEA-02` region to the Juniper Mist Import, Export, and Live Views.
* Added `US-WEST-5`, `US-EAST-1`, and `UAE-NORTH1` regions to the Aruba Import.

**Bugfixes**

* In the frontend, it looked like a non-admin on a team could change someone's permission. They couldn't (the command would quietly fail in the back end), but we made it so it doesn't _look_ like it works.

**APs and Antennas**

* Aruba InstantOn AP32
* Netgear WBE710
* Ubiquiti U6-Mesh-Pro
* Ubiquiti U7 Pro
* Rigado Cascade 500
* TP-Link EAP683 LR
* TP-Link EAP773
* TP-Link EAP783
* There were a couple of problems with our implementation of the Aruba AP365 (such as orientation), so we fixed it.

### 2024/06/05

**Improvements**

* Remember the pipeline from last week? This production push builds on that to introduce Fast Ray Tracing, which provides simulation of reflections and diffractions!
* To activate FRT (Fast Ray Tracing), Hamina Network Planner Plus users can click the FRT button on the right of the map view, which will do a one-time ray-tracing calculation for the design. If we need to recalculate the heatmap and any reason, it will reset to a non-FRT calculation. You can click the FRT button whenever you like. Watch those shadows behind concrete pillars melt away! _Note: Fast Ray Tracing is only available for Hamina Network Planner Plus users. It is not currently available in web-based or PDF-based reports._
*   As part of FRT, there is a slider to adjust the intensity of simulated diffraction and reflection effects. Adjust it to "High" for more reflective environments.\


    <div align="left">

    <figure><img src="../.gitbook/assets/frt-slider.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
*   There's also a new **Auto-select prediction input** toggle. Previously, behind the scenes, the **Environment type** setting in in the **Project settings** applies blanket attenuation to the project based on the environment type, until you draw walls and attenuating objects. Now, you can select which you want to use. While this option doesn't do a lot today, it paves the way for our upcoming **Environment learning** feature. Stay tuned!\
    \


    <div align="left">

    <figure><img src="../.gitbook/assets/environment-type.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
* The requirement for multi-factor authentication has been waived for Hamina Network Planner Lite users.
* The 3D antenna viewer is now available in Hamina Network Planner Lite! You're welcome.
*   Previously, the mouseover inspector only showed BSSIDs, which was hard to read. Now, it shows resolved AP names!\


    <div align="left">

    <figure><img src="../.gitbook/assets/resolved-mouseover-inspector.png" alt="" width="372"><figcaption></figcaption></figure>

    </div>
* We now only allow positive values in coordinates for OpenIntent exports.
* The survey interference heatmaps seem to be working great, so we removed the "Beta" label from them.

**Bug Fixes**

* If you drew a map on your Macintosh SE/30, and found that it doesn't work in Hamina Network Planner, then congrats! 🎉 You found the greyscale map bug! That's been fixed. _Note: To be clear, absolutely nobody found the bug like that._

**Access Points**

* Galgus IC450, OC400, OC410, IX450, IX850, and OX451
* Huawei AirEngine 5573-23HW, 8760R-X1, 8760R-X1E
* Ventev M6060040O1D42420L
* EdgeCore EAP111
* AccelTex ATS-OO-2456-344-4 and ATS-OP-2456-477-4

### 2024/05/29

**Improvements ✨**

*   Hamina Network Planner now features a simulated pipeline for heatmaps, which our CTO Jarno Harno says improves performance and enables some fancy stuff like cancelling the generation of a heatmap. Here's a totally real photo of Jarno, working on the simulated heatmap pipeline.\


    <div align="left">

    <figure><img src="../.gitbook/assets/jarno-pipeline.png" alt="" width="345"><figcaption></figcaption></figure>

    </div>
* Related to our new pipeline: we're smarter about only doing calculations where necessary in and around Scope Zones.
* Here's another one that's related to the pipeline. You've probably noticed that Hamina calculates successively higher and higher resolution heatmaps in the background while you work (which is part of how we keep everything super fast and real-time). Now, we smoothly animate between the heatmaps, as the higher-resolution maps are calculated. This is happening on your GPU, so it's basically free from a computing perspective. _Note: You can see this in action in the GIF below._
*   See the impact of a switch failure with **Blast Radius**. Clicking on a switch (with a heatmap enabled) shows the heatmap for all of the APs connected to that switch to see what it is covering. You can inverse this by selecting all of the switches on the map and then `Shift` + clicking a switch to remove it from selection, visualizing the blast radius of the switch going down.\


    <div align="left">

    <figure><img src="../.gitbook/assets/blast-radius (2).gif" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   In the survey tab, you can now remove AP locations. This doesn't remove the AP from the survey data or anything, it just basically says, "Don't place this AP here, or anywhere." Of course, you can always put the AP back on the map with the Place AP option that we introduced a couple of production pushes ago.\


    <div align="left">

    <figure><img src="../.gitbook/assets/hide-ap.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   Previously for surveys, virtual SSIDs would only be shown in the **Edit Access Point** pane if they were selected in the heatmap drop-down menu. Now, we display all of the virtual SSIDs that the AP is broadcasting, whether they are selected or not.\


    <div align="left">

    <figure><img src="../.gitbook/assets/virtual-ssid-visibility.png" alt=""><figcaption></figcaption></figure>

    </div>
* We implemented a new progress indicator at the bottom center of the map viewport. For some reason, this was internally called the "Snack Bar", probably because it's a progress bar, and it was a small change. Like a snack. So, a "Snack Bar".
* The new progress indicator now appears when loading survey results. On a small survey, you'll barely see it, but it can take a little while if the survey is really big.
* Uh-oh, missed your payment? No worries, we now give you an extra two weeks to talk your accounting team or purchasing agent. Everyone using the overdue subscription will get a reminder in the notification area each day, so it doesn't surprise anyone when it stops working.
* We added band n79, which is a TDD band spanning from 4400 to 5000 MHz.
* Hamina Network Planner now supports 6 GHz MBSSID (Multi BSSID) elements in beacons.
* We updated `OUI.csv`, which is a list of which OUI (the first three nibbles of a MAC address) belong to which vendor. We use this to identify AP vendors, and to properly group virtual SSIDs together.
* Hey, 'member Mojo access points?! We 'member! Now they show up as "Arista".
* We updated the text on the project start page. It's all the, small things. 🎸
* Totally in the background: we moved a bunch of functions into container applications that automagically start and stop as needed, which makes our cloud more scalable and easier to maintain. Plus, we can say that Hamina uses "microservices" or whatever. Next, we need to figure out how to shoehorn "AI" into this thing...

**Bugfixes 🚫🪲**

* There was an issue where setting a new channel width wouldn't affect other floors on the building. We've corrected that now!
* The Juniper Mist AP45 5/5/6 now correctly maps to the AP45 in exports to the Juniper Mist Cloud.
* There was a bug that would cause the map to be waaaaaaaay zoomed out when you switched to it. That's fixed!

**APs and Antennas 🏗️**

* Askey EAO2522P
* ASUS EBA63
* Cambium X7-35X
* Cisco CW-ANT-D1-NS-00
* Extreme AP5020
* Extreme ML-2452-SEC6M4-036
* Huawei AirEngine 5773-21
* Huawei AirEngine 5773-22P
* Huawei AirEngine 5573-23H
* Huawei AirEngine 5573-23HW
* KP Performance KP-3QOMNI-8
* MosoLabs Canopy 5GOD1 (External)
* Nokia AWHTA 5G AirScale Micro
* Ruckus R350e
* Ruckus R670
* Ruckus T670
* Sunwoo Sector 17dBi
* Ubiquiti U6 In-Wall
* WAVE GAWiFi6E4OV1
* Ventev M6080080P1D436
* Corrected an issue with the Ruckus T750SE, which now defaults to a wall mount.
* We fixed the capitalization on the Ruckus T350SE and T750SE.

### 2024/05/10

**Improvements** 😵‍💫

*   Hamina Network Planner now includes an Interference heatmap for surveys! In the **Adjust Requirements** Pane, you can adjust some of the specifics for the heatmap. Most notably, you can show interference for **My network** or **All networks**. The Interference heatmap is currently in beta and will likely see some changes and bugfixes in the coming weeks.\


    <div align="left">

    <figure><img src="../.gitbook/assets/interference-heatmap.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   You can also adjust the **Guess range** for surveys. We recommend keeping your survey paths fairly close together, only adjusting the Guess range to higher numbers to fill in gaps.\


    <div align="left">

    <figure><img src="../.gitbook/assets/guess-range.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   You can manually disable radios! Has Hamina gone too far?! 🤯 To use it, right-click the channel labels underneath the access point and select **Disable Radio**.\


    <div align="left">

    <figure><img src="../.gitbook/assets/disable-radio.png" alt="" width="362"><figcaption></figcaption></figure>

    </div>
*   This marks our first release with support for OpenIntent importing and exporting! It won't import and export everything about the project, but the basics are there. Expect to see more iterations on this feature soon.\


    <div align="left">

    <figure><img src="../.gitbook/assets/export-openintent.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
* Importing from Mist now includes the AP orientation and height. Convenient!
* Bitmap background images are now processed with fancy new cloudly cloud stuffs. They're a bit faster now, and easier for us to maintain.

**Bugfixes** 🐛

* In online and PDF reports, in the AP List, the order that we listed access points looked random. We added some logic to sort the list by floor, and then AP number per floor. In the online reports, you can still click the columns to reorder them on the fly.
* There was a teeny tiny bug that could cause a subscription to show up in Hamina Network Planner. Small, but bad. We squished that one!

### 2024/04/29

**Improvements 💫**

*   Once a license has been activated by a user for at least 90 days, the subscriber (who has a list of users who have activated their keys) can release their license! This is useful if someone leaves the company, moves to a different role, or if the team just plain needs to move the license to someone else.

    <div align="left">

    <figure><img src="../.gitbook/assets/release-license (1).png" alt="" width="319"><figcaption></figcaption></figure>

    </div>
*   If an access point wasn't loud enough for us to automatically place it, you can now right-click on the map with the **Edit** tool and click **Place access point**. The list respects any filters that you have an place, and will show a heatmap for the access point as you mouse over it.\


    <div align="left">

    <figure><img src="../.gitbook/assets/place-access-point (1).png" alt="" width="317"><figcaption></figcaption></figure>

    </div>

**Bugfixes 🪲**

* We found a corner case where survey measurements might not synchronize properly, and got it fixed.
* If there were multiple photos in a note, the full-screen image viewer would switch back to the first image if you nudged your mouse. We fixed that.
* One of the selectable map note icons was broken, so we fixed that too.
* The Meraki MR86 was erroneously marked as an indoor AP, which caused the description in the bill of materials to be incorrect. It is now marked as an outdoor AP.
* In the external antennas list, we corrected "NetGear" to "Netgear".

**APs and Antennas 🛰️**

* Cradlepoint A2415
* Fortinet 421E
* Ubiquiti U6 Enterprise In-Wall
* Intelbras AP5626
* HFCL ion12xi
* HFCL ion4xi\_WP
* We also updated the antenna pattern for the Acceltex ATS-OHDP-245-1312-6

### 2024/04/11

**Improvements ✨**

* Surveyed AP selections persist when you switch floors, so now you can see what other floors an access point (or multiple access points) was audible on. When an AP on another floor is selected, you'll see an **Adjacent floor measured access points** filter applied at the top.
* When importing an Arista network, we now include import the transmit power and current channel for each AP radio.
* In the **Project Settings** menu, we renamed **Remove** to **Delete project**.
* We made some minor improvements to the styling in the Teams dialogue.

**Bugfixes 🪲**

* There was a bug that caused the Legend to always say 5 GHz, even if 2.4 or 6 GHz is selected. Oops. No more!
* When viewing site surveys, there was a bug that would sometimes cause the access point details pane to be mostly empty. We fixed it!
* In Hamina Network Planner Lite, we now show an **🔒 Upgrade** tag next to the **Duplicate floor** option, to show that you can't do it without a Planner or Planner Plus subscription.
* The drop shadow was missing from the Layers menu button, so we added it back in.
* There was a strange bug where if you placed a big **Out of Scope zone**, and drew a small **In Scope zone** inside of it, everything would turn green (even if there were no access points). Weird, but fixed!

**APs and Antennas 📻**

* Gamma Nu IOAOXY2FLAT\_MIMO
* Extreme ML-2452-HPA5-036
* AccelTex:
  * ATS-ID90RD-245-23-1
  * ATS-ID90RD-245-46-1
* L-com HG3513DP4-NF
* JMA Wireless IV02OMI136-M4
* KP Performance:
  * KP-3DP120S-45
  * KP-3DP33S-45
  * KP-3DP65S-45
  * KPP-3SX4-65
  * KPPA-3GHZDP90S-45
  * KPPA-3GHZ-DPOMA
* Aruba (omnidirectional antennas):
  * AP-ANT-311
  * AP-ANT-312
  * AP-ANT-313
  * AP-ANT-340
  * AP-ANT-320
* Aruba (directional antennas):
  * AP-ANT-345
  * AP-ANT-348
  * AP-ANT-325
  * AP-ANT-328
* Netgear WBE750
* Netgear WBE758
* We also updated the antenna pattern for the Meter MW08

### 2024/04/03

**Improvements 🥳**

*   This release adds the option to generate stairs in sloped floors! The stair sizes are based on the scale of the map, and are purely cosmetic (they don't affect the predictive model at all). To enable them, just click the **Draw stairs** option in the **Edit Sloped Floor** pane.\


    <div align="left">

    <figure><img src="../.gitbook/assets/stairs.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   In the last release, we stacked the **Top height from floor** and **Bottom height from floor** boxes for the wall type editor. In this release, we gave the Attenuating object type editor the same treatment.\


    <div align="left">

    <figure><img src="../.gitbook/assets/attenuating-object-editor.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
* We added map notes images to reports!
* If you duplicate a project, the note images will now be duplicated along with it.
*   In the Survey tab, when selecting multiple radios, we don't try to show all of the radio details anymore. Instead, we'll just show you the stuff that you might want to bulk edit, like the AP height and model.\


    <div align="left">

    <figure><img src="../.gitbook/assets/ap-multiselect.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
* Hamina Network Planner Lite (aka "free tier") users can now adjust heatmap settings.
* The cyan, orange, and purple colors that we were using didn't have very much contrast (and didn't match our designs), so we fixed those up. We also fixed and improved some other styling around the app.
* We used to show a separate toast notification for each PDF page that was uploading. Now, we just show one toast for the entire file. 🍞

**Bugfixes** 🪲

* There was an issue where some users could get stuck in an endless loop while logging in if they have multiple accounts, which could cause them to get stuck in an endless loop while logging in, if they have multiple accounts, which could cause them to get stuck in and endless loop while logging in...
* There was another loopy login bug, where if you clicked **Cancel** on the MFA page, you'd get stuck in one infinite loop.
* There was a bug where if you have only an Onsite license (a common scenario, especially for people who only do surveys and don't need to create designs), you'd still see the **Upgrade** button towards the upper right. That was confusing to people who only subscribe to Onsite, so we fixed it.
* In the AP Radio Details page in the Report Editor and Viewer, radios now correctly say "Off".
* On the **Subscriptions** page, under **Your licenses**, users with Hamina Network Planner Lite (basically, anyone without a paid Network Planner or Network Planner Plus subscription) would see **Free evaluation**. We're calling it **Hamina Network Planner Lite** these days, so we fixed it.
* There was a bug where sloped floors didn't take out-of-scope zones into account. That's been taken care of.
* Routers were missing from the BoM. They aren't missing from the BoM anymore.
* There was a weird bug where if you placed an IDF or MDF without any switches or power, it would show a warning icon on the map.
* Previously, if you started the project notes with an image, the Save button would be disabled. That's fixed now - feel free to begin your notes with a logo, or whatever you like!
* If there wasn't enough room, or if the browser size was too small, some of the submenus would get really weird. They behave normally now.

**APs and Antennas** 📡

* Eero PoE 6
* Eero Max 7
* Ventev M6060060P23602NBC
* Ventev M6040040P23602
* Ventev M6060060P1D43602M
* Ventev M6130130MP1D3607D
* Ventev M6060060D3D43699
* Ventev M6060060P1D43699D
* Nomadix AP-6NA
* Calix u6t
* Calix u6txg
* Aruba AP-305
* Aruba Instant On AP-12
* Fortinet AP-432G
* Meraki MR42E
* Meraki MR45
* Meraki MR84
* EnGenius EWS377AP
* Juniper AP45 in 5/5/6 mode
* Cisco IW-ANT-PNL25610-R antenna
* Extreme 7532-67040 (which is the external antenna version of the 7532)
* Edgecore OAP101
* Celona AP-11 2-sector mode
* Added Zigbee patterns to the Ruckus H510, R550, R650, R850, and T750

<figure><img src="../.gitbook/assets/APs.png" alt=""><figcaption></figcaption></figure>

**Known Issues** 🫢

* If you place the Celona AP-11 in 2-sector mode without defining an antenna, it will be stuck with a default antenna that you can't change. If you pick the antenna before placing it, it works fine. We didn't catch this one until it was out the door, so we'll fix it in the next release.
* The Meraki MR86 is marked as an "Indoor" AP, when it is in fact an outdoor AP.

### 2024/03/13

**Improvements ✨**

*   Floor duplication is now a thing that exists in Hamina Network Planner!\


    <div align="left">

    <figure><img src="../.gitbook/assets/duplicate-floor.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   AP labels on the map! Now, in the **Layer Visibility** menu, you can turn Labels on and off, and switch them between **Numbers** and **Names**. We don't have this on the reporting side yet, but we will soon.\


    <div align="left">

    <figure><img src="../.gitbook/assets/labels (1).png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   The **Mouseover inspector** in the **Heatmap legend** now works in the **Survey tab**! Inspect all of the things!\


    <div align="left">

    <figure><img src="../.gitbook/assets/mouseover-inspector.gif" alt="" width="408"><figcaption></figcaption></figure>

    </div>
*   BLE radios (like the Mist BT11) have a Bluetooth logo now, and it looks pretty slick! Wi-Fi and RTLS wired clients have shiny new icons, too!\


    <div align="left">

    <figure><img src="../.gitbook/assets/new-icons.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   Previous, in the wall profile editor, the **Top height** and **Bottom height** text boxes were next to each other, and we confused them almost every single time we edited a wall profile. We couldn't stand it anymore, and raised the issue with our UX guy, and he totally, totally fixed it. The **Top height from floor** and **Bottom height from floor** input boxes have now been stacked, and have handy diagrams that show exactly what they do! 👏\


    <div align="left">

    <figure><img src="../.gitbook/assets/top-height-bottom-height.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   **High quality graphics** and **Transparency effects** are now available in the **Report Editor**. The settings will mirror whatever you're using the main web app.\


    <div align="left">

    <figure><img src="../.gitbook/assets/high-quality-reporting.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
* We made some improvements to the **Shared Report Viewer** (the one that your customers see when you send them a link), too! It hasn't received the transparency and shadow effects yet, but we did add outlines to make things look nicer. We're planning to revisit this soon.
* The maximum zoom level is now based on the map scale, instead of being tied to the background map resolution. If you're trying to do precise things like select co-located access points and precisely draw walls, this should make things much easier.
* Project invitation and team invitation links now take 30 days to expire, instead of two days like before.&#x20;
* For surveys, we improved our AP location estimation a bit.
* If you open a photo note, full-screen a photo, and press **`Esc`**, we now close just the full-screen photo, instead of closing the entire note.

**Bugs** 🐛

* If you had a Hamina Network Planner subscription, and activated a Hamina Onsite subscription, there was a weird bug that would deactivate Network Planner. Not anymore!
* We improved automatic BSSID grouping for Juniper Mist and Cisco access points.
* Email addresses for team invitations are now case-insensitivie (just in case uppercase letters sneak into your email addresses).

**APs**

* The CW9163E was available in Cisco before, but it shows up under Meraki now as well.

**Known Issues** 😅

* Routers don't appear in the BOM. Fix coming soon!
* The weird issue with sloped floors being backwards is still there, but we haven't been able to reliably reproduce it. We might put it in the back burner for now.

### 2024/03/06

**Improvements 🍻**

*   We've added a new "Teams" feature to Hamina Network Planner! In the **Account** menu (in the upper right), visit the Teams view to create teams, manage who is part of your team, and manage their permissions. Critically, when you share a project, you can share it with an entire team!\


    <div align="left">

    <figure><img src="../.gitbook/assets/team-shared-project.png" alt=""><figcaption></figcaption></figure>

    </div>
*   When viewing the results of a survey, Hamina won't show an access point on the map, unless we hear it above -60 dBm. In Hamina Network Planner, you can now manually show and place an access point by selecting the **Edit** tool, right-clicking on the map, and selecting **Place Access Point**. Then, you can select the SSID and BSSID of the AP you'd like to place. A manually placed access point won't automatically update if you add more survey data.\


    <div align="left">

    <figure><img src="../.gitbook/assets/place-access-point.png" alt="" width="322"><figcaption></figcaption></figure>

    </div>
* Previously, the raised and sloped floors feature tried to be smart about what default heights to use;  when drawing a new area, the heights would be inherited from other areas. We think it was a pretty good idea, but in practice, it ended up just being confusing. Now, just like with access points and switches, when you draw a new sloped or raised floor, we just copy the values of whatever you last selected.
* Previously, if you placed a Wall/Pole mounted AP within 0.7 meters (2.3 feet) of a wall, it would automatically point away from the wall at a 90° angle. We've increased the threshold to 1 meter, so you don't have to click quite as precisely when you place the access point.
* Attenuating objects were visible in the Survey tab when viewing in 3D. Since Attenuating objects don't affect the survey data, we removed them from the survey 3D view.

**Bug Fixes 🐛**

* In the Survey tab, if you selected some SSIDs and switched to a different floor, the heatmap breadcrumbs would show the wrong amount of selected SSIDs. It's a small bug, but we fixed it.
* We found and fixed a bug where some APs in survey reports were missing some data, such as channels and names.
* Mesh links wouldn't survive project duplication. Now, when you duplicate a project, mesh links are preserved!
* If a survey path point was deleted in Planner, and then the delete was undone, the survey path wouldn't appear back in the Onsite app. Fixed!

**Known Issues 🔍**

* When drawing sloped areas, Hamina Network Planner is supposed to draw the low side first. For some reason, sometimes the first side drawn ends up being the high side of the slope. We'll investigate that and get it fixed.

### 2024/03/01

**Improvements ✨**

* You can now create online reports for surveys! This initial release includes Survey Paths, AP Placement, Coverage, Secondary Coverage, and SNR heatmaps. PDF reporting will follow soon, along with more heatmaps.
* We made how we read survey measurements a bit more efficient. It's pretty technical stuff, so don't worry about it too much. Just know that things should be a bit faster now.
* In Hamina, whatever access point you selected last will be duplicated when you place more APs. Previously, this was partially true for switches as well, but it would break when you switched maps/floors. Now, the previous switch settings will persist when you switch to another floor.
* Before this production push, we always calculated propagation across the entire map, regardless of what was in or out of scope. Now, we ignore areas that are outside of the scope zones, so things compute more faster-er.

**Bugs 🪲**

* Previously, Onsite users couldn't adjust heatmap thresholds due to a licensing bug. Not anymore.
* In the **AP Radio Details** list in reports, the **Tx Power (EIRP)** field was incorrect, due to a calculation bug. That's fixed now!

### 2024/02/20

**Improvements** 🔧

* If you place a Wall/Pole mounted AP within 0.7 meters (2.3 feet) of a wall, it will automatically point away from the wall at a 90° angle! We hope that saves you a lot of time manually pointing antennas around.
* You can now use **`Option`** + **`C`** (macOS) or **`Alt`** + **`C`** (Windows) to open the Channel and Network Settings!
* We inverted the direction that the map moves with the arrow keys, which feels a lot more natural.
* Opening the heatmap settings (Requirements pane) doesn't de-select APs anymore, which is nice if you want to make small adjustments while looking at a set of specific APs.

**Bug Fixes** 🔨

* There was a bug that would break photos in notes if you didn't have a Hamina Onsite subscription. Oops! It's fixed now.
* We squished some more bugs, but they were all related to upcoming features that aren't available yet. 🤫

**New APs and Antennas** ✨

* Celona AP-13 and AP-13E
* Meraki MR53 and MR74

### 2024/02/13

**Improvements 🎉**

*   It has been possible to view antenna patterns for internal antennas on access points for a long time, but only after pressing a cryptic keyboard shortcut. Now, you can enable the antenna pattern viewer for access points in **Edit account**.\


    <div align="left">

    <figure><img src="../.gitbook/assets/antenna-viewer-option.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   Once that is enabled, you can mouse over access points to see their antennas.\


    <div align="left">

    <figure><img src="../.gitbook/assets/internal-antenna-viewer.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
* We applied some more performance improvements to Survey mode. There are still some more things to do, but we're moving things in the right direction. 👍

**Bug Fixes 🤦‍♂️**

* If the heatmap was turned off (set to **None**) in Simulation mode, then the heatmap legend would not re-appear in Survey mode (even when you turned the heatmaps back on). That's fixed!
* We got the orientation of the MP Antenna 1039 and 1041 wrong, but it should be fixed now! Thanks Jeremy for the heads-up about this, and be sure to check out his recent appearance on [The Industrial Wi-Fi Shop podcast](https://industrialwifishop.com/2024/01/15/the-industrial-wi-fi-shop-podcast-ep-2-industrial-wireless-safety-mobility/).

**New APs and Antennas**

* Alta AP6 and AP6 Pro
* MosoLabs Canopy 4GID1 (4G Indoor), 4GOD1 (4G Outdoor), 5GID1 (5G Indoor), and 5GOD1 (5G Outdoor)
* Fortinet 441K and 443K

### 2024/02/05

**New Features** 📷

*   Photo notes are here! Now you can now view photos that were added from Hamina Onsite, as well as upload, download, and remove photos. _Note: We don't have project duplication or copy/paste for photos in notes supported quite yet, but we'll get them taken care of soon._\


    <div align="left">

    <figure><img src="../.gitbook/assets/photos-in-note (2).png" alt="" width="375"><figcaption></figcaption></figure>

    </div>

**Improvements** 🔧

* We removed the scale marker from the 3D view, which was only correct for 2D and doesn't apply to 3D very well. Just what you want to see, _less_ features for your money!
* We worked on ther performance of the Survey tab and Survey Paths pane, especially when viewing larger surveys. We think there's more we can do to improve this, but we made good progress.

### 2024/01/30

**New Features 🎉**

*   In this update, we've introduced transparent walls, transparent attenuating objects, and a high-quality graphics mode! Check it out!\


    <div align="left">

    <figure><img src="../.gitbook/assets/high-quality-graphics.png" alt=""><figcaption></figcaption></figure>

    </div>
*   **High quality graphics** and **Transparency effects** can be enabled in the **Edit account** menu. There is a performance impact from these, so experiment with your machine to see how it does. We'd also recommend not having a bunch of Hamina tabs open at once, as it does consume more RAM. That said, it works pretty well for us, even on modest machines.\


    <div align="left">

    <figure><img src="../.gitbook/assets/edit-account-3d.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   For both Walls and Attenuating objects, you can enable or disable transparency for each material type.\


    <div align="left">

    <figure><img src="../.gitbook/assets/transparent-setting.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   In addition to just looking cool, we think transparency will be helpful for tall warehouse shelves, and also for situations where you need to see a heatmap under the material, like this custom ceiling Attenuating Object that we made for this warehouse.\


    <div align="left">

    <figure><img src="../.gitbook/assets/transparent-ceiling.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
* We applied some more smoothing to the survey heatmaps. They're 0.42% smoother. Or was is 4.2%, or 42%?&#x20;
* The Survey tab now supports 3D mode, which is nice for visualizing heatmaps in buildings with raised floors, sloped floors, and holes in the floor.
* The selected heatmap, band, and SSID are now saved to the project, and synchronized between Hamina Planner and Hamina Onsite.
* In 2D mode, a **Floor holes** area no longer masks the heatmap, if the **Floor holes layer** is hidden.

**Improvements** 🔧

* Previously, if you disabled Note visibility in Simulation mode, and then switched to the Survey tab, you couldn't see the notes anymore without switching back to the Simulation mode to re-enable them. Now, they're always visible in the Survey tab. We'll add fine-grained layer visibility to Survey mode soon.
* In Hamina Onsite and Hamina Network Planner, we don't try to place an AP on the map, unless we're pretty confident that we know which map it should be placed on (such as in a multi-story building).
* Previously, if you used the Edit tool to select an area, it would select invisible APs. Now, the Edit tool only selects visible APs.
* We improved the appearance of heatmap contours on low-resolution displays.
* When exporting to ExtremeCloud and creating a building, you can now input the building's country, which is required by the ExtremeCloud API.
* In the Survey tab, Coverage is now the default heatmap.
* Cisco Catalyst (DNA) Center is now available directly in Export! It's marked as "Beta", since we're still fine-tuning it.

**Bugfixes 🪲**

* There was an issue where switching AP models could cause the direction arrow to disappear. We fixed it!
* We fixed an issue where switching the mouse mode (mouse/trackpad) in shared reports would cause the page to reload.
* There was a minor bug in our authentication code that was causing us to ask you to log back in way too often. We fixed it, so now you don't have to log in nearly as often. Sorry about the hassle!
* We fixed the Netgear 630, which wasn't implemented correctly in our AP database. Now in Hamina Planner, it supports dual 5 GHz with the correct channel selection limitations.

**New APs and Antennas**

* We added dual 5 GHz mode for the Fortinet 231G, which appears as Fortinet 231G (2.4/5/5).
* We added dual 5 GHz mode for the Fortinet 431G, which appears as Fortinet 431G (2.4/5/5).
* Fortinet 233G Custom, 234G, and 432FR.
* Fortinet FANT-02ACAX-0606-P-R.
* Ruckus T300, T301n, and T301s.
* Ruckus T710o and T710s.
* Mist AP64.
* CyberTAN EWW631-B1.
* Extreme AP650.
* Acceltex ATS-OO-2456-466-4.
* AccelTex ATS-OP-2456-81010-4.
* Ventev Nano Patch M6060060D3D36.

### 2024/01/15

#### Features and Changes

*   We added an all-new feature for constructing doors and windows: **Top and Bottom Fill**. For walls with a custom lower or upper height, the empty space will be filled with whatever wall type is on either side of it. For example, if you draw a door on a brick wall, the empty space above the door will now be filled with Brick.\


    <div align="left">

    <figure><img src="../.gitbook/assets/top-bottom-height.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>
*   Here's an example in a pretty standard building, in this case a small medical clinic. The doors and windows are drawn in like standard walls, and the **Fill top & bottom** setting takes care of the rest. We've added all of the correct profiles for new projects, so this will work out-of-the box. There's still a floor-to-ceiling **Glass** profile for fancy conference rooms.\


    <div align="left">

    <figure><img src="../.gitbook/assets/3d-building (1).png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
*   Here's the window and door effect in a warehouse. Notice that even though the Concrete walls are pretty tall, the Windows are still at the correct height, because of the static **Top height** and **Bottom height** settings. Note that everything you see is included in the predictive model, so your models will be a tiny bit more accurate now, too.\


    <div align="left">

    <figure><img src="../.gitbook/assets/3d-warehouse (1).png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
* When Importing access points, they are now "Not Connected" by default.
* We no longer fetch survey data until you switch to the "Survey" tab.

#### Bugs

* There was a bug where you couldn't select notes in the Survey tab. That's fixed now.
* If two measurements were in the exact same location, some strange visual artifacts could occur. Fixed!

#### New APs and Antennas

* MP Antenna 08-ANT-1072.
* Aruba AP-584, AP-634, AP-635, AP-654, and AP-655.
* Alcatel OAW-AP1321, OAW-AP1322, OAW-AP1331, OAW-AP1361, OAW-AP1361D, and OAW-AP1362.
* Extreme ML-2452-APA2-02.
* Siemens ANT793-8DJ and ANT793-8DL.

### 2024/01/10

#### Features and Changes

* When using the Export feature, with the "Match by name" selected, Hamina Planner will now attempt matching unassigned APs by name, instead of randomly assigning them.
* We made some other model matching improvements.

### 2024/01/09

#### Features and Changes

* Previously for measured data, the heatmaps would fade to red near the edges, suggesting that signal strength wasn't as good there. This has now been corrected; the heatmaps now have a clean cut at the edges without a color change.
* We adjusted the default heatmap thresholds. For Primary Coverage:
  * Green: -65 dBm
  * Yellow: -70 dBm
  * Red: -75 dBm
* For Secondary Coverage:
  * Green: -67 dBm
  * Yellow: -70 dBm
  * Red: -75 dBm
* For SNR:
  * Green: 25 dB
  * Yellow: 20 dB
  * Red: 15 dB
* The Secondary Coverage and SNR heatmaps are now available for measured data.
* For the various integration/import/export features in Hamina Network Planner, we renamed "Meraki" to "Cisco Meraki".

#### Bugs

* Fixed a bug where the channel optimizer wouldn't re-run when switching AP models.
* The Cisco 3802 was labeled as "Wi-Fi 6", which is not correct. Now, it says "Wi-Fi 5" in the BOM, like it should.

### 2024/01/04

Happy New Year! 🎉

#### Features and Changes

* Aruba, Hewlett-Packard Enterprise, and Hewlett Packard OUIs have been combined and grouped as "Aruba" (which, looking at this a few weeks later, is pretty funny).
* Cisco and Cisco Systems are now grouped as "Cisco".
* When switching between the Simulation and Survey tabs, the viewport location and zoom does not change, and the map doesn't reload, which makes it easy to flip and back and forth between Simulation and Survey for comparison purposes.
* Previously, moving or deleting survey points wouldn't update AP locations without refreshing the browser. Now, the AP locations update without a refresh.

#### Bugs

* Previously, you couldn't activate an Onsite license without a Planner license. That is fixed now.
* Pressing Ctrl+C to copy something would change all of the selected walls to whatever button "C" was bound to (which was usually Concrete). This is fixed - you can now safely copy a bunch of walls without turning them into stone. Well, concrete.
* There was a weird bug where the channel planning could try to set an 80 MHz channel in 2.4 GHz, which would cause a small crash. Ha, whoops. Fixed now.

### 2023/12/21

One last production push of the year, and right before Christmas! 🎅🌲🎁 This one contains a bunch of stuff, so we'll break it up into categories a little bit. ❄️⛄🎄

#### Features and Changes

* **Vendor Integrations**
  * Cisco Catalyst (DNA) Center users can now define an existing hierarchy with building and areas (with multiple nested areas) when exporting a Cisco Catalyst XML file.
    * If there isn't a hierarchy defined in Cisco Catalyst Center, it can be exported as as separate CSV file.
    * The building name defaults to the Hamina project name, but this can be overridden.
  * Added APAC01 region to Juniper Mist.
* **Client View**
  * Added a scroll bar to the Client experience pane.
  * When the Client View is activated, the heatmaps are now automatically hidden, but you can show them again by unchecking **Show association area** in the **Client experience** pane.
  * In the **Survey paths** pane, the newest surveys are now at the top, making them the easiest to find.
  * In 3D, if the client height is changed, the "Roaming Man" in the Client View now has a vertical line to show it's precise location on the ground.
  * The maximum client height is now tied to the height of the current floor.
* **Folder Behavior**
  * To prepare for our upcoming team project sharing features, we converted the concept of "Folders" to "Tags". With this change, we are able to drastically simplify the development and usage of the team project sharing feature.
    * As part of the conversion from "Folders" to "Tags", when you tag a project and share it, the person you are sharing with will see the same tag structure as you.
    * Conversely, if someone shares a tagged project with you, you'll see the tag structure as well.
* **Surveys**
  * We show the location of measured APs if they exceed -60 dBm.
  * For users with Hamina Network Planner subscriptions, the Survey tab only appears if the project contains survey data.
* **Miscellaneous**
  * When mousing over areas with Interference in the Interference heatmap, the APs causing that interference have a red highlight. Nice.
  * Previously, we gave new Hamina accounts the opportunity to view one of several example projects, which would then copy that example project to their account. Now, we copy all of the example projects to the new user's account, so they can explore all of them.

#### APs and Antennas

* Added the Calix GigaPro p6dx

#### Bugs

* We fixed an issue where a measured AP could appear on two maps. This was mostly true before (but is extra-true now): if you have a project with multiple maps/floors, a surveyed AP will only appear on one at a time.
* We decided to make the "Roaming Man" in the Client View is more grounded. Seriously. At the default client height, in 3D, his feet appear to be on the ground.
* There was an issue where you couldn't place notes on survey paths. That's fixed, now you can put map notes wherever you want!
* There were some memory usage issues in Safari, which we mitigated with... uh... memory-usage-mitigating techniques.

### 2023/12/11

*   Added support for an innovative new input method for computer mice: **scroll wheels**! The camera controls toolbar on the right now has a **Switch to mouse/trackpad mode** button, which changes the behavior of the "scroll wheel". Trackpad mode optimizes for two-finger scrolling and pinch-to-zoom, and mouse mode optimizes for zooming in and out with the scroll wheel. We put the button right there in the toolbar, so if you switch back and forth instantly. 🐭\


    <div align="left">

    <figure><img src="../.gitbook/assets/mouse.png" alt="" width="191"><figcaption></figcaption></figure>

    </div>
*   While we typically don't want it to happen, clients do occasionally roam to APs on different floors! The problem is that the Client View only paid attention to the current floor, but we fixed that. Now, the client can roam to APs on the floors above and below. Enable **Full Building propagation** and the client can potentially roam to any AP on any floor! The association area turns red, too.\


    <div align="left">

    <figure><img src="../.gitbook/assets/wrong_floor (1).png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
*   Speaking of the Client View, it's all-new to make room for **Client capacity**! Now, when a Capacity zone is drawn, and clients are associated to the current associated AP, the Client view will now show the capacity of the current radio from a client association perspective.\


    <div align="left">

    <figure><img src="../.gitbook/assets/client_capacity.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
* With Hamina Network Planner Plus, the Client View can now show **Downlink**, **Uplink**, and... you're gunna love this one, we made it all up on our own: **Worstlink**®! It shows you, uh... the worst of the two.
* In the Client View, enabling **Show association area** now automagically disables the current heatmap.
* Cisco Catalyst (DNA) Center Export now includes the building, floor, and radio details! The **Building** is populated from the **Hamina project name**, and the **Floor** is derived from the multi-floor feature. The radios now include azimuth, elevation (from the AP height), and radio type. It's all still in beta though, so be careful!
*   The **x** button in the Share menu is now a trash can. Am I getting paid per bullet point? No...? Why do you ask?

    <div align="left">

    <figure><img src="../.gitbook/assets/Screenshot 2023-12-11 at 7.17.58 PM.png" alt="" width="374"><figcaption></figcaption></figure>

    </div>
* Previously, entering 3D mode would cause the map to slowly rotate, which looked pretty cool. Unfortunately, changing the zoom or rotation would stop it. Now, you can right-click the Switch to 2D button in the camera controls toolbar to restart rotation. Ok, this is mostly for us to demo things and sell more Hamina subscriptions, but maybe you'll find some use for it too.

#### Bugs

* The Channel Width column in the AP Radio Details table had a decimal place for no reason. It will now, for example, say "20 MHz" instead of "20.0 MHz".
* In PDF reports, the Legend in the lower left was all red, but only in Preview on macOS. In other PDF viewers, it was fine, but we changed how we draw the legend in the PDF so it would look right in Preview.
* The title for the "table mount" was wrong in the BOM, so we fixed it.

### 2023/11/23

* Behind-the-scenes work for Hamina Onsite. 😮

#### Bugs

* In some cases, the tops of overlapping walls might flicker, so we applied a temporary fix. We'll do a permanent fix soon, along with some big 3D improvements that are on the horizon. 🤩

### 2023/11/21

* Added the MikroTik cAP ax
* Added the MikroTik hAP-ac3 and hAP-ax3 that uses an HGO-52 antenna.
* Added the Huawei 8760-X1E.
* Added the Juniper Mist AP41E.
* Added the Alcatel Lucent AP1301 and AP1311.
* Added the an AirSpeed 1900/2900 external antenna variant. You're all variants!
* Behind-the-scenes work for Hamina Onsite. 🤫

#### Bugs

* There was an issue where users without a subscription (the "free tier" users) couldn't create reports. That wasn't intentional, and it's fixed now!
* PDF report generation was sometimes failing. We figured it why, and fixed. it.
* We accidentally added the Extreme AP3000 as a tri-radio AP. In reality, it is a dual-band AP with a band-selectable radio, so we fixed it. There is now a 2.4/5 GHz version, and a 5/6 GHz version.
* The EnGenius ECW215 and ECW230 had the wrong Wi-Fi generation assigned. Now, they're Wi-Fi 6, as they should be.

### 2023/11/01

* We added multi-radio support for cellular APs (or "eNodeBs" as the cool kids say), which means support for different antennas per radio and selecting radios individually (both for heatmaps and azimuth controls).
* We added an Upcoming AP models flag to the APs/antennas database, and a **Preview upcoming AP models** checkbox, so vendors can see their APs and antennas in Hamina ahead of their official release.
* Added the Zyxel WBE660S.
* You guessed it, more behind-the-scenes work for Hamina Onsite! 🤫

#### Bugs

* Just one bugfix this time: switching between cellular and Wi-Fi APs could have broken the external antenna switcher. It doesn't break anymore!

### 2023/10/25

* Implemented the new Planner layout to prepare for Hamina Onsite.
* We added the resolved AP number to the Copy function, which some of our users needed for doing automation and stuff.
* Added channel width indicators to the Access point pane, so you could quickly see what channel width the Automatic channel width feature is using.
* Added the Ruckus R770.
* Behind-the-scenes work for Hamina Onsite. 🤫

#### Bugs

* Fixed a bug where the channel settings wouldn't save if you opened them through the access point pane. 🐛
* Fixed a bug where a project wouldn't save to the folder you specified, if you assigned it to  a folder during creation. 🪲
* Here's a weird one: if you uploaded some maps, and quickly switched to a different project, you'd get map upload notifications for the previous project.
* Fixed an issue where the Extreme AP3000 didn't default to a ceiling mount. Whoops. 🤪
* Fixed an issue where the Automatic channel width would get stuck. I tell you what, we hit it with some WD-40. It doesn't get stuck no more.

### 2023/10/19

*   Added Co-channel interference tooltips! Now, with the **Interference** heatmap enabled, mousing over any interference will show which APs are causing the interference down in the Legend.\


    <div align="left">

    <figure><img src="../.gitbook/assets/interference.png" alt="" width="372"><figcaption></figcaption></figure>

    </div>
* Added **Automatic channel width**! Now, Hamina Network Planner can automagically optimize the channel width, based on how much co-channel interference you have. For now, you'll need to visit the **Channel settings** to enable it for each band, but someday, we'll probably make it on by default. Once it's enabled, as you add APs, you'll see &#x20;
* Behind-the-scenes work for Hamina Onsite. 😮

### 2023/10/13

There's so much stuff in this one that we're going to split out the release notes into **Features and Changes**, **Bugs**, and **New APs and Antennas**. Let's gooooooo!

**Features and Changes**

* Map/floor ordering in PDF reports didn't have a specific order, so we added sorting to it.
* We renamed "Cisco DNAC" to "Cisco Catalyst (DNA) Center", which we think is both correct and universally recognizable. _Note: this feature is still in a Feature Preview state, and isn't considered production-ready yet._
* In sample projects, we now automatically select a heatmap for the user when they open it for the first time.
* In the Client View, there is now an option to make the iPhone 6E capable of Wi-Fi 6E, so you can simulate the iPhone 15 Pro in 6 GHz.
* In a previous release, we introduced the new mesh feature, which automatically meshed any access points that were configured to **Not connected** via Ethernet. This broke a few corner cases (such as our current lack of connecting to a switch/IDF on another floor), so we brought back the normal "Not connected" option, and gave mesh it's own option, simply called "Mesh".

**Bugs**

* In our last production push, we accidentally introduced some slowdown in the heatmap rendering. Basically, we were constantly recalculating a bunch of stuff that we didn't need to. That's fixed now, so the heatmaps should feel smooth again.
* Note images were broken, due to some data isolation issues. The images have been... uh... un-isolated.

**New APs and Antennas**

* Renamed "Home Wi-Fi" to "Acme Technology", which fits the list better.&#x20;
* Alcatel Lucent
  * OAW-AP1411 2.4/5
  * OAW-AP1411 2.4/6
  * OAW-AP1411 5/6
  * OAW-AP1431
* Ubiquiti U6 Plus
* Arista C-330
* Huawei
  * AirEngine5760-51
  * AirEngine 5760-51 2.4/5/5
  * AirEngine 5761-11
  * AirEngine 5761-11W
  * AirEngine 5761-12W
  * AirEngine 5762-10
  * AirEngine 5762-12SW
  * AirEngine 5762-15HW
  * AirEngine 5762-17W
  * AirEngine 6760-X1
  * AirEngine 6760-X1E
  * AirEngine 6761-21 (Omni)
  * AirEngine 6761-21 (HD)
  * AirEngine 6761-21E
  * AirEngine 6761-21T
  * AirEngine 8760-x1-PRO
  * AirEngine 8760-x1-PRO 2.4/5/5
  * AirEngine 8761-X1
  * AP7060
* Celona
  * AP 20 4G
  * AP 20 5G
* Meraki
  * 9166D1-MR 2.4/5/6
  * 9166D1-MR 2.4/5/5
  * _Note: these were already available in the Cisco group, but have just been copied here for completeness._
* Alpha Wireless
  * AW3161
  * AW3711
  * AW3939
* Ventev
  * Terrawave M6060060D4D3602FP
  * Terrawave 58070MP13620P2

### 2023/10/03

* This release adds the AP Radio Details page to the PDF output. Now, the PDF report should include everything that the online report does, except for the Client View, which requires interactivity that only a browser can provide. 😉
* **Beta feature**: We've also added an option to enable Full Building Propagation. By default, Hamina shows propagation from the floor above and below the currently selected floor. This helps keep performance pretty fast without sacrificing any accuracy in most environments, as signal usually doesn't propagate through more than two floors. The[ Full Building Propagation (Beta)](https://docs.hamina.com/kb/basics/heatmaps#full-building-propagation-beta) option enables signal propagation calculations across all floors in the building for special buildings like theaters and arenas.
* **Special feature preview**: Export to Cisco DNA Center! This feature isn't done yet, but we wanted to show you our progress. It probably won't work at all, but [feel free to give it a try](https://docs.hamina.com/kb/import-export/cisco-catalyst-center).
* There was a bug that would cause the automatic channel planner to use 40, 80, and 160 MHz channels that don't exist. For example, the channel planner would create a 160 MHz channel in UNII-3, with channel 149 as the primary 20 MHz channel. Now, in addition to checking the regulatory domain and what channels the user has allowed, it now understands which 40, 80, and 160 MHz channels are valid.
* The signaling rate in the Client View was incorrectly labeled MBps (megabytes per second), instead of the correct Mbps (megabits per second). The label now correctly says Mbps. Sometimes, it's the small things. 🎸

### 2023/09/25

* We used to have an option to “Dowload” a PDF. We decided to depreciate that feature, and offer a new “Download” PDF option instead. 🤪
* There was a bug where you couldn’t add Interference thresholds after you removed them. We’ve removed the Interference removal bug, which removed the ability to safely remove Interference thresholds.
* In online reports, it wasn't possible to select a cellular client in the Client View. That's been fixed!
* We fixed a minor bug that would cause the mouseover inspector in the legendy to stop updating.
* We added some access points and antennas:
  * Fortinet 221-C
  * Cambium XV3-8
  * Airspan 1900/2900
  * Celona AP 21
  * Celona AP 22
  * Ventev M6060060MO1D3607O
  * Fortinet FANT-06ABGN-0606-O-N
* We also changed some access points and antennas:
  * The Calix u10xe now defaults to a table mount.
  * We updated the Celona external antennas to use the same part numbers that appear on the Celona data sheets.
  * Since the Meter MW05 and MW09 use external antenna connectors, we split them out into two variants: Default, which includes the stock antennas, and custom, so you can select whatever antenna you’d like to use.
  * The gain on all of the generic home Wi-Fi access points seem a bit high, so we decreased it a little bit.
  * BLE Gateways now connect back to switches by default.

### 2023/09/12

* In Safari, heatmaps weren't updating. We fixed it, and they're updating now!
* We fixed a little bug that was causing duplicate users to show up in our payment processing service.

### 2023/09/08

* Wait. _Another_ production push? There was a sneaky surprise in yesterday's push: single-hop mesh support! We did a mini-production push today to enable it. Now, **Connected via Ethernet** is set to `Not Connected (Mesh)`, mesh options appear. Check out our [Mesh Planning knowledgebase article](../design/mesh-planning.md) to learn more.
* In addition to the new mesh feature, we also added generic `Home Wi-Fi` gear. Now, new users can create an account and design their home Wi-Fi network for free. If you're a consumer router/access point/home mesh system vendor, and want us to include your gear, let us know and we can get it added for you. We'll just need your [specs and antenna patterns](requesting-aps.md#what-data-do-you-need-to-add-aps-and-antennas-to-hamina). 😃

### 2023/09/07

* If the heatmap is set to None, placing the first AP on the map automatically turns on the primary coverage heatmap for that type of AP (Wi-Fi, Private Cellular, BLE, or Zigbee)! 🔥
* Previously, the pin icon for private cellular base stations used a “5G” icon, which didn’t make sense for base stations that were 4G. We switched it to a generic  “cellular bars” icon to make it more universal. 📶
* Consumer routers and customer premises equipment is now “on the table” in Network Planner, with the all-new “Table Mount” option. 🍽️
* Fixed a bug where all APs in PDF would be blue, no matter what. Now, alternate AP colors appear in PDF reports. 🗒️
* Previously in 3D, the lines from the client view tracked back to the floor underneath the AP. Now, the lines terminate at the height of the AP, which is nice for seeing if the client has line-of-sight through sloped floors and attenuating objects.
* Added the Airspan Velocity 1901
* Added the Arista O-235E
* Added the CIG WF-660A
* Added the Meter MW05 and MW09

<figure><img src="../.gitbook/assets/Cell.png" alt=""><figcaption><p>Check out the latest amazing Hamina innovation: new cellular radio unit icons! Whoa!</p></figcaption></figure>

### 2023/09/01

* The Auto-draw walls tool has been hugely improved! It now draws less segments, and straighter walls.
* New accounts now include five sample projects, so new users can immediately see what the tool is capable of, and start moving APs around. 🎉
* In addition to the new sample accounts, there is now a 15-minute tutorial video. 📺
* In the Auto-draw walls tool, you can now click on a wall layer, and assign a material to it with a hotkey. ⌨️
* When sharing a project with another Hamina Network Planner user, you can now type in their address and hit Enter (without having to click on the Share button).
* The scale marker in the lower left wasn’t working correctly with feet, although it was fine in meters. We beat feet and got it fixed. 🏃

<figure><img src="../.gitbook/assets/Wall Drawing (1).png" alt=""><figcaption><p>Comparison of the old automatic wall drawing and the new automatic wall drawing on the same CAD-sourced PDF file.</p></figcaption></figure>
