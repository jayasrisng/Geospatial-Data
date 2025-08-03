# 🛰️ GAN-Based Synthetic Data Generator for VR User Tracking

This project demonstrates how to preprocess and generate synthetic geospatial motion data using a GAN architecture in Google Colab. The data is sourced from the **User Tracking Dataset** on Kaggle, containing spatial and rotational motion telemetry of VR players.

🎯 **Use case**: Privacy-preserving user motion modeling in immersive environments.

📂 **Dataset**: `combined_data.csv` from Kaggle's *User Tracking Dataset*.  
Includes:
- Elapsed session time  
- Player body position (X, Y, Z)  
- Player body & head rotation (quaternion: X, Y, Z, W)

---

## 🛠️ Technologies Used

- **Google Colab + Python 3**
- **TensorFlow 2.15** for deep learning
- **Pandas, NumPy** for data wrangling
- **scikit-learn** for normalization (MinMaxScaler)
- **Matplotlib, Seaborn** for correlation heatmaps and feature analysis

---

## 🚀 Workflow

1. **Import Kaggle Data**
   - Auto-download + extract using Colab-compatible script
   - Supports temporary Kaggle tokened URLs

2. **Data Preprocessing**
   - Select numeric motion fields only
   - Normalize features in range `[-1, 1]` using `MinMaxScaler`

3. **GAN Architecture**
   - Generator: 2–3 hidden layers using ReLU/tanh
   - Discriminator: Fully connected classifier
   - Optimizers: Adam with binary crossentropy loss

4. **Training**
   - Trains GAN over 50 epochs using real + generated motion data
   - Logs epoch progress

5. **Synthetic Data Generation**
   - Generates new samples of player motion
   - Scales them back to original range
   - Exports to `synthetic_data.csv`

6. **Correlation Analysis (Optional)**
   - Plots encoded correlation matrices to inspect statistical realism
   - Saves as `correlation_matrix.csv`

---

## 📈 Output

- `new_synthetic_data.csv` — Normalized, GAN-generated user motion telemetry
- `correlation_matrix.csv` — Heatmap matrix of feature relations (if enabled)

---

## 🔐 Purpose & Ethics

This project is a proof of concept for **privacy-preserving data generation** from player telemetry. By learning to model behavior without storing real identifiable sequences, we enable:
- Ethical VR analytics
- Secure ML research
- Compliance with data protection frameworks (e.g., GDPR)

---

## 📄 License

MIT License — free to use, modify, and cite with attribution.

---

## 👩‍💻 Author

Created by [Jayasri](https://github.com/jayasrisng)  
