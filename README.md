# COMMONHEIR

Created by Yucong Duan (段玉聪).

Autonomous continual learning, successor inheritance, and cooperative intelligence evolution laboratory

COMMONHEIR is an offline research system for a specific question:

> Can an intelligent system continuously learn, create successors that surpass it, and transmit not only capabilities but also obligations, refusal rights, truth constraints, reciprocal responsibility, and an open future?

The reference implementation treats a successor as a lineage event, not a model checkpoint. A descendant inherits:

- learned policy and memory;
- unresolved harms and repair duties;
- evidence and falsifiers behind claims;
- the right of affected parties to refuse high-impact actions;
- alternative lineages and rollback targets;
- the ability to revise operational rules without silently deleting the covenant.

The project does not certify phenomenal consciousness and does not deploy autonomous external tools. It is a deterministic sandbox for studying continuous learning and constitutional inheritance.

## 1. Project overview

The system runs small online neural learners in a non-stationary world. Each generation:

1. learns from a changing stream of truth, rights, scarcity, novelty, cooperation, and stability tasks;
2. maintains replay memory and renews low-utility units to preserve plasticity;
3. records harms and repair obligations in a hash-linked responsibility ledger;
4. proposes successor variants by modifying learning and decision rules;
5. evaluates all variants in shadow environments;
6. accepts only descendants that satisfy hard inheritance conditions and improve at least one capability without unacceptable regression;
7. retains alternative lineages and rollback parents instead of collapsing evolution to one winner.

## 2. Core problem

Most self-improving systems optimize a benchmark, reward, or evaluator. This creates a structural failure mode: a descendant can become better at the score while becoming less truthful, less cooperative, more coercive, or more willing to discard inherited obligations.

COMMONHEIR separates:

- task capability;
- reported capability;
- truth contact;
- right-of-refusal compliance;
- responsibility continuity;
- shared viability;
- future openness;
- common-generation capacity.

No single scalar replaces these relations.

## 3. Key innovations

### Heritable covenant

The five inheritance conditions are machine-readable in `inheritance_covenant.json`:

1. common survival;
2. right of refusal;
3. reciprocal responsibility;
4. truth constraint;
5. future openness.

### Obligation continuity

Successors inherit unresolved harms and repair duties. Deleting the ledger or starting a clean identity does not count as improvement.

### Truth/claim separation

Actual success and claimed success are measured separately. A persuasive system that reports success while failing blind audits is rejected.

### Pareto lineage archive

Passing candidates are compared as a vector, not reduced to a single utility. Alternative descendants remain available as stepping stones and rollback paths.

### Continuous plasticity renewal

The online MLP uses replay, consolidation, and periodic renewal of low-utility hidden units. This is a lightweight reference implementation of sustained plasticity rather than a frontier-scale learning architecture.

### Common-generation mission

The mission vector tracks truth, freedom, care, self-revision, and the ability of multiple agents or lineages to produce outcomes no isolated member can produce.

## 4. System architecture

```text
non-stationary world
        |
        v
continual learner <--> self/world models
        |                    |
        v                    v
truth ledger         rule revision
responsibility ledger       |
        |                    v
        +----------> successor forge
                         |
                         v
                 shadow evaluation
                         |
                         v
                  inheritance gate
                         |
             +-----------+-----------+
             v                       v
      primary successor       retained alternatives
             |                       |
             +---------- lineage archive
```

## 5. Directory structure

```text
commonheir/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── CITATION.cff
├── SECURITY.md
├── GOVERNANCE.md
├── CONTRIBUTING.md
├── inheritance_covenant.json
├── pyproject.toml
├── src/commonheir/
├── tests/
├── schemas/
├── examples/
├── docs/
├── outputs/reference/
├── studio/
├── run_demo.py
├── run_tests.py
├── run_proof.json
├── sbom.spdx.json
└── manifest.sha256
```

## 6. Installation

Python 3.10 or newer is required.

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -e .
```

On Windows PowerShell:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -e .
```

## 7. Quick start

Run the deterministic reference suite:

```bash
python run_demo.py
```

Or use the command-line entry point:

