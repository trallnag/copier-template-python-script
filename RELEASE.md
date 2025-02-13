# Release!

This document describes the release process and is targeted at maintainers.

Check the existing tags:

```sh
git tag --list --sort=taggerdate 'v*' | tail --lines=5
```

Pick the next version:

```sh
VERSION=8
```

Create the new tag:

```sh
git tag --sign --message="" v$VERSION
```

Make sure that the tree looks good:

```sh
git log --graph --oneline --all --max-count=5
```

Push it:

```sh
git push origin master
git push origin v$VERSION
```

Done. In repositories that use this template, update to the new version using
for example the following command:

```sh
rm -rf .git/hooks
copier update --defaults
just init
```

For more information, check the
[Copier documentation](https://copier.readthedocs.io/en/stable/updating/).
