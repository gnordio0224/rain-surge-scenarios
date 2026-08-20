# rain-surge-scenarios

Example files for modeling rain–storm surge scenarios along a coastal hillslope, set up to run in [Amanzi-ATS](https://github.com/amanzi/ats).

These files were used to produce the results reported in:

> Nordio, G., & Dennedy-Frank, P. J. **"Pre-Surge Rainfall Protects Coastal Groundwater from Storm Surge Salinization during Flooding Events."**

## Repository contents

1. **`.xml`** — The input file read by Amanzi-ATS.
2. **`.exo`** — The domain mesh file.
3. **`.h5`** — Boundary condition files containing sea level and meteorological forcing read by the model. These were synthetically generated in RStudio using the approach described in the Supplementary Material.

## Scenario naming

### `data_SS.h5` — Storm surge scenarios

Each column corresponds to a storm surge scenario:

| Column      | Surge height | Duration |
|-------------|--------------|----------|
| `lowSS`     | 1.5 m        | 24 h     |
| `highSS`    | 2.5 m        | 24 h     |
| `lowSSlong` | 1.5 m        | 48 h     |
| `highSSlong`| 2.5 m        | 48 h     |

### `data_Rain_SS.h5` — Rainfall scenarios (relative to surge onset)

Each column corresponds to a rainfall scenario, at either a **light** or **moderate** rate, starting a given time before surge flooding:

| Timing before surge | Light rain | Moderate rain |
|----------------------|-----------|----------------|
| 1 week + 1 day        | `L1`      | `M1`           |
| 1 day                 | `L2`      | `M2`           |
| 2 days                 | `L3`      | `M3`           |
| 1 week + 18 h          | `L4`      | `M4`           |
| 18 h                   | `L5`      | `M5`           |
| 12 h                   | `L6`      | `M6`           |
| Same time as surge onset | `SRl`   | `SRm`          |

For full details on scenario construction, see the Supplementary Material.
