---
title: "Google Analytics"
date: 2019-08-31T01:46:10.010Z
draft: false
weight: 50
---

<img src="/imgs/modules/google_analytics.png" class="screenshot" width="600" height="150" alt="google analytics screenshot"/>

Display website visitors information from Google Analytics API

To make this work, you'll need a google API credential, link it to google analytics and find your website viewID.

1. Open the [Service accounts page](https://console.developers.google.com/iam-admin/serviceaccounts) and create a project named wtfutil.
1. Navigation menu > IAM & admin > Service accounts
1. Click add Create Service Account, enter a name (wtfutil) for the service account.
1. The Service account permissions (optional) section that follows is not required. Click Continue.
1. On the Grant users access to this service account screen, scroll down to the Create key section. Click add Create key.
1. In the side panel that appears, select the format for your key: JSON.
1. Click Create. Your new public/private key pair is generated and downloaded to your machine; it serves as the only copy of this key.
1. Copy this json to indicated filepath in wtfutil googleanalytics module Configuration.
1. Enable the Google Analytics APIS and Services (Navigation menu > APIS and Services > +Enable APIS and Services > Google Analytics Reporting API > Enable)

The newly created service account will have an email address that looks similar to:

```console
something@PROJECT-ID.iam.gserviceaccount.com
```

Use this email address to add a user to the [Google analytics view](https://analytics.google.com/analytics/web/) you want to access via the API (admin > user management > add users). Only Read & Analyze permissions are needed. Get the website viewID and put it in the config file.

## Real Time Data

This module also supports displaying the number of visitors on each view live via the Google Analytics Real Time Reporting API Beta. In order to use this feature, you must [sign up](https://docs.google.com/forms/d/1qfRFysCikpgCMGqgF3yXdUyQW4xAlLyjKuOoOEFN2Uw/viewform) for the beta and wait for your whitelist application to be approved (which takes less than 24 hours). Once you're approved, all you need to do is set `enableRealtime: true` in the module settings.

## Configuration

```yaml
googleanalytics:
  enabled: true
  enableRealtime: true
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
  {{< attributes/custom name="enableRealtime" desc="When set to `true`, the live count of users on each listed view will be displayed in addition to historical visitor counts.  This requires you to [sign up](https://docs.google.com/forms/d/1qfRFysCikpgCMGqgF3yXdUyQW4xAlLyjKuOoOEFN2Uw/viewform) for the Real Time Reporting API Beta. Default: false." value="true, false" >}}
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
