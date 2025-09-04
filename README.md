
# QPSK Channel Estimation using Neural Networks

This mini-project demonstrates how to simulate a QPSK-based wireless communication system and use a simple neural network to estimate the complex channel coefficients (Rayleigh fading) from the received signal.


## 🚀 Project Goals

- Simulate a wireless system using QPSK modulation.
- Add Rayleigh fading and AWGN noise to simulate a realistic channel.
- Train a neural network to estimate the channel coefficients `h` from noisy signals.
- Evaluate the model using standard regression metrics (MAE, MSE, R²).
- Visualize predictions vs ground truth.


## 🛠️ Tools Used

- **Python**
- **NumPy**
- **Matplotlib**
- **Scikit-Learn**
- **TensorFlow / Keras**


## 📊 Dataset Generation

We simulate:
- Random bits → QPSK symbols.
- Rayleigh channel: `h ~ CN(0, 1)`
- Received signal: `y = h * x + n`
- Additive White Gaussian Noise (AWGN).

Input features:
``[Re(x), Im(x), Re(y), Im(y)]``  
Labels:
``[Re(h), Im(h)]``


## 🧠 Neural Network

- Input: 4 features (real & imag parts of x and y)
- Output: 2 values (real & imag parts of h)
- Loss: Mean Squared Error (MSE)
- Metrics: Mean Absolute Error (MAE), R² Score


## 📈 Results

MAE: 0.1767
MSE: 0.0489
R²: 0.9048

This indicates that the network is learning the channel coefficients quite accurately.


## 🧠 Summary

- QPSK modulation
- Rayleigh channel modeling
- Noise in digital communications
- Dataset creation for regression
- Neural network training and evaluation
- Model saving & reusability

## 🙌 Credits

This project was developed as a part of independent learning in digital communications and machine learning with guidance from educational resources and support from ChatGPT for conceptual clarity and coding assistance. Gratitude to the open-source community and the developers behind NumPy, Scikit-Learn, TensorFlow/Keras, and Matplotlib.
