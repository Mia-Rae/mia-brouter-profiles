# Mia's MTB Trekking Brouter Profiles

Trekking profile for [Brouter](https://github.com/abrensch/brouter) that strongly avoids cars and adheres to cycle routes. Initially inspired by [Poutnik's profiles](https://github.com/poutnikl/Brouter-profiles).

> the general idea: avoid cars and traffic noise, and make it as pleasant a ride as possible
> with optional toggles for trekking bikes, or sticking to lit up paths/roads

---

### mtb-trekking-mia

> Peaceful, scenic routes with minimal car interaction; ~15-20% longer than usual trekking profile routes

- Base profile, extended by others
- Main logic `fuckcarspenalty`:
    - Avoids cars as much as possible
    - Chooses calm, quiet streets if necessary
    - Prefers real cycle tracks over painted bike lanes on main roads
    - Avoids multi-lane and high-speed roads
- Sticks to cycle routes on paved ways (`pavedbutnotlongdistancecyclewaypenalty`)
- On off-road paths, prefers easy, non-technical trails (`surfacequalitypenality`, `pathqualitypentalty`)

### Variations
- these are basically just presets for the toggles `non_mtb_bike`, `only_lit_ways` `avoid_adventure_route`, but those have a massisve effect
- (`allow_steps` & `allow_ferries` may also be set but are always `true` by default)


##### trekking-mia

> Quiet and calm routes, mostly compacted and paved surfaces

- Stricter `surfacequalitypenality` for non-compacted/paved surfaces
- Suitable for normal trekking bikes


##### lit-up-trekking-mia

> Routes through residential and quiet areas and paths, preferring lit-up streets/paths

- Limits `mtb-trekking-mia` to lit routes wherever reasonable
- **Highly experimental**, but seems to work well


##### mtb-adventure-mia
> out exploring in nature -- accepting to get stuck on sketchy or impassable ways sometimes, as it allows going down less surveyed paths

- strongly prefers easy, flowy trails (`mtb:scale=0|1|2`)
- but does not exclude un-surveyed ways in `surfacequalitypenality`, `pathqualitypentalty`, thus one will realistically get stuck exploring sketchy or impassable paths
- **Highly experimental**, dont expect to make it to your destination on time

## Limitations

- Tested only in Germany; performance in other countries may vary
- MTB or gravel bike recommended; trekking bike may struggle at times
