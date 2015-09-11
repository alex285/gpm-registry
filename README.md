## GPM Registry
Packages definitions for GPM. Minimum GNOME version support is 3.18.

### Requirements
The source of the package should be hosted on [Github!](http://github.com/)

**Name:** The name is what your thing is called. Folder name should be the same as the package name, and it should be unique. Use dashes to separate the words.
- Can't start with a dot or an underscore.
- Must not have uppercase letters.
- Can't contain any non-URL-safe characters.

**Version:**
Packages follow [semver](http://semver.org/) schema. Since authors so far don't follow semver, add a `0.1.0` default.  

**Type:**
- `extension` for Gnome Shell extensions.
- `shell` for Gnome Shell themes.
- `gtk` for Gtk+ themes.
- `icons` for icon themes.


### Samples
This is a minimum required `gpm.json`

```
{
  "name": "foo-me",
  "version": "0.1.0",
  "gnome": {
    "type": "extension",
    "version": [
      "3.16",
      "3.18"
    ],
  },  
  "repository": {
    "type": "git",
    "url": "https://github.com/foo/foo.git"
  }
}
```


#### A more complete sample
Some extensions might have package requirements. We'll deal with those later. Prolly add those on web service directly.
```
{
  "name": "foo-me",
  "pretty-name:" "Foo Me!"
  "version": "0.1.0",
  "description": "An extension that fooing Gnome Shell activities",
  "gnome": {
    "type": "extension",
    "version": [
      "3.16",
      "3.18"
    ],
  },
  "keywords": [
    "activities",
    "foo"  
  ],
  "repository": {
    "type": "git",
    "url": "https://github.com/foo/foo.git"
  },
  "homepage": "http://foo.com",
  "author": "Foobar",
  "bugs": {
    "url": "https://github.com/foo/foo/issues"
  },
  "license" : "MIT",
}
```

## Pull Requests

Please make requests **only** for Gnome Shell extensions (not themes now) and that **only** work on GNOME 3.18. `gpm.json` files might change. Hopefully not!

## GPM Dist
For packaging auto deployment there should be a standard format. Since it is not possible for everyone to modify their repos, may authors can provide a `gpm-dist` directory on their repos? Ideas? 
