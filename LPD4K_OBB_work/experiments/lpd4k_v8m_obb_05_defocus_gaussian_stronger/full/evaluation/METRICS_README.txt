Ratios are 0..1; multiply by 100 for percentages. No classification accuracy or background TN is invented.
mAP50 and mAP50-95 use the pinned Ultralytics OBB validator (ProbIoU-based matching).
Its summary P/R uses its own confidence-curve operating point, not the fixed threshold below.
The separate fixed metrics use exact convex-polygon IoU, same-class one-to-one matching,
predictions sorted by confidence, and the predeclared confidence/IoU thresholds.
precision=TP/(TP+FP); recall=TP/(TP+FN); F1=2PR/(P+R). Undefined ratios are stored as 0.
Mean matched IoU excludes false positives/misses; it is not an overall accuracy score.
The iou argument to predict/val controls NMS, not the true-positive matching threshold.
Official OBB mAP and custom polygon-IoU metrics are distinct and need not be numerically identical.
Do not tune hyperparameters or thresholds on the test split. Smoke results are not reportable research results.
Ground-truth crops were produced independently BEFORE any model prediction.
