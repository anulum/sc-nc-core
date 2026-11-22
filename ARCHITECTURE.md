<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SC-NC-CORE — repository foundation
-->

# Architecture

## Current executable surface

The checkout contains:
- repository validation tooling;
- dedicated tests;
- workflow definitions;
- native documentation.

No domain component of SC-NC Core is implemented yet, and no code has moved here from SC-NeuroCore. The metadata keeps domain capabilities, claims and qualified record formats empty.

## Intended records

1. **Population:** Model identity, size, parameters and initial state of one neuron population.
2. **Graph:** Projections between populations, with their weights and delays.
3. **State:** A snapshot of model state at one step, with the numeric format of every quantity.
4. **Event:** A spike or other discrete event, with its source, time and payload.
5. **Seed:** The seed and stream identity behind every stochastic draw.
6. **Numerics:** The numeric format of a quantity: fixed-point width and fraction bits, or floating type, and rounding.

## Ownership

**This project owns** the planned SC-NC Core records and boundary rules.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| neuron and synapse models and model descriptors | SC-NC Catalogue |
| simulation, native lanes and checkpoints | SC-NC Engine |
| the public package, documentation and releases of the monolith | SC-NeuroCore |

## Interpretation

- **Formats.** A declared numeric format is a representation rule, not an accuracy claim for any model.
- **Moves.** Code arrives only through SC-NeuroCore's split import gate, unit by unit; a planned move is not a moved capability.

Read [the documentation architecture](docs/ARCHITECTURE.md) for the planned records, rules and schema identifiers.
