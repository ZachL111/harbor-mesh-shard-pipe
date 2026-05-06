# Harbor Mesh Shard Pipe Walkthrough

This note is the quickest way to read the extra review model in `harbor-mesh-shard-pipe`.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | quorum health | 160 | ship |
| stress | lease drift | 172 | ship |
| edge | replica lag | 190 | ship |
| recovery | membership churn | 202 | ship |
| stale | quorum health | 205 | ship |

Start with `stale` and `baseline`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

`stale` is the optimistic case; use it to make sure the scoring path still rewards strong signal.
