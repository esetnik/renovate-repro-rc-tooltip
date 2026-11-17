# renovatebot/renovate#48166

`package.json` depends on `rc-tooltip` 6.4.0, the last release under that name. Development continues as `@rc-component/tooltip` in the same repository, [`react-component/tooltip`](https://github.com/react-component/tooltip). Its 1.0.0 came out on 2025-01-10, three days after `rc-tooltip` 6.4.0.

`renovate.json` only extends `config:recommended`.

## Current behavior

Renovate proposes no update for `rc-tooltip`. 6.4.0 is its newest version, and npm has no deprecation notice pointing at the new name.

## Expected behavior

Renovate proposes a replacement from `rc-tooltip` 6.4.0 to `@rc-component/tooltip` 1.0.0 on the branch `renovate/rc-tooltip-replacement`. It does this through `replacements:rc-tooltip-to-scoped`, which `config:recommended` includes through `replacements:all`.

## How to check

From a Renovate checkout on the pull request's branch, run Renovate in this directory:

```bash
LOG_LEVEL=debug node /path/to/renovate/lib/renovate.ts --platform=local --dry-run=lookup
```

The `packageFiles with updates` log entry lists the update for `rc-tooltip`.

## Link to the Renovate pull request

<https://github.com/renovatebot/renovate/pull/48166>
