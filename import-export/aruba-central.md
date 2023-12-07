---
description: Learn how to import maps and access points from Aruba Central.
---

# 🟠 Aruba Central

Hamina Network Planner includes integration with Aruba Central, which can be used to import maps and access points (including model, name, MAC, serial) into Hamina Network Planner. Then, you can add walls, attenuating objects, and scope zones to simulate the current network configuration in a predictive model.

{% hint style="info" %}
Exporting to Aruba Central is not yet supported due to limitations of Aruba Central API. You can [track the status of the issue on the Hamina feedback page](https://feedback.hamina.com/suggestions/341313/export-from-hamina-to-aruba-central-capability).
{% endhint %}

## Creating API Access Token

1. Log in into Aruba Central and select **Organization** from the side menu.

<div align="left">

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

</div>

2. Select the **Platform Integration** tab.

<div align="left">

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

</div>

3. Under the **API Gateway** section, select **Rest API.**

<div align="left">

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

</div>

4. Select the **My Apps & Tokens** tab.

<div align="left">

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

</div>

5. Select **Add Apps & Tokens**.

<div align="left">

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

</div>

6. Click the **Generate** button to confirm creating a new token.

<div align="left">

<figure><img src="../.gitbook/assets/image (26).png" alt="" width="511"><figcaption></figcaption></figure>

</div>

6. Find the token you created in the **Token List**, and click the **Download Token** link.

<div align="left">

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

</div>

7. From the window that opens, copy the value of the `access_token` field. In the example below, the access token is `1uA87rI5QgI4otIlGh9sqUt8CMACb6A4`.

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

{% hint style="warning" %}
Due to a limitation in Aruba Central, the access token is only valid for two hours. A new access token needs to be generated after the token expires.
{% endhint %}

