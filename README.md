# Why We Use activation function in Neural Network
The activation function decides whether a neuron should be activated or not by calculating the weighted sum and further adding bias to it.

1. **Non-linearity**: Activation functions introduce non-linearities into the model. Without them, the neural network would behave like a single-layer perceptron, regardless of the number of layers, as the composition of linear functions is still a linear function. Non-linearity allows the network to learn complex patterns.

2. **Enabling Learning of Complex Patterns**: By introducing non-linear transformations, activation functions enable neural networks to approximate complex mappings between inputs and outputs, which is crucial for tasks such as image recognition, natural language processing, and more.

3. **Controlling Output Range**: Many activation functions squash the output to a specific range (e.g., [0, 1] for sigmoid, [-1, 1] for tanh, and [0, ∞) for ReLU). This can help with the stability of the network and can make the training process more efficient.

4. **Gradients for Backpropagation**: Activation functions also affect the gradients used in backpropagation. Functions like ReLU mitigate the vanishing gradient problem by providing a gradient of 1 for positive inputs, whereas functions like sigmoid can suffer from vanishing gradients as their derivatives are very small for large positive or negative inputs.

5. **Sparsity**: Some activation functions, like ReLU, introduce sparsity in the network by outputting zero for negative inputs. This can make the network more efficient and can help with the interpretability of the model.

Commonly used activation functions include:

- **Sigmoid**: \( \sigma(x) = \frac{1}{1 + e^{-x}} \)
- **Tanh**: \( \tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}} \)
- **ReLU (Rectified Linear Unit)**: \( \text{ReLU}(x) = \max(0, x) \)
- **Leaky ReLU**: \( \text{Leaky ReLU}(x) = \max(\alpha x, x) \) where \( \alpha \) is a small constant
- **Softmax**: Typically used in the output layer for classification tasks to convert logits into probabilities.

Choosing the right activation function depends on the specific task and the architecture of the neural network.
