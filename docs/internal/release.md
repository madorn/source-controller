# Release

To release a new version the following steps should be followed:

1. Create a `api/<next semver>` tag and push it to remote.
1. Create a new branch from `main` i.e. `release-<next semver>`. This
   will function as your release preparation branch.
1. Add an entry to the `CHANGELOG.md` for the new release and change the
   `newTag` value in ` config/manager/kustomization.yaml` to that of the
   semver release you are going to make. Commit and push your changes.
1. Create a PR for your release branch and get it merged into `main`.
1. Create a `<next semver>` tag for the merge commit in `main` and
   push it to remote.
1. Confirm CI builds and releases the newly tagged version.
