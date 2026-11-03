# ProofCI demo

A tiny Rust ledger whose guarantees are proved in Lean and checked on every
pull request by [ProofCI](https://github.com/nhestrompia/proofci).

| File | Role |
|---|---|
| `src/lib.rs` | the Rust code (`calculate_fee`, `transfer`) |
| `proofci.yaml` | which guarantees are required |
| `proofci/Contract.lean` | what each guarantee means (protected: read from `main`) |
| `proofci/Proofs.lean` | why each guarantee holds (updated by pull requests) |

Open pull requests show the three outcomes: a change that keeps every
guarantee, a buggy change that breaks one, and a change that tries to weaken
the policy.
