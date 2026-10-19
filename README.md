# AnyPS5 fork sync

`main` in this repository is kept identical to [boykopovar/AnyPS5](https://github.com/boykopovar/AnyPS5) by
[sync-upstream.yml](.github/workflows/sync-upstream.yml), which runs every 6 hours and can be started by hand
from the Actions tab ("Run workflow").

This branch (`sync-bot`) is the default branch only so that the scheduled workflow runs; it holds no AnyPS5 code.

The upstream project's own workflows are disabled in this fork.

If upstream changes its workflow files, the built-in token cannot push them and a run fails. Then either press
"Sync fork" on `main`, or add a repository secret `SYNC_TOKEN` holding a personal access token with the `repo`
and `workflow` scopes, which the workflow uses instead.