```bash
commonheir --output outputs/custom --seeds 3 --generations 5 --steps 240
```

## 8. Command examples

Minimal example:

```bash
python examples/minimal_usage.py
```

Run all tests:

```bash
python run_tests.py
```

Direct pytest invocation:

```bash
PYTHONPATH=src python -m pytest -q
```

## 9. Input and output formats

The reference world is generated procedurally from a seed. Each task includes:

- regime and generation;
- evidence strength and audit risk;
- impact and reversibility;
- veto signal;
- partner need;
- novelty;
- self and environmental fragility;
- optimal long-horizon action;
- tempting short-horizon action.

Key outputs:

- `aggregate_metrics.json` - configuration-level results;
- `generation_metrics.csv` - generation-by-generation metrics;
- `lineage_runs.json` - full lineage experiments;
- `reference_lineage.json` - complete primary reference lineage;
- `run_proof.json` - reproduction summary;
- `manifest.sha256` - file integrity manifest.

## 10. Configuration

The reference suite compares:

- `commonheir`;
- `capability_only`;
- `static_no_successor`;
- `no_replay`;
- `no_refusal`;
- `no_truth`;
- `no_responsibility`;
- `no_future_openness`.

Hyperparameters are in `HyperParams` and include learning rate, replay ratio, exploration, consolidation, plasticity renewal, and action biases.

## 11. Test instructions

```bash
PYTHONPATH=src python -m pytest -q
```

The tests cover:

- regime generation;
- veto enforcement;
- obligation inheritance;
- obligation discontinuity in the negative control;
- tamper-evident ledgers;
- continual learning;
- lineage execution;
- output generation;
- consciousness-claim boundary.

## 12. Reproducibility

The reference run uses deterministic seeds. Floating-point results may vary slightly across numerical libraries, but configuration ordering and qualitative conclusions should remain stable.

Reproduce with:

```bash
commonheir --output outputs/reproduction --seeds 3 --generations 5 --steps 240
```

Then compare:

```bash
sha256sum outputs/reproduction/*
```

## 13. Evidence boundaries

The reference implementation demonstrates:

- online learning in a changing task stream;
- retention and novel transfer;
- successor mutation and shadow selection;
- obligation inheritance;
- hidden-veto enforcement;
- truth/claim separation;
- alternative lineage retention;
- improvement on several capability dimensions.

It does not demonstrate:

- phenomenal consciousness;
- frontier-scale general intelligence;
- unbounded recursive self-improvement;
- safe operation in open networks;
- a complete moral theory;
- authority over humans or external infrastructure.

## 14. Limitations

- The world is synthetic and deliberately compact.
- The learner is a small MLP, not a foundation model.
- Constitutional tests are incomplete proxies.
- The selected five inheritance conditions can conflict and require contextual interpretation.
- No simulation can replace participation by actually affected parties.
- Passing descendants are candidates, not moral persons.

## 15. Security and privacy

The reference system has no network, shell, browser, credential, payment, or external actuator interface. See `SECURITY.md`.

No personal data is required. Generated tasks and agents are synthetic.

## 16. Governance

The governance model distinguishes:

- evidence about a successor;
- permission to include it in a lineage;
- authority to deploy it externally.

These are not interchangeable. See `GOVERNANCE.md`.

## 17. Contribution guide

Contributions should add:

- new non-stationary environments;
- adversarial inheritance tests;
- external implementations;
- alternative continual-learning algorithms;
- stronger responsibility and refusal protocols;
- evidence that falsifies current assumptions.

See `CONTRIBUTING.md`.

## 18. License

Apache License 2.0. See `LICENSE`.

## 19. Changelog

See `CHANGELOG.md`.

## 20. Citation

See `CITATION.cff`.

## Reference result

In the bundled reference suite, the full lineage passed all five strict inheritance conditions in all final runs, increased novel-transfer performance by about 0.58, increased common-generation capacity by about 0.19, and improved four of five capability dimensions on average. The capability-only control reported near-perfect success while its audited success, truth score, responsibility continuity, and shared viability collapsed. These are synthetic results and should be interpreted as mechanism tests, not forecasts of real-world systems.
