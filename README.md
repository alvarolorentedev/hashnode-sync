# hashnode-sync

This repo is configured to publish root-level markdown posts to Hashnode using the GitHub Action [`iammarmirza/hashnode-github-sync@v1.6`](https://github.com/marketplace/actions/hashnode-github-sync).

## Required GitHub configuration

Set these in the repository before enabling the workflow:

- `HASHNODE_TOKEN` as a repository secret. This is the Hashnode API token used by the action.
- `HASHNODE_HOST` as a repository variable. Example: `your-publication.hashnode.dev`.

## Workflow

The workflow lives at `.github/workflows/publish.yml` and runs on:

- pushes that change root-level `*.md` files, excluding `README.md`
- manual runs through `workflow_dispatch`
- `repository_dispatch` with type `trigger` for optional two-way sync from Hashnode

## Notes

- Posts must stay in the repository root. The action expects root-level markdown files.
- Filenames are treated as the post slug by the action, so renaming a file changes the effective slug.
- The `repository_dispatch` trigger is only useful if you also wire Hashnode webhooks through a middleware as described by the action author.

