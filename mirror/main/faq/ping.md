# Ping

### Ping (Connection Latency)

**Ping** shows how many milliseconds it takes for a server to respond to a request. Lower value = faster and more stable connection. Remember: Ping reflects latency, not bandwidth.

***

#### How to Check Ping

**1) For an entire subscription**

<figure><img src="https://982415813-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FWmh3vwnaQq8nqAu5YVYE%2Fuploads%2FdamMciLlzk3dHiiU4fGr%2F0001-min.png?alt=media&#x26;token=11e6fb65-9e08-4eca-a170-490f675684d9" alt="" width="188"><figcaption></figcaption></figure>

1. Open the main screen.
2. Tap the speedometer icon in the header of the desired subscription.
3. The Ping for each server in that subscription will appear next to it.

<figure><img src="https://982415813-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FWmh3vwnaQq8nqAu5YVYE%2Fuploads%2FzJUhLJkgplMNLQn0h0u2%2F0002-min.png?alt=media&#x26;token=5d9787f0-83b4-4f80-80ef-9c896cf32ab5" alt="" width="188"><figcaption></figcaption></figure>

**2) For an individual configuration**

<figure><img src="https://982415813-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FWmh3vwnaQq8nqAu5YVYE%2Fuploads%2FTqEmftiJyJ2BZ2HMPShU%2F0003-min.png?alt=media&#x26;token=54aac9b1-7687-4435-827b-9bd673b4d33d" alt="" width="188"><figcaption></figcaption></figure>

1. On the main screen, swipe the configuration element to the right вЂ” an actions panel will appear.
2. Tap the speedometer icon вЂ” the Ping for this specific configuration will be displayed.

**3) For the current connection**

1. Tap **"Check Current Connection"**.
2. It will display:
   * Ping value in milliseconds (always **ms**);
   * **"Timeout"** error if unavailable.

***

#### What Affects Ping

* Server distance (closer = lower latency);
* Quality and load of your internet channel;
* Network and device load;
* Background processes (downloads, updates, etc.).

***

#### Ping Types in Xpert Lab

The app supports three measurement methods. They solve different tasks and may show slightly different results.

**ICMP Ping**

Checks basic network availability with ICMP packets (similar to the `ping` command).

* Requires **temporarily disconnecting the VPN tunnel**.
* Used less frequently due to inconvenience in daily use.

**TCP Ping**

Measures the time to establish a TCP connection to the server.

* **Does not require** disconnecting the VPN tunnel.
* May reflect latency to the **nearest CDN point** if the server uses a content network вЂ” so actual latency to the final node may differ.

**Ping via Proxy**

Measures latency **through the active VPN connection**, accounting for the entire path.\
This is the most indicative method for users.

**How the check works:**

1. The app resolves the server's domain name (if a domain is specified).
2. Establishes a TCP connection; performs TLS handshake if necessary.
3. The test resource's domain is resolved on the server side.
4. The server establishes a TLS connection with the target site (if HTTPS).
5. Measures the time to receive a response from the target resource.

**Advantages:**

* Accounts for encryption and the entire data route;
* Provides the most realistic latency value when working with VPN.

**Via Proxy Modes:**

* **Via Proxy GET** вЂ” used **by default**; standard HTTP request.
* **Via Proxy HEAD** вЂ” request without body; **slightly lighter** on servers.

***

#### How to Change Ping Display Method

**Path:** Settings в†’ **Ping**

Two options are available:

* **Time (ms)** вЂ” precise latency value (e.g., *42 ms*).
* **Status Icon** вЂ” availability only:
  * green with checkmark вЂ” server is available;
  * red with exclamation mark вЂ” server is unavailable.

> The selected option is saved automatically and applies to all servers.

***

#### Automatic Check on Launch

The **"Ping on Launch"** feature checks the availability of all servers at once when opening the app вЂ” you immediately see the current status without manual testing.

**How to enable:**\
Settings в†’ **Subscriptions** в†’ enable **"Ping on Launch"**.

<figure><img src="https://982415813-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FWmh3vwnaQq8nqAu5YVYE%2Fuploads%2FhWKokMNDmn4Exzy1hXag%2F0004-min.png?alt=media&#x26;token=f69da0c2-04b6-4132-824b-9fe6b800eff1" alt="" width="188"><figcaption></figcaption></figure>

After activation, Ping is measured for all servers and their status is updated (response time or icon) every time the app launches.

***

#### Usage Tips

* Compare Ping **under identical conditions** (same network, similar device load).
* Repeat tests: one-off latency spikes are possible due to network overload.
* For assessing real user experience, focus on **Ping via Proxy**.

