# Architecture Notes: 3D Tumor Segmentation (MRI)

## Pipeline

```text
MRI Volume -> Preprocessing -> 3D Segmentation Model -> Tumor Mask -> Metrics + 3D Visualization
```

## Components

- 3D MRI preprocessing
- Tumor segmentation model
- Tumor mask generation
- Evaluation metrics (Dice, IoU, sensitivity)
- 3D visualization

## Design Notes

- Keep provider/model choices swappable behind interfaces (see `multi-llm-router`
  and similar projects in this portfolio for the general pattern).
- Prefer configuration-driven pipelines (YAML/JSON in `configs/`) over hardcoded
  parameters so experiments are reproducible.
