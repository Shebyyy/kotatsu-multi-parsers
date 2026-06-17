# kotatsu-multi-parsers

Automatically builds and publishes parser JARs from multiple Kotatsu-based repos.

## Latest Release

Always available at: [Releases → latest](https://github.com/Shebyyy/kotatsu-multi-parsers/releases/latest)

## Latest Release

| Owner | JAR | Source Repo |
|-------|-----|-------------|
| Kotatsu-Redo | `Kotatsu-Redo.jar` | [kotatsu-parsers-redo](https://github.com/Kotatsu-Redo/kotatsu-parsers-redo) |
| YakaTeam | `YakaTeam.jar` | [kotatsu-parsers](https://github.com/YakaTeam/kotatsu-parsers) |
| TamerAli-0 | `TamerAli-0.jar` | [kotatsu-parsers](https://github.com/TamerAli-0/kotatsu-parsers) |
| glitch-228 | `glitch-228.jar` | [kaisoku-parsers](https://github.com/glitch-228/kaisoku-parsers) |
| hany18h | `hany18h.jar` | [kotatsu-parsers](https://github.com/hany18h/kotatsu-parsers) |

### Latest JAR Direct URLs

**Kotatsu-Redo.jar**
```
https://github.com/Shebyyy/kotatsu-multi-parsers/releases/latest/download/Kotatsu-Redo.jar
```

**YakaTeam.jar**
```
https://github.com/Shebyyy/kotatsu-multi-parsers/releases/latest/download/YakaTeam.jar
```

**TamerAli-0.jar**
```
https://github.com/Shebyyy/kotatsu-multi-parsers/releases/latest/download/TamerAli-0.jar
```

**glitch-228.jar**
```
https://github.com/Shebyyy/kotatsu-multi-parsers/releases/latest/download/glitch-228.jar
```

**hany18h.jar**
```
https://github.com/Shebyyy/kotatsu-multi-parsers/releases/latest/download/hany18h.jar
```

## How It Works

1. **Check** — every push, manual trigger, or every 6 hours, the workflow checks each repo for new commits
2. **Build** — only repos with new commits get built (in parallel), others are skipped
3. **Release** — if anything changed, a new release is published with all 5 JARs

> If no repos have new commits, no new release is created.

## Adding a Repo

Edit the `REPOS` list in [`.github/workflows/publish.yml`](.github/workflows/publish.yml) (it appears in both the `check` and `build` jobs):

```yaml
REPOS=(
    "owner/repo-name"
    ...
)
```

The JAR will be named `owner.jar` automatically.
