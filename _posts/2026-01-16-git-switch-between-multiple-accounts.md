---
layout: post
title: "Git author based on directory"
date: 2026-01-16
---

Recently I was writing a small comment-delete PR to [omnicron](https://github.com/oxidecomputer/omicron/pull/9661) and was surprised when I saw the commits were unverified with a generated profile picture.

Turns out I was commenting on the PR using my personal account but writing the commits with my work account.

# Per Domain

```ini
[user]
    name = Gregory Ganley
    email = greg@ganley.dev
    signingkey = PERSONAL_KEY_ID

[commit]
    gpgsign = true

[includeIf "hasconfig:remote.*.url:*gitlab.com*"]
    path = ~/.config/git/config-gitlab-work
```

```ini
[user]
    name = Gregory Ganley
    email = gregory.ganley@company.com
    signingkey = WORK_KEY_ID
```

# Per Repo

```ini
[user]
    name = Gregory Ganley
    email = greg@ganley.dev
    signingkey = PERSONAL_KEY_ID
[includeIf "gitdir:~/Developer/work"]
    path = ~/.config/git/config-work
```

```ini
[user]
    name = Gregory Ganley
    email = gregory.ganley@company.com
    signingkey = WORK_KEY_ID
```
