

## gh repo delete

```
gh repo delete [<repository>] [flags]
```

Delete a GitHub repository.

With no argument, deletes the current repository. Otherwise, deletes the specified repository.

Deletion requires authorization with the "delete_repo" scope. 
To authorize, run "gh auth refresh -s delete_repo"

### Options


<dl class="flags">
	<dt><code>--confirm</code></dt>
	<dd>直接通过提示</dd>
</dl>


### See also

* [gh repo](./gh_repo)
