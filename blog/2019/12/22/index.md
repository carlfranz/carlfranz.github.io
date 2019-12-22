---
title: Useful daily git command: remove useless remotes
---
# Useful daily git command: remove useless remotes
Working with feature branches is pretty handy. Everything starts with a branch from `develop` named `feature/<something>`. When you start committing, changes does not affect the `develop` branch. 
If your repository manager handles merge requests, once the branch is created, you open a merge request. When the feature job is done you close the request and through web, merge changes into `develop` branch. 
As a side effect the repository manager removes the branch. Not bad, the job is done and the edits are tracked with a "merge commit".

By client side, those branches are never removed. This could lead to a messy repository and wrong checkouts, better keep the stuff nice, to avoid useless problems. Here this command come in help.

```bash
git fetch origin --prune
```

What `fetch` do is to get "news" about remote branches. What the flag `--prune` do is explained by the git documentation:

> Before fetching, remove any remote-tracking references that no longer exist on the remote. 

Doing that on one of my repositories lead to this output:
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
