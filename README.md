# Get `aptos` action

This GitHub Action delivers specified [`solc`] release for a solc network.

[`solc`]: https://github.com/ethereum/solidity

> Please note that this is an initial release and will be improved as the Solc team make decisions on versioning, naming releases etc.

## Parameters

- `version` - Specified version of the release. Optional. Default value is `latest`.
- `prerelease` - Allow pre-release. Default value is `false`.
- `token` - GITHUB_TOKEN. Optional.

## Usage Example

Download the latest version of solc

```yaml
- name: get solce
  uses: pontem-network/get-solc@main
```

Download a specific version of solc

```yaml
- name: get solc
  uses: pontem-network/get-solc@main
  with:
    version: v0.8.15
```

Allow downloading pre-releases

```yaml
- name: get solc
  uses: pontem-network/get-solc@main
  with:
    prerelease: "true"
```

Download a specific version of solc and token

```yaml
- name: get solc
  uses: pontem-network/get-solc@main
  with:
    version: v0.8.15
    token: ${{ secrets.GITHUB_TOKEN }}
```