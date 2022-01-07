---
layout: manual
permalink: /:path/:basename
---

## gh extension

GitHub CLI extensions are repositories that provide additional gh commands.

The name of the extension repository must start with "gh-" and it must contain an
executable of the same name. All arguments passed to the `gh <extname>` invocation
will be forwarded to the `gh-<extname>` executable of the extension.

An extension cannot override any of the core gh commands.

See the list of available extensions at <https://github.com/topics/gh-extension>


### Commands

* [gh extension create](./gh_extension_create)
* [gh extension install](./gh_extension_install)
* [gh extension list](./gh_extension_list)
* [gh extension remove](./gh_extension_remove)
* [gh extension upgrade](./gh_extension_upgrade)


### See also

* [gh](./gh)
