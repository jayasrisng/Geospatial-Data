# 🎯 GAN for VR Telemetry Data – Open in Colab

This notebook demonstrates how to use a Generative Adversarial Network (GAN) to generate synthetic telemetry data from a VR user tracking dataset. It includes secure data loading from Kaggle, preprocessing using MinMax scaling, and a full GAN training loop using TensorFlow.

> ✅ Designed for **Google Colab**  
> 📦 Uses real motion tracking data from Kaggle  
> 🔒 Supports data privacy and research reproducibility

---

## 📂 Dataset

We use the **User Tracking Dataset** from Kaggle. The script mounts and unpacks the dataset into `/kaggle/input` for use in this notebook.

**Includes:**  
- Elapsed time  
- Player body and head position/rotation (XYZ + quaternions)

---

## 🧰 Technologies Used

- **Python 3**
- **TensorFlow 2.15**
- **Pandas & NumPy**
- **scikit-learn (MinMaxScaler)**
- **Google Colab environment**

---

## 🚀 How to Run (Colab Instructions)

1. Click **"Open in Colab"** from the repo (if linked) or open this notebook manually in Google Colab.
2. Run the first cell to download and mount the Kaggle dataset.
3. Follow the notebook step-by-step:
   - Data preparation
   - Scaling features
   - Building the GAN (generator + discriminator)
   - Loss function and optimizer setup
   - Training for 50 epochs

---

## 📈 Output

After training:
- The generator learns to synthesize realistic user motion patterns.
- The discriminator differentiates real vs fake motion vectors.
- You can extend this pipeline to evaluate privacy-preserving synthetic data.

---

## 💡 Use Cases

- Safe simulation of VR telemetry
- Privacy-focused data generation for ML training
- Synthetic datasets for research and demo environments

---

## 📄 License

MIT License — free to use with credit.

---

## 👩‍💻 Author

Built by [Jayasri](https://github.com/jayasrisng) 
