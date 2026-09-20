# M4-U3 - Assignment
This repository includes all the deliverables required for the M4-U3 - Assignment on Computer Vision.

# Problem framing
* Object of interest: Concrete spalling.
* Environment: Exposed concrete surfaces in buildings and civil infrastructure, captured under varying indoor and outdoor conditions.
* Critical metric: Recall.
* Success criteria: The model should detect the majority of visible spalling instances in unseen images while maintaining acceptable precision.
* Failure mode: False negatives, where visible concrete spalling is present but not detected by the model. Secondary failure modes include false positives caused by visually similar features such as concrete scaling and honeycombins.

# Class definitions
See docs/class_definitions.md

# Dataset
* Roboflow link: ()
* Image count: 120
* Train/val/test split: ()

# Labeling rules
* I will label only areas with visible concrete material loss or detachment.
* I will not label cracks without concrete material loss.
* I will not label concrete scaling or honeycombing unless clear spalling is also present.
* I will not label stains, shadows or discoloration as spalling.
* I will not label very small or unclear damage that cannot be confidently identified as spalling.
* I will label partially visible spalling only when enough of the damaged area is visible to identify it confidently.
