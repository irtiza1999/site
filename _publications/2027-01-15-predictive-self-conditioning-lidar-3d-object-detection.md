---
title: "Predictive Self-Conditioning for Accurate and Calibrated LiDAR 3D Object Detection"
collection: publications
category: conference
permalink: /publication/2027-01-15-predictive-self-conditioning-lidar-3d-object-detection
excerpt: 'This paper introduces Predictive Self-Conditioning (PSC), a within-frame feature-level feedback mechanism that converts Pass-1 proposals into confidence-weighted Gaussian heatmaps and injects them as a BEV feature residual before Pass-2, significantly boosting accuracy and calibration for LiDAR 3D object detection.'
date: 2027-01-15
venue: 'IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)'
citation: 'Sami Sadat, Md. Irtiza Hossain, Shreya Adrita Banik, Md Zia Uddin, Md. Golam Rabiul Alam. (2027). "Predictive Self-Conditioning for Accurate and Calibrated LiDAR 3D Object Detection." <i>IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)</i>. Accepted.'
---

Two-stage LiDAR detectors commit their bird's-eye-view (BEV) feature map before the detection head runs, so the evidence the first detection pass produces — where objects were found, and how reliable each detection is — can never improve the representation it was computed from. We close this gap with Predictive Self-Conditioning (PSC): a within-frame, feature-level feedback mechanism that converts Pass-1 proposals into per-class, confidence-weighted Gaussian heatmaps and injects them as a BEV feature residual before Pass-2, letting a detector refine its own representation from its own first-pass evidence, with no teacher and no temporal memory.

PSC is the core of our detector PSC-PV-RCNN, flanked by two optional modules: Density-Gated BEV Fusion (DGBF), enriching the features PSC conditions on, and a Region-Aware conditional variational autoencoder (RA-CVAE), a per-proposal uncertainty gate targeting calibration. PSC attaches to any detector that materialises a dense BEV map, and transfers across multiple backbones and head families: against matched baselines, it achieves +2.48 Moderate mAP on KITTI (+3.95 pedestrian, +3.44 cyclist) and +1.15 mean LEVEL 2 heading-weighted AP (APH) on the Waymo Open Dataset. In addition, the LiDAR-only Region-Aware CVAE lowers Expected Calibration Error (ECE) by 12.7% without requiring camera inputs.
