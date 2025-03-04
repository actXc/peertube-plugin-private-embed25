# PeerTube plugin private embedding

This plugin restricts the visibility of a not listed video to be embedded on a certain domain.

When selecting "Not listed" from the privacy options, the user can check a box to activate the private embedding:

![Screenshot](docs/screenshot.png)

Ensure that the domain contains the protocol and a trailing slash like shown in the screenshot!

If checked, the video can no longer be viewed without being embedded on the domain entered in the respective input field.

Multiple domains can be added separated by comma.

## Remove restriction

If you want to remove the restriction ensure to remove the domains from the domain field, then uncheck the box and save the changes.

## Update from previous version

If you update from version 0.0.1 you need to rewrite the storage column "storage" in the "plugin" table.

You will find something like in the json:

```
"restrict-embedding-domain-42": "https://example.com/",
```

and need to convert it to:

```
"restrict-embedding-domain-42": ["https://example.com/"],
```

## Author and contributors

* The plugin was created by [osiris86](https://github.com/osiris86/peertube-plugin-private-embed).
* Code for options to use multiple domains was added by [rdroro](https://gitlab.com/rdroro/peertube-plugin-private-embed-multiple-domain/).
* jfqd upgraded to use it with peertube > v.5,
* I try to publish jfqd to the plugins in Peertube, but its my first attemt to do so.
