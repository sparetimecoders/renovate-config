# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) config presets for the sparetimecoders organization.

The [default.json](./default.json) file contains the shared presets.

## Usage

Add a `.github/renovate.json` file to your repository:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>sparetimecoders/renovate-config"]
}
```

Repo-specific overrides can be added alongside the extends:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>sparetimecoders/renovate-config"],
  "packageRules": [
    {
      "description": "Group TanStack packages",
      "matchPackagePatterns": ["^@tanstack/"],
      "groupName": "TanStack"
    }
  ]
}
```

## GitHub/Organization setup

Renovate GitHub App [setup](https://docs.renovatebot.com/modules/platform/github/#running-as-a-github-app)
