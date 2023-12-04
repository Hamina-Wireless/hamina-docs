---
description: Learn how to import maps and access points from Aruba Central.
---

# 🟠 Aruba Central

Hamina Network Planner includes integration with Aruba Central, which can be used to Import maps and access points from Aruba Central.

The Import function will bring the map and access points (including model, name, MAC, serial) into Hamina Network Planner. Then, you can add walls, attenuating objects, and scope zones to simulate the current network configuration in a predictive model.

{% hint style="info" %}
Exporting to Aruba Central is not yet supported due to limitations in Aruba Central API. You can follow the status of this feature here: [Export from Hamina to Aruba Central capability](https://feedback.hamina.com/suggestions/341313/export-from-hamina-to-aruba-central-capability)
{% endhint %}

## Creating API Access Token

Login into Aruba Central and select _Organization_ from the side menu:

<div align="left">

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

</div>

Select _Platform Integration_ from the top menu:

<div align="left">

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

</div>

Click _REST API_ under _API Gateway_ section:

<div align="left">

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

</div>

Select _My Apps & Tokens_ tab.

<div align="left">

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

</div>

Click _Add Apps & Tokens_.

<div align="left">

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

</div>

Click _Generate_ button to confirm creating a new token.

<div align="left">

<figure><img src="../.gitbook/assets/image (26).png" alt="" width="511"><figcaption></figcaption></figure>

</div>

Find the token you created in _Token List_ and click _Download Token._

<div align="left">

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

</div>

From the window that opens, copy the value of the "_access\_token_" field. This is the value needed in Hamina. For example, in the the access token downloaded token information below, the access token would be `1uA87rI5QgI4otIlGh9sqUt8CMACb6A4`.

```json
{
  "access_token": "1uA87rI5QgI4otIlGh9sqUt8CMACb6A4",
  "appname": "nms",
  "authenticated_userid": "user@hamina.com",
  "created_at": 1701695769497,
  "credential_id": "7d8bc788-55ca-42c5-9477-6319fa07e737",
  "expires_in": 7200,
  "id": "9b7973ae-7de8-49d8-8ca5-ba610d08d5fb",
  "refresh_token": "IaJ4iWO16SAM1Ib4CCMZUE1EdvLGlWZ1",
  "scope": "all",
  "token_type": "bearer"
}
```

{% hint style="info" %}
Due to a limitation in Aruba Central, the access token is only valid for two hours. A new access token needs to be generated after the token expires.
{% endhint %}

