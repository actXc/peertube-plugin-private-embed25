# PeerTube plugin private embedding

This plugin restricts the visibility of a not listed video to be embedded on a certain domain.

When selecting "Not listed" from the privacy options, the user can check a box to activate the private embedding:

![Screenshot](docs/screenshot.png)

If checked, the video can no longer be viewed without being embedded on the domain entered in the respective input field.

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