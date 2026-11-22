# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) presets.

| Preset | For | Adds |
| --- | --- | --- |
| `local>bendrucker/renovate-config` | Every repo | `config:recommended`, automerge for minor/patch/pin/digest, majors manual |
| `local>bendrucker/renovate-config:application` | Repos that ship their lockfiles (installed or deployed code) | Weekly lock file maintenance, automerged |
| `local>bendrucker/renovate-config:library` | Published packages, where consumers resolve their own ranges | `rangeStrategy: widen`, no lock file maintenance |

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>bendrucker/renovate-config:application"]
}
```

Repo-specific rules (custom managers, schedules, groups) stay in each repo's own config.
