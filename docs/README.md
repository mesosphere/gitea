# Gitea: Docs
## D2iQ Fork

This repository is a fork hosting specific patches which for various reasons couldn't be merged with the upstream repository.

|Name|Branch/Tag|Notes|
|-|-|-|
|v1.19.2-d2iq|Tag| DKP v2.7.x release of Gitea which updates Alpine from `3.17.3` -> `3.17.6` which fixes CVEs found in the base image. This patch was not [accepted upstream](https://github.com/go-gitea/gitea/pull/28641).|

## D2iQ Releasing

We usually require Docker Images with patched versions. The process to release is as follows:
1. Checkout the specific tag that ships with a DKP Release. eg `vA.B.C`
1. Create a related release branch. eg `release/vA.B.C-d2iq`
1. Apply patches to branch `release/vA.B.C-d2iq`
1. Once statisfied, create and push the associated tag `vA.B.C-d2iq`
1. Run the [D2iQ Specific Release tooling GHA](../.github/workflows/d2iq-release-tag-version.yml). With Tag as `vA.B.C-d2iq` and Docker Image as `docker.io/mesosphere/gitea:vA.B.C-d2iq`
1. Once the image is published, push a PR to `kommander-applications` to finish using the forked image.

---

[![Join the chat at https://img.shields.io/discord/322538954119184384.svg](https://img.shields.io/discord/322538954119184384.svg)](https://discord.gg/Gitea)
[![](https://images.microbadger.com/badges/image/gitea/docs.svg)](http://microbadger.com/images/gitea/docs "Get your own image badge on microbadger.com")

These docs are ingested by our [docs repo](https://gitea.com/gitea/gitea-docusaurus).

## Authors

* [Maintainers](https://github.com/orgs/go-gitea/people)
* [Contributors](https://github.com/go-gitea/docs/graphs/contributors)

## License

This project is under the Apache-2.0 License. See the [LICENSE](LICENSE) file
for the full license text.

## Copyright

```
Copyright (c) 2016 The Gitea Authors <https://gitea.io>
```
