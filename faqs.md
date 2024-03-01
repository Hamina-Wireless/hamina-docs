---
description: Frequently asked questions about Hamina Network Planner.
---

# ❓ FAQs

### My organization manually allowlists URLs. Which ones do we need to unblock for Hamina to work properly?

To ensure Hamina functions correctly within your organization, certain URLs will need to be unblocked. The list of these URLs is provided below. If you still have trouble accessing Hamina after unblocking these URLs, please contact us at [support@hamina.com](mailto:support@hamina.com).

#### **US Instance**

* `https://us.hamina.com`
* `https://login.us.hamina.com`
* `https://sthaminasigninprodus1.blob.core.windows.net`
* `https://sthaminapubassetsprodus1.blob.core.windows.net`

#### **EU Instance**

* `https://eu.hamina.com`
* `https://login.eu.hamina.com`
* `https://sthaminasigninprodeu1.blob.core.windows.net`
* `https://sthaminapubassetsprodeu1.blob.core.windows.net`

#### **Global**

Video and image resources:

* `https://sthaminaglobalassets.blob.core.windows.net`

Application health and analytics:

* `https://o1234513.ingest.sentry.io`
* `https://www.googletagmanager.com`
* `https://*.google-analytics.com`

Fonts:

* `https://fonts.googleapis.com`
* `https://fonts.gstatic.com`

### My organization allowlists IP-addresses in vendor APIs. Which IP-addresses do I need to allow in order to get Hamina vendor integrations to work?

To ensure that Hamina can connect to vendor APIs, the IP addresses listed below need to be allowlisted. If you still have trouble using Hamina vendor integrations after allowing these IP addresses, please contact us at [support@hamina.com](mailto:support@hamina.com).

#### US instance

* `4.249.203.234`
* `20.84.195.194`
* `20.221.120.99`

#### EU instance

* `20.79.87.213`
* `20.79.85.126`
* `20.113.5.11`
* `20.113.5.58`
* `20.113.43.45`

### There's black artifacts all over my heatmaps. What's going on?

Hamina Network Planner takes full advantage of your 3D graphics accelerator to draw heatmaps. As a result, support for hardware acceleration must be enabled in your browser.

{% hint style="success" %}
These instructions are for Google Chrome, but the process of enabling hardware acceleration is very similar in most browsers.
{% endhint %}

1. In the upper right corner of your browser, click on the **hamburge**r (three dot) menu.
2. Select **Settings**.
3. The **Settings tab** will appear. Towards the bottom of the Settings menu on the left, select **System**.
4. Enable **Use graphics acceleration when available**.
