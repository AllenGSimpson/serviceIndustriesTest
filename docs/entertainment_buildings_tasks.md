# Entertainment Buildings Expansion

The following service industries are proposed for future development:

- Opera House
- Theater
- Bandstand
- Sports Stadium
- Radio Station
- Movie Theater
- Film Studio (industry)

This document outlines the tasks required to integrate these buildings and related systems.

## Tasks

1. **Define Building Group**
   - Create a new `bg_entertainment` building group in `common/building_groups/`.
   - Set urban category and appropriate lens (likely `development`).

2. **Add Building Definitions**
   - For each facility (`building_opera_house`, `building_theater`, `building_bandstand`, `building_sports_stadium`, `building_radio_station`, `building_movie_theater`, `building_film_studio`), add an entry in `common/buildings/` with icons, construction costs, and the `bg_entertainment` group.
   - Ensure levels_per_mesh and background art references are in line with existing hospitality buildings.

3. **Create Production Method Groups**
   - Each building requires a `pmg_base_building_*` group file in `common/production_method_groups/`.
   - Include at least one default production method per building.

4. **Implement Production Methods**
   - Add entries in `common/production_methods/` to convert input goods (e.g., paper, instruments, radios) into `service_entertainment` outputs.
   - Consider unique effects such as prestige or state modifiers for large venues (e.g., sports stadium prestige).

5. **Localization**
   - Add building and production method names in `localization/english/buildings_l_english.yml` and `production_methods_l_english.yml`.

6. **Design Notes Update**
   - Expand `Goals.md` with a short description of the Entertainment building group and reference this task file.
   - Document balancing considerations (input ratios, workforce mix, prestige bonuses).

