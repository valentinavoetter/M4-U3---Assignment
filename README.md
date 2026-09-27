# M4-U3 - Assignment
This repository includes all the deliverables required for the M4-U3 - Assignment on Computer Vision. This model is an assistive tool for preliminary screening only. It produces false negatives. It must NOT be used as the sole verifier for life-safety decisions.

# Problem framing
* Object of interest: Concrete spalling.
* Environment: Exposed concrete surfaces in buildings and civil infrastructure, captured under varying indoor and outdoor conditions.
* Critical metric: Recall.
* Success criteria: The model should detect the majority of visible spalling instances in unseen images while maintaining acceptable precision.
* Failure mode: False negatives, where visible concrete spalling is present but not detected by the model. Secondary failure modes include false positives caused by visually similar features such as concrete scaling and honeycombs.

# How to install
()

# Class definitions
See docs/class_definitions.md

# Dataset
* Roboflow link: https://universe.roboflow.com/valentina-votter/m4-u3-assignment-d3j9b
* Release URL v1.0:
* SHA256 checksum v1.0: 087A862753D6427E53FA5615317F250693462B47974E048347102B423C7C5230
* Release URL v2.0: ()
* SHA256 checksum v2.0: ()
* Image count: 120
* Train/val/test split: 70/20/10

# Labeling rules
* I will label only areas with visible concrete material loss or detachment.
* I will not label cracks without concrete material loss.
* I will not label concrete scaling or honeycombing unless clear spalling is also present.
* I will not label stains, shadows or discoloration as spalling.
* I will not label very small or unclear damage that cannot be confidently identified as spalling.
* I will label partially visible spalling only when enough of the damaged area is visible to identify it confidently.

# How to reproduce
* ![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)
* Open in Google Colab: [https://colab.research.google.com/github/ValentinaVotter/M4-U3---Assignment/blob/main/notebooks/M4-U3%20-%20Assignment.ipynb]

# Results summary
* Precision: ()
* Recall: ()
* mAP: ()
* Key takeaways: ()

# Reproducibility checklist
* Dataset version/link: v2/()
* Model variant: YOLOv11
* Epochs: 50
* Batch: ()
* Image size: ()
* Ultralytics version: ()

# Reproducibility proof
* Date/time of las successful run: ()
* GPU/CPU used: ()
* Expected runtime range: ()
