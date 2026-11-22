<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SC-NC-CORE — repository foundation
-->

# SC-NC Core

SC-NC Core is being built as the root of the SC-NeuroCore split: the shared data model that every other SC-NC repository imports. It defines how neuron populations, connectivity graphs, model state, events, random seeds and numeric formats are represented and checked, and the protocol by which a computational backend is dispatched, and it imports no other SC-NC repository. This checkout contains repository validation tooling and documentation only. Full foundation qualification is in progress. There is no installed data-model package, backend dispatcher, numeric-format checker or qualified record schema.

SC-NC Core is part of the **SC Neuromorphic Computing Systems** group (SC-NEUROMORPHIC-COMPUTING-SYSTEMS). The [group and project map](https://github.com/anulum/sc-neurocore/blob/main/docs/ecosystem.md) shows the whole programme and where this repository sits in it.

**What does not exist yet:**
- any code moved from SC-NeuroCore;
- a registered runtime record schema;
- an installed data-model package, backend dispatcher or numeric-format checker.

## Boundary

**What this project owns:**

| Record | Scope |
|---|---|
| Population | Model identity, size, parameters and initial state of one neuron population |
| Graph | Projections between populations, with their weights and delays |
| State | A snapshot of model state at one step, with the numeric format of every quantity |
| Event | A spike or other discrete event, with its source, time and payload |
| Seed | The seed and stream identity behind every stochastic draw |
| Numerics | The numeric format of a quantity: fixed-point width and fraction bits, or floating type, and rounding |

**Static imports:** none. SC-NC Core sits at the root of the SC-NC split and imports no other SC-NC repository.

**Records read without importing their code:** SC-NeuroCore, every other SC-NC repository, Mutation SNN and SNN Divergence Harness read this repository's records.

**Records it reads without importing their code:** none. It reads no other repository's records.

**Code planned to move here from SC-NeuroCore,** package by package, when SC-NeuroCore's split import gate allows it: `core`, `identity`, `math`, `utils`, `integrators` (the ode, stiff and symplectic solvers) and `_version` (the version module).

**Explicit non-claims and operating boundaries:**
- It contains no neuron model, simulator, compiler, trainer or hardware driver.
- A numeric format describes a quantity; it does not certify accuracy for a model or a target.

## Current tooling

Repository controls inspect:
- metadata and source attribution;
- workflows and dependency alignment;
- native documentation and repository inventory;
- preflight orchestration.

Metadata declares architecture-only maturity with empty implemented domain capability and claim inventories.

- Use the exact environment in [Contributing](CONTRIBUTING.md).
- Full CI and preflight belong in CI or in an explicitly admitted pre-push environment.
- See [Validation](VALIDATION.md) for the maintained validation scope.

## Intended evidence

Every future record will carry its source and environment digests, its numeric formats where it has them, and its explicit verification boundary. None of the planned record schemas is registered or qualified by this foundation.

## Documentation and support

Read [Architecture](ARCHITECTURE.md), [support](SUPPORT.md), [security reporting](SECURITY.md) and [citation metadata](CITATION.cff).

**Not claimed:**
- a hosted service, released package or DOI;
- a public CI status;
- a performed simulation, hardware measurement or benchmark result.

## Licence

Source is licensed under [AGPL-3.0-or-later](LICENSE). A commercial licence is available through the contact in [NOTICE](NOTICE.md).

![ANULUM](docs/assets/anulum_logo_company.jpg)

![Fortis Studio](docs/assets/fortis_studio_logo.jpg)

## Text and data mining reservation
The rightsholder, Miroslav Šotek (ANULUM), expressly reserves the use of the
works in this repository for text and data mining, including the collection of
this content for, and its use in, training, fine-tuning or evaluating machine
learning and artificial intelligence models, in accordance with Article 4(3) of
Directive (EU) 2019/790 and the national provisions transposing it.

No permission for such use has been granted beyond what the licence in
`LICENSE` grants. This reservation does not change that licence: uses the
licence permits remain permitted on its terms, including its attribution and
share-alike conditions.

Reservation made on 2026-11-22. Requests for permission: contact the
rightsholder through the contact listed in this repository.
