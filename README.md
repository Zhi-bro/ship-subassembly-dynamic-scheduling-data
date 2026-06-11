# Benchmark Data for Diverse-Scene Dynamic Scheduling of Ship Sub-Assembly Construction

This repository provides the public data used for the manuscript:

**Multi-initialization meta-learning based diverse-scene dynamic scheduling for ship sub-assembly construction**

The dataset contains JSON-formatted benchmark input instances and dynamic disturbance-scene descriptors for computational experiments on dynamic ship sub-assembly construction scheduling.

## Contents

- `cases/`: 27 merged JSON case files.
- `LICENSE`: dataset reuse license.

Each case file is named:

```text
case_<N>-<R>-<P>.json
```

where:

- `N` is the number of ship sub-assemblies: `40`, `50`, or `60`.
- `R` is the fixed rescheduling interval: `20`, `25`, or `30` time units.
- `P` is the disturbance probability: `0.20`, `0.25`, or `0.30`.

The 27 files cover the full factorial design:

- `N = {40, 50, 60}`
- `R = {20, 25, 30}`
- `P = {0.20, 0.25, 0.30}`

## Case File Structure

Each JSON file has two main sections:

- `static_instance`: static scheduling input data.
- `dynamic_scenario_data`: dynamic scene descriptors and objective-function selections.

The `static_instance` section contains:

- `instance_parameters`: global case parameters, worker types, worker quantities, construction-site size, and shape ratios.
- `sub_assemblies`: sub-assembly operation data, including processing times, worker requirements of each operation, precedence relations, release time, due date, and spatial vertices.

The `dynamic_scenario_data` section contains:

- `dynamic_scene_count`
- `objective_position_order`
- `worker_type_order`
- `dynamic_scenes`

Each dynamic scene records:

- rescheduling time and previous rescheduling time
- actual rescheduling interval
- remaining operation count
- objective-function flags
- problem-setting changes from the static instance

## License

This dataset is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0). See `LICENSE` for details.

## Data Availability Statement

The data that support the findings of this study are openly available in GitHub at https://github.com/Zhi-bro/ship-subassembly-dynamic-scheduling-data.

## Ethics and Privacy

The released benchmark data are computational scheduling instances and dynamic scene descriptors generated for academic research and algorithmic comparison, without personal, human-subject, or sensitive private information.
