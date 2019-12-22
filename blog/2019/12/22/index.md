---
title: Useful daily git command: remove useless remotes
---
# Useful daily git command: remove useless remotes
Working with feature branches is pretty handy. You branch from the `develop` into a `feature/<something>` branch then start committing and create a merge request. Your repository manager should handle merge requests. Once the job is done and you need to merge into `develop` the repository manager allow you to do it from web, and as a side effect it can remove the branch. Not bad, the job is done and we have tracked the edits with a "merge commit". 

By client side, those branches are never removed. This could lead to a messy repository and wrong checkouts, better keep the stuff nice, to avoid useless problems. Here this command come handy.

```bash
git fetch origin --prune
```

What `fetch` do is to get "news" about remote branch. What the flag `--prune` do is explained by the git documentation:

> Before fetching, remove any remote-tracking references that no longer exist on the remote. 

Doing that to my repository lead to this output:
```
From gitlab.mgmt.somewhere.it:lceyt/nova
 - [deleted]           (none)     -> origin/feature/closed-domain-queries
 - [deleted]           (none)     -> origin/feature/error-mapping
 - [deleted]           (none)     -> origin/feature/healthcheck-2
 - [deleted]           (none)     -> origin/feature/renaming
 - [deleted]           (none)     -> origin/feature/requests-queries
 - [deleted]           (none)     -> origin/feature/security-layer
 - [deleted]           (none)     -> origin/feature/security-layer-fe
 - [deleted]           (none)     -> origin/feature/template-schema
 - [deleted]           (none)     -> origin/feature/thorntail
 - [deleted]           (none)     -> origin/feature/wildfly
 - [deleted]           (none)     -> origin/feature/wildfly-migration
 - [deleted]           (none)     -> origin/feature/writeconcern
 - [deleted]           (none)     -> origin/feature/yaml-config
 - [deleted]           (none)     -> origin/first_impl
```

What about yours?
