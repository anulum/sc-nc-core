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

SC-NC Core is being built as the root of the SC-NeuroCore split: the shared data model that every other SC-NC repository imports. It defines how neuron populations, connectivity graphs, model state, events, random seeds and numeric formats are represented and checked, and the protocol by which a computational backend is dispatched, and it imports no other SC-NC repository. Its current executable surface is repository validation tooling. It has no installed data-model package, backend dispatcher, numeric-format checker or qualified record schema.

Read [Architecture](ARCHITECTURE.md), [validation tooling](validation-tooling.md), [data boundaries](THREAT_MODEL.md) and the [repository boundary decision](adr/0001-repository-boundary.md).
