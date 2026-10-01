# Day 6 - Automated Log Aggregation

> Day 6 of 14 in the **Zero to Production Infrastructure & Security** series.

Centralised logging pipeline collecting and parsing syslog and auth logs into Grafana.

| | |
|---|---|
| **Day** | 6 of 14 |
| **Status** | Under construction |
| **Verification** | `docker compose -f docker-compose.yml config --quiet` |
| **Tags** | `loki`  `promtail`  `grafana`  `logging`  `observability` |

## Focus

- Promtail log scraping and labelling
- LogQL query and parsing regex
- Retention and compaction policy
- Real-time visualisation panels

## Status

Implementation lands during the Day 6 build session. Until then this
repository holds the agreed structure only - there is no placeholder code here
pretending to work.

The nightly pipeline appends the real verification result to [STATUS.md](STATUS.md).

## Layout

```
06-log-aggregation-loki/
  README.md        this file
  LICENSE          MIT
  STATUS.md        machine-written verification record
  .gitignore       shared from the series root
  .gitattributes   forces LF endings so bash scripts run on Windows
```

## Verify

```bash
docker compose -f docker-compose.yml config --quiet
```

The nightly job at 22:00 runs this command, records the result and
exit code in STATUS.md, then tags and pushes the repository.

## Licence

MIT. See [LICENSE](LICENSE).