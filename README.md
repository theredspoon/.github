# Organization Configuration

This repository contains organization-wide defaults for all `theredspoon` repositories.

## What's in here

### `renovate.json` - Dependency Update Automation

Organization-wide Renovate configuration that applies to all repositories.

**Schedule:**
- Minor/patch updates: Weekly (Mondays 3am ET)
- Major updates: Monthly (1st of month, 3am ET)
- Security updates: Immediate

**Automerge:**
- ✅ Patch updates for stable packages (v1.x.x → v1.x.y)
- ✅ GitHub Actions updates
- ❌ Minor/major updates (require manual review)

**Individual repos can override** by creating their own `.github/renovate.json`:

```json
{
  "extends": ["github>theredspoon/.github"],
  "packageRules": [
    // Add repo-specific rules here
  ]
}
```

## How it works

GitHub automatically uses configuration from this repo as defaults for:
- Community health files (CODE_OF_CONDUCT, CONTRIBUTING, SECURITY, etc.)
- Issue/PR templates
- Funding info
- Renovate configuration
- Dependabot configuration

See: https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file
