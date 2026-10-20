# Engineering notes

## Thin panels and local flexibility

The main panels are 0.80 mm thick. Keeping a large panel thin reduces material approximately in proportion to thickness: **V ≈ A t**, where A is panel area and t is thickness.

For an ideal rectangular beam section, **I = b t³ / 12** and bending rigidity is E I. This cubic thickness dependence explains why reducing thickness everywhere can quickly make a panel much more flexible. FoldDeckCase instead uses local thin regions for folds and latches.

<!-- MEDIA 06: Panel and hinge cross-section with dimensions beside the thickness equations. -->

## The two frequently operated fold bands

The two consecutive upper lid folds use nominal 2.00 mm bands with 0.20 mm minimum thickness. Other assembly folds use nominal 1.00 mm bands with 0.30 mm minimum thickness.

For ideal uniform bending, the outer-fiber strain can be approximated by **ε ≈ t θ / (2 L)**, where θ is in radians and L is the active bending length. A 0.20 mm band bent through 90 degrees over 2.00 mm gives roughly **7.85%**. If bending is concentrated into 1.50 mm, the same expression gives about **10.47%**.

These are geometric strain estimates, not allowable PLA strains or fatigue predictions. Printed strands, shoulder geometry, local creasing, and plastic deformation affect the real fold. A successful assembly does not establish repeated-cycle life.

<!-- MEDIA 07: Fold-band side profile showing t, L, and bend angle. -->

## Latch-root reliefs

All three hooks retain their tip and window locations. Each of the six slit endpoints extends 0.80 mm along its original slit direction toward the root, ending in an R0.40 mm relief. The widened root slit is 0.60 mm and transitions into the original 0.50 mm slit.

The surrounding 0.50 mm-thick flexible patches have square perimeter transitions in this version. The large patch is 24.00 × 11.50 mm; each smaller patch is 16.00 × 9.90 mm.

For an ideal small-deflection cantilever, **F = 3 E I δ / L³** and **εmax ≈ 3 t δ / (2 L²)**. At a fixed opening displacement δ, increasing active length L reduces the required force and root strain. Rounded slit ends remove sharp geometric tips, but these equations do not capture the actual large-deflection latch contact or establish its strength.

<!-- MEDIA 08: Dimensioned large and small latch details, with enlarged rounded slit endpoints. -->

## Validation scope

The v1.5 STEP file is a valid single solid and its mesh and seven-layer print project have been checked. Earlier printed prototypes and the faster print approach worked in the designer's tests. The latest root-relief changes still need a physical assembly test. No quantified drop, crush, retention-force, or hinge-fatigue results are available.

Useful next measurements are actual filament mass, complete print time, latch opening force, and the number of lid cycles before visible whitening or cracking.
