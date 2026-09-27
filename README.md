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
* SHA256 checksum v1.0: 087A862753D6427E53FA5615317F250693462B47974E048347102B423C7C5230
* Image count: 100
* Train/val/test split: 70/20/10

# Labeling rules
* I will label only areas with visible concrete material loss or detachment.
* I will not label cracks without concrete material loss.
* I will not label concrete scaling or honeycombing unless clear spalling is also present.
* I will not label stains, shadows or discoloration as spalling.
* I will not label very small or unclear damage that cannot be confidently identified as spalling.
* I will label partially visible spalling only when enough of the damaged area is visible to identify it confidently.

# How to reproduce
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/valentinavoetter/M4-U3-Assignment/blob/main/notebooks/M4-U3-Assignment.ipynb)

# Results summary (Roboflow)
* Precision: 62.5 %
* Recall: 83.3 %
* mAP: 65.7 %
* F1: 71.4 %

# Key takeaways:
1) Recall = 83.3 %. The problem framing was essentially that a missed spalling region is more costly than a false alarm because a missed defect would not be flagged for human inspection. With 83.3% recall, the model is finding a fairly large proportion of the annotated spalling instances. So the result is aligned with the objective you defined before training.
2) Precision = 62.5 %. The model is relatively liberal in identifying spalling. A precision of 62.5 % indicates that false positives are significant.
3) The model achieved an mAP@50 of 65.7 % indicating moderate object-detection performance on the test set. However, the relatively high recall (83.3 %) compared with precision (62.5 %) indicates that the model is more successful at finding existing spalling than at avoiding false-positive detections.
4) Results should be interpreted cautiously due to the limited test-set size. With a relatively small dataset, individual correct or incorrect detections can have a noticeable impact on the reported metrics. Further evaluation on a larger and more diverse set of unseen images would be necessary to assess the model's generalization to real-world inspection conditions.

# Reproducibility checklist
* Dataset version/link: v1.0/https://universe.roboflow.com/valentina-votter/m4-u3-assignment-d3j9b
* Model variant: YOLOv11
* Epochs: 10
* Batch: 16
* Image size: 640
* Ultralytics version: 8.4.163

# Reproducibility proof
* Date/time of las successful run: ()
* GPU/CPU used: ()
* Expected runtime range: ()
