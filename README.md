# Automata-Driven Neural Network Model Compression

This repository explores the concept of **automata-driven neural network compression**, focusing on **weight pruning** to enhance model efficiency without sacrificing performance. The project integrates automata-based mechanisms to identify and remove insignificant weights, making it ideal for resource-constrained environments.

## Motivation

Neural network models often face challenges when deployed on devices with limited computational and memory resources. **Weight pruning** helps reduce model size and computational overhead while maintaining performance. By introducing automata-driven approaches, this project aims to optimize the pruning process further.

## Methodology

The **automata-driven pruning framework** works as follows:
1. Automata models identify connections with minimal contribution.
2. Insignificant weights are pruned iteratively while monitoring accuracy and loss.
3. The pruning process adapts dynamically based on the network's complexity.

This approach is demonstrated on two datasets: **MNIST** and **Breast Cancer Detection**, using standard models to showcase the benefits of automata-based pruning.

## Experimental Results

We tested both models for classification on the **MNIST dataset** and sklearn’s **Breast Cancer Detection dataset**. Both models were trained for **10 epochs** using the **Cross Entropy Loss** function. For Regression the **California Housing Dataset** was used with **10 epochs** and **MSE Loss** function. The results demonstrate the effectiveness of automata-driven pruning in reducing active connections while maintaining or improving accuracy.

### Observations:
- On the **MNIST dataset**, a **24.89% decrease** in weights was observed.
- On the **Breast Cancer Detection dataset**, a **7.14% decrease** in weights was noted.

Classification Datasets:

| Dataset         | Model          | Loss (CE) | Accuracy | Active Connections |
|-----------------|----------------|-----------|----------|--------------------|
| MNIST           | Simple Model   | 0.0885    | 97.81%   | 535,818            |
| MNIST           | Pruned Model   | 0.0880    | 98.35%   | 402,411            |
| Breast Cancer   | Simple Model   | 0.0525    | 98.25%   | 4,130              |
| Breast Cancer   | Pruned Model   | 0.0551    | 99.12%   | 3,835              |

Regression Datasets: 

| Dataset            | Model          | Loss (MSE) | Active Connections |
|--------------------|----------------|------------|--------------------|
| California Housing | Simple Model   | 0.3181     | 9473               |
| California Housing | Pruned Model   | 0.3256     | 8483               |




These results confirm that the **pruned model**:
1. Achieves **higher accuracy** in both datasets compared to the simple model.
2. Significantly **reduces active connections**, highlighting the efficiency of automata-driven pruning.

## Future Work

Future work will focus on enhancing efficiency and adaptability through:
- **Improved Automata Models:** Advancing automata mechanisms, including probabilistic and multi-state models, for better adaptability to complex architectures.
- **Generalization to Other Architectures:** Expanding the approach to CNNs and RNNs to improve performance across various tasks.
- **Integration with Other Compression Techniques:** Combining pruning with techniques like quantization and knowledge distillation for higher compression and maintained accuracy.

## Conclusion

This project demonstrates that automata-driven pruning can:
1. Significantly reduce active connections in neural networks.
2. Maintain or improve model accuracy across datasets.
3. Provide a scalable framework adaptable to diverse architectures and tasks.

By integrating advanced automata models and combining this approach with other compression techniques, automata-driven pruning has the potential to revolutionize model compression in resource-constrained environments.

---

