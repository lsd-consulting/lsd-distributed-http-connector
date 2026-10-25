[![semantic-release](https://img.shields.io/badge/semantic-release-e10079.svg?logo=semantic-release)](https://github.com/semantic-release/semantic-release)

# lsd-distributed-http-connector
![GitHub](https://img.shields.io/github/license/lsd-consulting/lsd-distributed-http-connector)
![Codecov](https://img.shields.io/codecov/c/github/lsd-consulting/lsd-distributed-http-connector)

[![CI](https://github.com/lsd-consulting/lsd-distributed-http-connector/actions/workflows/ci.yml/badge.svg)](https://github.com/lsd-consulting/lsd-distributed-http-connector/actions/workflows/ci.yml)
[![Nightly Build](https://github.com/lsd-consulting/lsd-distributed-http-connector/actions/workflows/nightly.yml/badge.svg)](https://github.com/lsd-consulting/lsd-distributed-http-connector/actions/workflows/nightly.yml)
[![GitHub release](https://img.shields.io/github/release/lsd-consulting/lsd-distributed-http-connector)](https://github.com/lsd-consulting/lsd-distributed-http-connector/releases)
![Maven Central](https://img.shields.io/maven-central/v/io.github.lsd-consulting/lsd-distributed-http-connector)

## About
This is a HTTP implementation of the data access connector for the distributed data storage.

## Releasing

Pushing to main builds but does not release. Maven Central limits the
io.github.lsd-consulting namespace to 7 releases a month, so each release is
started on purpose. semantic-release still picks the version from the feat/fix
commits since the last release, and does nothing if there are none.

Release by hand:

```
gh workflow run release.yml -R lsd-consulting/lsd-distributed-http-connector -f reason="why this release is needed"
```

To release weekly instead (Tuesday 07:00 UTC), set the repository variable
`WEEKLY_RELEASE` to `true`. It is off by default.
