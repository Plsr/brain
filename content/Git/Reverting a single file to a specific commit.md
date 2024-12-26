#seed

First, we'll need to find the hash of the commit that we want to revert to. This can be done via

```bash
> git log -p filename
```

When we know the hash, we checkout the desired file to the desired hash:

```bash
git checkout [hash] -- path/to/file
```
