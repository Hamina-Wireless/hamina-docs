---
description: >-
  Learn how to Export maps and AP locations from Hamina Network Planner to
  ExtremeCloud IQ.
---

# 🏂 ExtremeCloud IQ

Hamina Network Planner includes integration with ExtremeCloud IQ, which can be used to export from Hamina Network Planner to ExtremeCloud IQ.

{% hint style="danger" %}
ExtremeCloud IQ Connect does not support API access. ExtremeCloud IQ Pilot is required.
{% endhint %}

The **Export** function rapidly deploys a new site, or updates an existing site directly from Hamina Network Planner. This removes the need for any repeat map-based deployment work - all of the mapping work is automatically copied directly from Hamina Network Planner.

{% hint style="info" %}
Importing from ExtremeCloud IQ to Hamina Network Planner is not currently supported by Extreme Networks.
{% endhint %}

## Generating an API Token

There are two keys that you can use to authenticate Hamina Network Planner to ExtremeCloud IQ:

* A bearer token, which will expire in 24 hours.
* A Developer API Key, which can be configured to not expire.

We recommend creating a **Developer API Key** for ExtremeCloud IQ, which can have a much longer duration.&#x20;

### Generating a Developer API Token

Creating the Developer API token requires two steps:

1. Authenticate with a username and password to generate a bearer token.
2. Perform an API call with the bearer token to generate the Developer API token.

To simplify the process, [ExtremeCloud IQ Key Retriever](https://potatofi.github.io/extreme-key/) can use your username and password to get a bearer token, and perform the API call to generate a full-access Developer API token that does not expire.

{% hint style="success" %}
The web application runs locally in your browser with JavaScript, and [the source code is available for viewing](https://github.com/PotatoFi/extreme-key).
{% endhint %}

{% hint style="warning" %}
This tool generates a full-access token. As with any API token, be sure to transport and store it safely.
{% endhint %}

### Generating a 24-hour Bearer Token

{% hint style="info" %}
Step-by-step instructions are coming soon.
{% endhint %}

