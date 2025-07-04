# QML

# Quantum-Inspired Machine Learning with Matrix Product States (MPS)

This project implements quantum-inspired machine learning models using Matrix Product States (MPS) for classification tasks, demonstrating the effectiveness of tensor networks in classical machine learning.

## Key Features

### Core Components
- **MPS-based Classifier**: Implements a tensor network classifier using Matrix Product States
- **Multiple Dataset Support**:
  - Synthetic datasets (linear, moons, circles, spiral)
  - MNIST digit classification (0s and 1s)
  - Custom feature mapping
- **Training Algorithms**:
  - Gradient-based optimization with momentum
  - Adaptive learning rate
  - Bond dimension adaptation via SVD truncation

### Technical Highlights
- **Quantum-Inspired Feature Maps**:
  ```python
  def phi(x, d):
      """Generalized feature map producing d-dimensional features"""
      terms = [np.cos((2*k+1)*np.pi/2 * x) for k in range(d//2)] + 
              [np.sin((2*k+1)*np.pi/2 * x) for k in range(d//2)]
      return np.array(terms)
