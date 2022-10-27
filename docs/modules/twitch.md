# Twitch

Displays twitch streams that are currently live on [Twitch.tv](https://www.twitch.tv/).

If you wish to see **top** live streams:

1. Follow the steps [here](https://dev.twitch.tv/docs/authentication/register-app) to create a twitch app.
2. Save your <code>clientId</code> and <code>clientSecret</code> in your configuration file.

If you wish to see your **followed** live streams:

1. Perform the previous steps and continue from [here](https://dev.twitch.tv/docs/authentication/getting-tokens-oauth/#authorization-code-grant-flow) until you receive a <code>userAccessToken</code> and <code>userRefreshToken</code>.
2. Get your twitch <code>userId</code> from [this site](https://www.streamweasels.com/tools/convert-twitch-username-to-user-id/).
3. Check which <code>redirectURI</code> you have for your app at [twitch developer console](https://dev.twitch.tv/console).
4. Save your <code>userAccessToken</code>, <code>userRefreshToken</code>, <code>userId</code> and <code>redirectURI</code> in your configuration file.

## Configuration

```yaml
twitch:
  enabled: true
  position:
    top: 1
    left: 1
    height: 1
    width: 2
  streams: "top"
  clientId: "client id" 
  clientSecret: "client secret"
  userAccessToken: "user access token"
  userRefreshToken: "user refresh token"
  redirectURI: "http://localhost:3000"
  userId: 123456789
```

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
<tr>
    <td>
        <code>streams</code>
        <br />
        Which streams to display, <code>top</code> or <code>followed</code>. Default: <code>top</code>
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>clientId</code>
        <br />
        Client ID of your twitch app.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>clientSecret</code>
        <br />
        Client secret of your twitch app.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>userAccessToken</code>
        <br />
        User access token gotten from accepting your twitch app. Required to fetch followed streams.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>userRefreshToken</code>
        <br />
        User refresh token gotten from accepting your twitch app. Required to fetch followed streams.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>redirectURI</code>
        <br />
        The redirect URI set for your twitch app. Required to fetch followed streams.
    </td>
    <td></td>
</tr>
<tr>
    <td>
        <code>userId</code>
        <br />
        Your twitch user ID. Required to fetch followed streams.
    </td>
    <td></td>
</tr>
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% set esc="Cancel the selection" %}
    {% include "keyboard/esc.md" %}

    {% set return="Open the selected stream in the browser" %}
    {% include "keyboard/return.md" %}

    {% set s="Open the selected stream via streamlink (https://github.com/streamlink/streamlink)" %}
    {% include "keyboard/s.md" %}
   
    {% include "keyboard/spacer.md" %}
    
    {% include "keyboard/arrowDown.md" %}
    {% include "keyboard/arrowUp.md" %}
  </tbody>
</table>

{% set src="twitch" %}
{% include "src_path.md" %}