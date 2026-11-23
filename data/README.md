# Shared dataset record

Person 1 maintains this record. Do not upload raw frames or dataset exports to Git.

- Group number: pending
- Roboflow public URL: pending
- Frozen dataset version: pending
- Export/download instructions: pending
- Source metadata location (`frame_metadata.csv`): pending
- Original frame count / logo count / null count: pending
- Split strategy, proportions and seed: pending group agreement
- Preprocessing: pending
- Training augmentation: pending

Store a shared `data/splits/manifest.csv` with one row per original frame and columns `filename,video_source,split`, where split is `train`, `val` or `test`. Preserve the mapping between original and exported filenames. All model exports must retain this partition.

Recommended: group by source video to reduce leakage between related broadcast frames. Check duplicates and review broadcaster, region and logo-presence distributions after splitting. Keep augmentation derivatives in training only. Do not tune on the test set.

Before release, verify every allocated frame is reviewed, null frames are explicitly marked, only `Logo` is used, boxes are valid and tightly fitted to visible logos, and digital overlays are excluded. Record review findings and corrections.
