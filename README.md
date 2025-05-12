# Jailbreaking Deep Models: Transferable Adversarial Attacks

### ✅ Task 1: Baseline Evaluation

- Evaluate ResNet-34 on the provided 500-image dataset
- Report Top-1 and Top-5 accuracy

### ✅ Task 2: FGSM (L∞ Attack)

- Implement Fast Gradient Sign Method (ε=0.02)
- Visualize perturbations
- Save perturbed images in `AdversarialTestSet1/`

### ✅ Task 3: Improved Attack (PGD)

- Iterative gradient sign method (PGD, 10 steps)
- Greater accuracy drop than FGSM
- Save images in `AdversarialTestSet2/`

### ✅ Task 4: Targeted Patch Attack

- Modify only a 32×32 patch in each image
- Use higher ε (0.3) for effectiveness
- Save images in `AdversarialTestSet3/`

### ✅ Task 5: Transferability

- Evaluate all three attack sets across:
  - DenseNet-121
  - MobileNetV3-Large
  - EfficientNet-B0
- Present results with relative accuracy drop

---

## 📊 Results Summary

| Model               | Original | FGSM           | PGD            | Patch (Targeted) |
| ------------------- | -------- | -------------- | -------------- | ---------------- |
| **DenseNet-121**    | 74.8%    | 38.6% (-48.4%) | 36.4% (-51.3%) | 39.6% (-47.0%)   |
| **MobileNetV3**     | 83.8%    | 40.4% (-51.8%) | 40.8% (-51.3%) | 40.8% (-51.3%)   |
| **EfficientNet-B0** | 83.0%    | 41.2% (-50.4%) | 40.8% (-50.8%) | 44.0% (-47.0%)   |

_All accuracy values refer to Top-1. Full tables in the notebook._

---

## 📌 Requirements

```bash
torch >= 2.0
torchvision >= 0.15
numpy
matplotlib
Pillow
tqdm
pandas
```
