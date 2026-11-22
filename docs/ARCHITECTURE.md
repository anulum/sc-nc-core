<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SC-NC-CORE — repository foundation
-->

# Repository architecture

## Current executable tooling

**What it contains:** the repository's metadata, source-provenance, workflow, dependency-alignment, documentation, inventory and preflight controls.

**What each control does:** it inspects its fixed, declared local scope.

**What received metadata cannot do:** select another acceptance policy or grant domain authority.

Foundation qualification is in progress.

## Intended domain boundaries

| Record | Responsibility | Required evidence |
| --- | --- | --- |
| Population | Model identity, size, parameters and initial state of one neuron population | Parameter and shape checks against the model's declared ranges |
| Graph | Projections between populations, with their weights and delays | Endpoint, shape and delay-range checks, with no dangling projection |
| State | A snapshot of model state at one step, with the numeric format of every quantity | Round trip through each declared numeric format without silent loss |
| Event | A spike or other discrete event, with its source, time and payload | Ordering and range checks, with no event before its source exists |
| Seed | The seed and stream identity behind every stochastic draw | The same draws reproduced from the same seed and stream |
| Numerics | The numeric format of a quantity: fixed-point width and fraction bits, or floating type, and rounding | Declared range, rounding and saturation rules checked per format |

## Planned record schemas

- `sc_nc_core.population.v1`
- `sc_nc_core.graph.v1`
- `sc_nc_core.state.v1`
- `sc_nc_core.event.v1`
- `sc_nc_core.seed.v1`
- `sc_nc_core.numerics.v1`

These are planned identifiers. None of them is registered or qualified here.

Read [validation tooling](validation-tooling.md) for the executable repository interfaces.
