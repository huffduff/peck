# peck

A platform independent build tool with monorepo support

## The goal

To build a platform and language independent cli build tool, similar to Bazel, that leverages existing tools to do the heavy lifting.

### Docker

With quality Docker implementations available on all popular platforms, containerized builds can aleviate the platform specific issues and make for relatively simple isolation of concerns during the build and compile stages.

### Woodpecker-ci

[Woodpecker](https://github.com/woodpecker-ci/woodpecker) already provides the containerized build logic needed for almost all of these tasks. And with the easy plugin system, can adapt to fit most use cases.

By bringing up a preconfigured Woodpecker instance locally we should be able to take advantage of staged builds, including cached results, pretty easily. It also means a remote Woodpecker instance running in a cluster can offload builds for performance and scalability, similar to how Bazel does it but with a significantly easier setup.

## Initial build tools

Our priorities at the moment include:

- [ ] **Go executables:**
      Cross compiling Go executables
- [ ] **Docker images:**
      Building cluster-ready docker images for Go based services
- [ ] **npm packages:**
      Specifically vite/webpack builds
- [ ] **Android:**
      Final packages for both testing and release
- [ ] **ios/macOS:**
      This is not likely to happen, but boy wouldn't it be great?

