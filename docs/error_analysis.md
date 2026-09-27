# False positives (see main/results/evidence/False positives)
* 1) What: Honeycombing. Why: The image shows a highly porous concrete area with extensive exposed coarse aggregate, consistent with the visual appearance of honeycombing rather than the defined spalling class. The model likely detects it as spalling with 85 % confidence because the irregular surface, exposed aggregate and apparent absence of mortar visually resemble the material-loss characteristics present in spalling examples.
* 2) What: Honeycombing/surface voiding. Why: The image shows an irregular concrete surface with localized cavities and exposed aggregate, which is more consistent with honeycombing or surface voiding than with the project definition of spalling. The model likely produces the false-positive detection at 65 % confidence because the rough, recessed texture and apparent material discontinuities resemble visual features learned from annotated spalling regions.
* 3) What: Surface scaling. Why: The image shows localized deterioration of the outer concrete surface, with a rough and partially detached-looking surface layer that is more consistent with scaling than with the defined spalling class. The model likely classifies this area as spalling with 80 % confidence because both defects can present irregular boundaries, rough textures and visible surface material loss, making them difficult to distinguish from image appearance alone.

# False negatives (see main/results/evidence/False negatives)
* What: (), Why: ()
* What: (), Why: ()
* What: (), Why: ()

# Next prioritized data improvements
* Adding more hard-negative examples: including more images of honeycombing, scaling, exposed aggregate, cracks and surface chipping without spalling to reduce false-positive detections.
* Increase diversity of spalling examples: add spalling at different sizes, shapes, lighting conditions, viewing angles, distances and concrete surface types to improve generalization to new inspection images.
* Review and refine annotations: re-check bounding boxes and ambiguous cases using the class definition to ensure consistent labeling, especially at the boundary between spalling, honeycombing and scaling.
