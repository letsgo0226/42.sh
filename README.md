# 42.sh

Stateful prime-scan TM; at tick 3 the Gödel product is **42**.

| Artifact | Role |
|----------|------|
| `42.sh` | One-liner (~1641B) |
| `42_DAEMON.sh` | Resident loop (default 1s) |
| `.github/workflows/42.yml` | Actions `*/5` |

```sh
rm -f state.json
LOG_TM_STATE=state.json CMD=step N=3 bash 42.sh
nohup bash 42_DAEMON.sh 1 >> 42_daemon.log 2>&1 &
```

Bound: formal consistency (`C`/`CF`) only — not a physical TOE proof.
