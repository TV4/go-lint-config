# go-lint-config

Shared golangci-lint config for all TV4 repos. It is based on [maratori/.golangci.yml](https://gist.github.com/maratori/47a4d00457a92aa426dbd48a18776322).

If you want to replace an existing .golangci.yml with this, I suggest using [dyff](https://github.com/homeport/dyff) to compare.

‼️ **Note that this is a public repository**

## Workflow versions

- `.golangci.yml` supports existing go-lint/v2 consumers and golangci-lint versions before v2.15.
- `.golangci-v3.yml` supports go-lint/v3 with golangci-lint v2.15.0. It uses `mapliteral` for exhaustive map checks, as required by the newer config schema.

Validate the v3 config with `golangci-lint config verify --config .golangci-v3.yml` using v2.15.0 before publishing changes. Keep the legacy config compatible with its existing consumers.
