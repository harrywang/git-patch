# git-patch

Check commits:

```
git log
commit d1a15a652860c4e0fbaa24afa9a8338acbf0e981 (HEAD -> main, origin/main, origin/HEAD)
Author: Harry Wang <harryjwang@gmail.com>
Date:   Tue Aug 20 10:41:56 2024 -0400

    fix bug

commit d7b2378faa43afd85000f794acf6a9384cb4880c
Author: Harry Wang <harryjwang@gmail.com>
Date:   Tue Aug 20 10:33:36 2024 -0400

    initial not working version

commit b7e0db2ed202f45fe7bd05ef676762e264c15323
Author: Harry Wang <harryjwang@gmail.com>
Date:   Tue Aug 20 09:27:35 2024 -0400

    Initial commit
```

create a patch from a commit:

```
git format-patch -1 d1a15a652860c4e0fbaa24afa9a8338acbf0e981
0001-fix-bug.patch
```

revert to a previous commit and apply the patch to see changes:

```
git checkout d7b2378faa43afd8
git apply 0001-fix-bug.patch
```


References:

- https://github.com/harrywang/git-patch.git
- https://graphite.dev/guides/git-apply-patch