# protocol-releaser
A GitHub action to prepare and release a protocol for Digital Trails.

## Branches and releasing

Protocols run this action from `main`: every protocol's `publish_on_release.yml` says
`uses: uvamaplab/protocol-releaser@main`. So `main` is the release. Work happens on `develop`, the
default branch; merging `develop` into `main` is what ships, and every protocol's next release uses
it. Nothing goes out until that merge. To roll back, revert on `main`.

Tag the merge (`v1.9.0` and so on) and publish a GitHub release for the record. The tag changes
nothing by itself; `main` is what runs.
