# Android TV API

{% columns %}
{% column %}

<figure><img src="https://982415813-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FWmh3vwnaQq8nqAu5YVYE%2Fuploads%2Fgit-blob-998b016bdb8001f086601bb1fc02435863668340%2F3242.png?alt=media" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column %}

<figure><img src="https://982415813-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FWmh3vwnaQq8nqAu5YVYE%2Fuploads%2Fgit-blob-8c883a70cfbf270139b884dbc4c086094d01c866%2F3425.png?alt=media" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

To transfer a subscription to a userвЂ™s TV, you need to know the 5-digit code generated when the app is first launched on the Android TV. The user can get this code by selecting the **Web Import** option in the app interface.

After that, you must send a **POST** request to:\
`https://check.xpert-lab.site/sendtv/[uid]`\
where **\[uid]** is the 5-digit code displayed on the TV.

The request body should be in JSON format:

```json
{ "data": "base64" }
```

The `data` field contains the server or subscription configuration encoded in **Base64**.

#### Example `curl` request:

```bash
curl -X POST https://check.xpert-lab.site/sendtv/12345 \
  -H "Content-Type: application/json" \
  -d '{"data":"aHR0cHM6Ly90ZXN0LXN1YnMuaGFwcC5zdS9wYWdlLnBocD9pZD14Y3huV254Uw=="}'
```

In this example, `12345` is the TVвЂ™s UID, and `data` holds the Base64-encoded configuration string.

