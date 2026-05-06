# harbor-mesh-shard-pipe

`harbor-mesh-shard-pipe` is a compact SQL repository for distributed systems, centered on this goal: Implement an SQL distributed systems project for shard visual model generation, using layout fixtures and stable geometry snapshots.

## Project Rationale

The point is to make a small domain rule concrete enough that a reader can change it and immediately see what broke.

## Harbor Mesh Shard Pipe Review Notes

Start with `quorum health` and `quorum health`. Those cases create the widest score spread in this repo, so they are the best quick check when the model changes.

## Feature Set

- `fixtures/domain_review.csv` adds cases for quorum health and lease drift.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/harbor-mesh-shard-walkthrough.md` walks through the case spread.
- The SQL code includes a review path for `quorum health` and `quorum health`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Architecture

The repository has two validation layers: the original compact policy fixture and the domain review fixture. They are separate so one can change without hiding failures in the other.

The SQL checks add a separate view over the domain review fixture.

## Usage

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Test Command

That command is also the regression path. It verifies the domain cases and catches mismatches between the CSV, metadata, and code.

## Next Improvements

The repository is intentionally scoped to local checks. I would expand it by adding adversarial fixtures before adding features.
