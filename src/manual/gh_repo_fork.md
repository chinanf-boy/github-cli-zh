---
layout: manual
permalink: /:path/:basename
---

## gh repo fork

```
gh repo fork [<repository>] [-- <gitflags>...] [flags]
```

Create a fork of a repository.

With no argument, creates a fork of the current repository. Otherwise, forks
the specified repository.

By default, the new fork is set to be your 'origin' remote and any existing
origin remote is renamed to 'upstream'. To alter this behavior, you can set
a name for the new fork's remote with --remote-name.

Additional 'git clone' flags can be passed in by listing them after '--'.

### Options


<dl class="flags">
	<dt><code>--clone</code></dt>
	<dd>Clone the fork {true|false}</dd>

	<dt><code>--org &lt;string&gt;</code></dt>
	<dd>Create the fork in an organization</dd>

	<dt><code>--remote</code></dt>
	<dd>Add remote for fork {true|false}</dd>

	<dt><code>--remote-name &lt;string&gt;</code></dt>
	<dd>Specify a name for a fork&#39;s new remote.</dd>
</dl>


### See also

* [gh repo](./gh_repo)
