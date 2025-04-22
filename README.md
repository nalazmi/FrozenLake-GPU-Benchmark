# 🧠 Q-Learning FrozenLake — CPU vs GPU Benchmark

This project adapts the original [Q-learning implementation](https://github.com/ronanmmurphy/Q-Learning-Algorithm) for the FrozenLake environment and benchmarks it using:

- ✅ **Pure Python with NumPy (CPU)**
- ✅ **GPU-accelerated PyTorch version**

---

## 🎯 Objective

> Optimize and benchmark Q-Learning on FrozenLake using GPU acceleration via PyTorch, and compare results with a CPU-based NumPy version.

---

## 📁 Files Included

- `Challenge11.ipynb` — Full implementation and benchmarking
- `README.md` — Project overview and results

---

## 🛠 Technologies Used

- Python 3.x
- `gym==0.26+` (FrozenLake-v1)
- `numpy==1.23.5`
- `torch`
- Google Colab (GPU)

---

## 📊 Benchmark Results

We trained the agent for **10,000 episodes** and recorded training times:

| Method            | Training Time (s)      |
|-------------------|------------------------|
| **CPU (NumPy)**   | `24.7515` seconds      |
| **GPU (PyTorch)** | `286.9483` seconds     |
| **Speed-Up**      | `0.09×` slower on GPU  |

---

## ⚠️ Key Observation

Despite using a GPU, the performance was slower. Reasons include:
- Very small Q-table (16×4)
- Lightweight environment
- GPU memory overhead outweighs benefit for this task

---

## ✅ Conclusion

While GPU acceleration is powerful, it's not always faster for small-scale problems.  
This project demonstrates how to:
- Migrate tabular Q-learning to GPU
- Benchmark it correctly
- Understand performance trade-offs

---

## 📚 Acknowledgements

- Based on: [ronanmmurphy/Q-Learning-Algorithm](https://github.com/ronanmmurphy/Q-Learning-Algorithm)
