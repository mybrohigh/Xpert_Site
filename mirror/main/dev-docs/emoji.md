# Displaying flags and smileys

### Flags

If the **first emoji** in the server name is a **flag**, it will be used as the server icon.\
Any additional flags or emojis after the first one will be ignored by the icon and only shown in the server name.

You can provide a flag in two formats:

* **As an emoji symbol** (e.g. рџ‡єрџ‡ё вЂ” visual representation)
* **As a UTF-8 URL-encoded string**, for example:
  * `%F0%9F%87%AF%F0%9F%87%B5` вЂ” рџ‡Їрџ‡µ (Japan)
  * `%F0%9F%87%B7%F0%9F%87%BA` вЂ” рџ‡Ёрџ‡і (China)
  * `%F0%9F%87%BA%F0%9F%87%B8` вЂ” рџ‡єрџ‡ё (USA)

вљ пёЏ For **subscription headers**, only emoji **symbols** (e.g. рџҐ°) are supported.\
**UTF-8 encoded emojis are not supported**.

***

### Emojis

You can also use regular emojis (like smileys) in server names.\
However, if a smiley appears **before the flag**, the flag will **not be shown as the icon**.

вњ… Correct example:\
рџ‡єрџ‡ё `рџЋ USA Node` в†’ icon: рџ‡єрџ‡ё

вќЊ Incorrect example:\
`рџЋ` рџ‡єрџ‡ё `USA Node` в†’ no icon

вљ пёЏ For **subscription headers**, only emoji **symbols** (e.g. рџҐ°) are supported.\
**UTF-8 encoded emojis are not supported**.

### Example

```
vless://uuid@ip:80?flow=&type=tcp&security=none#Right1%F0%9F%87%AF%F0%9F%87%B5%F0%9F%A5%B0
vless://uuid@ip:80?flow=&type=tcp&security=none#Right2рџ‡Їрџ‡µрџҐ°
vless://uuid@ip:80?flow=&type=tcp&security=none#Wrong1%F0%9F%A5%B0%F0%9F%87%AF%F0%9F%87%B5
vless://uuid@ip:80?flow=&type=tcp&security=none#Wrong2рџҐ°рџ‡Їрџ‡µ
```

<figure><img src="https://982415813-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FWmh3vwnaQq8nqAu5YVYE%2Fuploads%2Fgit-blob-d87cf359fa71a67271accf3ba666adbb4ebfc4e2%2Fimage.png?alt=media" alt=""><figcaption></figcaption></figure>

