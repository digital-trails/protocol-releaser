# protocol-releaser
A GitHub action to prepare and release a protocol for Digital Trails.

## Releasing

Protocols run this action as `uses: uvamaplab/protocol-releaser@latest`. The `latest` tag follows
the release that the Releases page marks as latest: publishing a release moves it forward, and
marking an older release as latest moves it back, both by the "Point latest at the latest release"
workflow. Commits to `main` move nothing until a release is published from them: tag the commit
(`v1.9.1` and so on) and publish a GitHub release for the tag.

GitHub runs a release event's workflow as of that release's commit, so the tag follows releases
from the first one that carries the workflow; to point `latest` at an older release, run the
workflow from the Actions tab.
