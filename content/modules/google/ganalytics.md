---
title: "Google Analytics"
date: 2019-06-10T18:26:26-04:00
draft: false
weight: 50
---

<img src="/imgs/modules/google_analytics.png" class="screenshot" width="600" height="150" alt="google analytics screenshot"/>

Display website visitors information from Google Analytics API

To make this work, you'll need a google API credential, link it to google analytics and find your website viewID.

1. Open the [Service accounts page](https://console.developers.google.com/iam-admin/serviceaccounts) and create a project named wtfutil.
2. Navigation menu > IAM & admin > Service accounts
3. Click add Create Service Account, enter a name (wtfutil) for the service account.
3. The Service account permissions (optional) section that follows is not required. Click Continue.
4. On the Grant users access to this service account screen, scroll down to the Create key section. Click add Create key.
5. In the side panel that appears, select the format for your key: JSON.
6. Click Create. Your new public/private key pair is generated and downloaded to your machine; it serves as the only copy of this key.
7. Copy this json to indicated filepath in wtfutil googleanalytics module Configuration.

The newly created service account will have an email address that looks similar to:

something@PROJECT-ID.iam.gserviceaccount.com

Use this email address to add a user to the [Google analytics view](https://analytics.google.com/analytics/web/) you want to access via the API (admin > user management > add users). Only Read & Analyze permissions are needed. Get the website viewID and put it in the config file.

## Configuration

```yaml
googleanalytics:
  enabled: true
  months: 5
  position:
    top: 0
    left: 3
    width: 2
    height: 1
  refreshInterval: 400
  secretFile: "~/.config/wtf/google_analytics/client_secret.json"
  viewIds:
    tessellation: "00000000"
    dylanbartels.com: "111111111"
```

{{% attributes %}}
  {{< attributes/enabled >}}
  <tr>
    <td>`months`</td>
    <td>The amount of months being displayed with website session data.</td>
    <td>Any positive integer.</td>
  </tr>
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
  <tr>
    <td>`secretFile`</td>
    <td>Your <a href="https://developers.google.com/sheets/api/quickstart/go">Google client secret</a> JSON file.</td>
    <td>A string representing a file path to the JSON secret file.</td>
  </tr>
  <tr>
    <td>`viewIds`</td>
    <td>Website(s) who will be displayed in the module, label does not have to corresponding to the actual url. Value must be the google analytics viewID of the website.</td>
    <td>A string representing the viewID.</td>
  </tr>
{{% /attributes %}}

## Source Code

```bash
wtf/modules/googleanalytics/
```
