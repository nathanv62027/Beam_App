# Beam Designer

## Purpose and limitations
An educational and preliminary sizing tool that displays shear, moment, and
deflection diagrams for a beam and checks bending stress and deflection.
It is not a complete code-compliance check or a substitute for professional
engineering review. A passing result applies only to the checks listed here.

## Inputs
- Beam type: simply supported or cantilever, and span in feet. The cantilever's
  fixed end is identified.
- Downward point loads, each with a magnitude in kips and a position along the
  span in feet.
- Downward uniform loads over the full span, in kips per foot.
- Beam selection: a steel W-shape or a lumber section. Lumber selection
  includes species, grade, and nominal size; calculations use actual
  dimensions.
- Catalog properties for each beam include the data source, modulus of
  elasticity `E`, moment of inertia `Ix`, section modulus `Sx`, and weight per
  unit length. Catalog properties can be edited.
- User-provided allowable bending stress for the selected beam. Store it with
  an editable catalog entry when desired.
- Consistent units are shown for all inputs and outputs. Beam self-weight is
  included automatically from the selected beam's weight per unit length.

## Calculations
- Reactions, shear, and moment from statics for the supported beam types and
  listed load types.
- Deflection using linear-elastic, small-deflection beam behavior.
- Bending stress `fb = M/S`, using maximum absolute bending moment, compared
  with the user-provided allowable bending stress.
- Maximum absolute deflection under the total load, including self-weight,
  compared with `L/360`.
- If an allowable bending stress or required section property is missing,
  report that check as not evaluated rather than passing it.

## Outputs
- Beam, supports, applied loads, and the self-weight load.
- Shear, moment, and deflection diagrams, including units.
- Maximum absolute moment, bending stress, and deflection.
- Separate pass/fail results for bending and deflection, with the compared
  values and criteria. A pass is not a certification of the beam's overall
  safety.

## Look and feel
Clean and professional, with a fully specified example beam and loading
displayed when the app opens.

## Validation
For a 20 ft simply supported W12x26 with a 1 kip/ft external full-span uniform
load, include the beam's 26 lb/ft self-weight. Using `E = 29,000 ksi` and
`Ix = 204 in^4` for this validation case gives a total uniform load of
`1.026 kip/ft`, maximum moment of `51.3 kip-ft`, and maximum deflection of
approximately `0.625 in`. Verify the section properties against the selected
catalog source. Validate the pass/fail comparison separately using a specified
allowable bending stress.

## Out of scope
Continuous beams, buckling and lateral-torsional stability, shear strength,
bearing, connections, vibration, load combinations, and code-compliance
design.
