# Maintain!

This document is targeted at project maintainers. It describes various
maintenance tasks and processes.

## Bump Debian release of dev container

While Renovate takes care of updates within a release, it overall stays stuck at
the defined release, for example Bookworm or Trixie. To update, remove the
checksum and adjust the release name.
