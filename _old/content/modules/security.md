---
title: "Security"
date: 2018-05-08T20:33:28-07:00
draft: false
weight: 203
---

Displays some general information about the state of the machine's wifi
connection, firewall, DNS settings, and logged-in users.

#### Wifi Network

<ul class="list-ornate">
  <li>The name of the current network</li>
  <li>Whether or not the network uses <a href="https://www.howtogeek.com/167783/htg-explains-the-difference-between-wep-wpa-and-wpa2-wireless-encryption-and-why-it-matters/">encryption</a> and if so, what flavour</li>
</ul>

#### Firewall

<ul class="list-ornate">
<li>Whether or not the <a href="https://support.apple.com/en-ca/HT201642">firewall</a> is enabled</li>
<li>Whether or not <a href="https://support.apple.com/en-ca/HT201642">Stealth Mode</a> is enabled</li>
</ul>

#### DNS

<ul class="list-ornate">
<li>Which <a href="https://developers.cloudflare.com/1.1.1.1/what-is-1.1.1.1/">DNS resolvers</a> (servers) the machine is configured to use</li>
</ul>

#### Users

<ul class="list-ornate">
<li> Which users are logged into the machine. Note: Does not yet
show hidden users.</li>
</ul>

## Configuration

{{< code lang="yaml" >}}
security:
  enabled: true
  position:
    top: 1
    left: 2
    height: 1
    width: 1
  refreshInterval: 3600
{{< /code >}}

## Screenshots

<img class="screenshot" src="/imgs/modules/security.png" width="320" height="192" alt="security screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/enabled >}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}
{{% /attributes %}}

## For Linux Firewall Users

For most Linux distributions, to get the correct firewall settings by default, the program needs to be run as root. 
This is obviously a bad idea. Here's is one potetial solution:

{{< code lang="bash" >}}
sudo visudo -f /etc/sudoers.d/ufwstatus

# Then add the following to that file:

# We need to add the "full" command as alias:
Cmnd_Alias      UFWSTATUS = /usr/sbin/ufw status

# Group privilege specification
%ufwstatus      ALL=NOPASSWD: UFWSTATUS
{{< /code >}}

Now run:

{{< code lang="bash" >}}
# Add new group: "ufwstatus"
sudo groupadd -r ufwstatus

# Add the username (here "xxxx") to the "ufwstatus" group
sudo gpasswd --add xxxx ufwstatus

# We add all "root" user sbin paths for convenience
export PATH=${PATH}:/usr/local/sbin:/usr/sbin:/sbin
{{< /code >}}

Thanks to [@E3V3A](https://github.com/E3V3A) for <a href="">Security Widget gives wrong firewall info for non-root linux users</a> which described the original issue and solution.

{{% sourcePath module="security" %}}