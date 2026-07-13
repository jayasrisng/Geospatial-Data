# Geospatial Data

**GAN-based synthetic motion-data generation for VR user tracking experiments.**

This project demonstrates preprocessing and synthetic-data generation for VR user-tracking telemetry. It uses a GAN workflow in Python/Colab to model spatial and rotational motion features from a user-tracking dataset.

## Problem

VR tracking data can expose behavioral patterns through body position, head rotation, and session timing. Synthetic data generation is one way to explore analytics workflows without relying directly on raw user traces.

This project asks:

> Can a lightweight GAN pipeline generate motion-like samples that preserve useful feature relationships for experimentation?

## Dataset context

The workflow is built around `combined_data.csv` from a Kaggle user-tracking dataset. Features include:

- elapsed session time;
- player body position `(X, Y, Z)`;
- body/head rotation represented as quaternion components.

## Workflow

1. Import and load the dataset.
2. Select numeric motion fields.
3. Normalize features with `MinMaxScaler`.
4. Train a simple GAN generator/discriminator.
5. Generate synthetic samples.
6. Scale outputs back to the original range.
7. Inspect feature relationships with correlation analysis.

## Outputs

- `new_synthetic_data.csv` — GAN-generated motion telemetry.
- `correlation_matrix.csv` — feature-correlation matrix when enabled.

## Tech stack

- Google Colab / Python
- TensorFlow 2.x
- pandas, NumPy
- scikit-learn
- Matplotlib, Seaborn
- GAN training workflow

## Case study

See [docs/case-study.md](docs/case-study.md) for the research framing, design choices, and limitations.

## Privacy note

This project should be treated as a proof of concept. Synthetic data generation does not automatically guarantee privacy. Any public examples should use permitted datasets, synthetic samples, or anonymized artifacts only.

## Current limitations

- Lightweight GAN architecture, not a production synthetic-data system.
- Dataset provenance and usage terms should be reviewed before redistribution.
- Privacy evaluation should be strengthened with explicit threat models and re-identification tests.
- Colab-first workflow should be converted into reproducible scripts if the project is extended.

## License

MIT License — use, modify, and cite with attribution.
