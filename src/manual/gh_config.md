---
layout: manual
permalink: /:path/:basename
---

## gh config

Display or change configuration settings for gh.

Current respected settings:
- git_protocol: the protocol to use for git clone and push operations (default: "https")
- editor: the text editor program to use for authoring text
- prompt: toggle interactive prompting in the terminal (default: "enabled")
- pager: the terminal pager program to send standard output to
- http_unix_socket: the path to a unix socket through which to make HTTP connection
- browser: the web browser to use for opening URLs


### Commands

* [gh config get](./gh_config_get)
* [gh config list](./gh_config_list)
* [gh config set](./gh_config_set)


### See also

* [gh](./gh)
