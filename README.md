# Mia's Brouter Profiles

Trekking profile for [Brouter](https://github.com/abrensch/brouter) that strongly avoids cars and adheres to cycle routes. Inspired by [Poutnik's profiles](https://github.com/poutnikl/Brouter-profiles).

## Main Profiles

### mtb-trekking-mia

> Peaceful, scenic routes with minimal car interaction; ~20% longer than standard trekking profile

- Base profile, extended by others
- Main logic `fuckcarspenalty`:
    - Avoids cars as much as possible
    - Chooses calm, quiet streets if necessary
    - Prefers cycle tracks over painted bike lanes on main roads
    - Avoids multi-lane and high-speed roads
- Sticks to cycle routes on paved ways (`pavedbutnotlongdistancecyclewaypenalty`)
- On off-road paths, prefers easy, non-technical trails (`surfacequalitypenality`, `pathqualitypentalty`)

### trekking-mia

> Quiet and calm routes, mostly compacted and paved surfaces

- Stricter `surfacequalitypenality` for non-compacted/paved surfaces
- Suitable for normal trekking bikes

### lit-up-trekking-mia

> Routes through residential and quiet, lit-up streets

- Limits `mtb-trekking-mia` to lit routes wherever reasonable
- **Highly experimental**

## Limitations

- Tested only in Germany; performance in other countries may vary
- Suitable for trails and paths as long as they are not too rough
- MTB or gravel bike recommended; trekking bike may struggle at times