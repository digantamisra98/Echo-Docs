---
description: The Hitchhiker's Guide to contributing your first pull request to Echo!
---

# Contributing Guidelines

### Code Style



### Tests

Echo enforces four types of test to maintain code standards and compatibility for stable releases across platforms. These four types include:

* **Smoke Tests**
* **Break Tests**
* **Unit Tests**

### Developer Certificate of Origin \(DCO\)

Echo enforces the [Developer Certificate of Origin](https://developercertificate.org/) \(DCO\) on all pull requests. All commit messages should contain the `Signed-off-by` line with an email address. The [GitHub DCO app](https://github.com/apps/dco) is deployed on Echo. The pull request's status will be `failed` if commits do not contain a valid `Signed-off-by` line.

Git has a `-s` \(or `--signoff`\) command-line option to append this automatically to your commit message:

```bash
git commit -s -m 'a new commit'
```

The commit message will be:

```text
    a new commit

    Signed-off-by: Your Name <yourname@example.org>
```

Full text of the DCO:

```text
Developer Certificate of Origin
Version 1.1

Copyright (C) 2004, 2006 The Linux Foundation and its contributors.
1 Letterman Drive
Suite D4700
San Francisco, CA, 94129

Everyone is permitted to copy and distribute verbatim copies of this
license document, but changing it is not allowed.


Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```

