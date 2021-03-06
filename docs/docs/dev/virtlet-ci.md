# Virtlet CI

Virtlet uses [CircleCI](https://circleci.com/) for building binaries,
docker images and running the tests. The CI configuration resides in
[.circleci/config.yml](https://github.com/Mirantis/virtlet/blob/master/.circleci/config.yml)
file. You can sign into CircleCI, and make it run tests for your own
fork of Virtlet by connecting it to your [GitHub](https://github.com/)
account.

There are some conventions about branch naming that are respected by
CircleCI. Namely, branches with names ending with `-net` will be
checked with extra e2e jobs that examine Weave, Flannel and multi-CNI
based network setups. For branches with names ending with `-docs` only
documentation will be built.

Also, you can append `[ci skip]` to your commit message to have CI
skip the particular commit/PR altogether.
