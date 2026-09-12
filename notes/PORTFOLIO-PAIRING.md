# Portfolio pairing playbook

How Kozphy keeps GitHub readable under the brand:

**CI/agent reliability × financial systems engineering**

## 1. One sentence per repo

Every description should answer: *what failure or decision does this reduce?*

Bad: "Python project for CI"
Good: "Dependency-aware CI failure orchestration with auditable self-healing"

## 2. Pairing rules

| Situation | Visibility | Naming |
| --- | --- | --- |
| Open product you want reused | Public only | short product name |
| Proprietary / portfolio-sensitive source | Private + public mirror | `Name` public, `Name-private` OR `name-public` docs mirror |
| Ops utility / incident tool | Private by default; public if safe & polished | keep Windows-specific tools secondary on profile |
| Coursework / fork / activator / unfinished | Unlist from narrative; archive or leave unpinned | do not feature |

## 3. Hero set (pin these)

1. `ci-failure-orchestrator`
2. `agentguard`
3. `EvalForge`
4. `finops-cloud-cost-platform-public`
5. `financial-analysis-tool`
6. `Kozphy.github.io` (optional sixth)

## 4. When creating a new pair

```bash
# Private workbench first
gh repo create Kozphy/<name> --private --source=. --remote=origin --push

# Public surface (docs-only or sanitized)
gh repo create Kozphy/<name>-public --public --description "Public portfolio showcase for <Name> (source is private)."
```

Cross-link in both descriptions:

- Private: `Public portfolio: https://github.com/Kozphy/<name>-public`
- Public: `Private source: https://github.com/Kozphy/<name>` (only if the private URL is meant to be known to you/collaborators; for true secrecy omit the private link from public README)

## 5. Profile surface

- Bio: short positioning line
- Profile README (`Kozphy/Kozphy`): pillars + 5 featured + pairing table
- Pins: hero set only
- Site: `https://kozphy.github.io` should repeat the same two pillars
