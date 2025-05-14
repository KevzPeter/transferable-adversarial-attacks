# 🧠 Jailbreaking Deep Models: Transferable Adversarial Attacks

This project investigates the adversarial vulnerability of deep image classifiers and the transferability of adversarial examples across modern neural architectures. We implement and evaluate several attack strategies on a pre-trained ResNet-34 model and test their effectiveness on DenseNet-121, MobileNetV3, and EfficientNet-B0 using a subset of the ImageNet-1K dataset.

---

---

## 🔍 Attacks Implemented

| Attack Type      | Description                                 |
| ---------------- | ------------------------------------------- |
| **FGSM**         | One-step L∞-bounded gradient sign method    |
| **PGD**          | Iterative version of FGSM with projection   |
| **Patch Attack** | Targeted attack localized to a 64×64 region |

Each attack is verified to comply with an L∞ constraint (`ε`), and adversarial examples are saved as `.png` files for transferability evaluation.

---

## 📊 Final Metrics

### ✅ ResNet-34 Accuracy

| Attack       | Top-1 (%) | Top-5 (%) |
| ------------ | --------- | --------- |
| Clean        | 76.00     | 94.20     |
| FGSM         | 6.00      | 35.40     |
| PGD          | 1.20      | 34.20     |
| Patch Attack | 35.40     | 68.40     |

### 🔁 Transferability (Top-1 / Top-5)

| Model           | FGSM          | PGD           | Patch         |
| --------------- | ------------- | ------------- | ------------- |
| DenseNet-121    | 70.80 / 92.20 | 72.20 / 92.20 | 66.40 / 87.60 |
| MobileNetV3     | 79.40 / 96.40 | 80.80 / 96.40 | 70.60 / 91.60 |
| EfficientNet-B0 | 79.40 / 96.40 | 79.80 / 96.40 | 75.20 / 93.80 |

> 📌 **Observation**: Patch attacks show the strongest transferability, especially to MobileNetV3.

---
