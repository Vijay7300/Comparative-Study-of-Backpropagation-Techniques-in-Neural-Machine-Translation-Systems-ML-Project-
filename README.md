 Improving Translation Quality using SGD, Adam, RMSProp & Adagrad  
 IIT Jodhpur | Machine Learning Project  

##  Overview
This project presents a **comparative analysis of optimization algorithms** used in **Neural Machine Translation (NMT)** systems, specifically for the **English–Hindi language pair**.
We implemented a **Sequence-to-Sequence (Seq2Seq) model with Attention** and evaluated how different optimizers impact translation quality and training stability.

##  Objectives
- Compare performance of different optimizers in NMT  
- Analyze training stability and convergence behavior  
- Evaluate translation quality using BLEU score  
- Study optimizer effectiveness in **low-resource settings**  

##  Key Concepts
- Neural Machine Translation (NMT)  
- Seq2Seq Architecture with Attention  
- Backpropagation & Optimization Algorithms  
- Gradient Descent Variants  
- BLEU Score Evaluation  

##  Technologies Used
- Python  
- PyTorch / TensorFlow  
- NumPy, Pandas  
- Matplotlib / Seaborn  

##  Model Architecture
- Encoder-Decoder (Seq2Seq) Model  
- Attention Mechanism  
- Tokenization & Embedding  
- Training via Backpropagation  

##  Optimizers Compared

### 🔹 SGD (Stochastic Gradient Descent)
- Basic optimizer  
- Slow convergence  

### 🔹 Adam
- Adaptive learning rate  
- Combines momentum + RMSProp  

### 🔹 RMSProp  (Best Performer)
- Stable convergence  
- Handles noisy gradients effectively  

### 🔹 Adagrad
- Adaptive per-parameter learning rate  
- Performs well on sparse data  

##  Results & Performance

| Optimizer | BLEU Score | Improvement |
|----------|-----------|------------|
| SGD      | 5.76      | Baseline   |
| Adam     | 9.79      | +69.97%    |
| Adagrad  | 13.73     | +138.37%   |
| RMSProp  | **17.63** | 🚀 +206.08% |

##  Key Findings
- **RMSProp achieved highest translation quality**  
   Adagrad outperformed Adam significantly  
-  Adam was not optimal in low-resource settings  
-  SGD showed very slow convergence  

##  Training Insights
- RMSProp → Smooth & stable convergence  
- Adam → Oscillations in later epochs  
- SGD → Slow learning  
- Adagrad → Strong intermediate performance  

##  Example Translations

| English | Hindi (RMSProp) |
|--------|----------------|
| Hello, how are you? | Namaste, aap kaise hain? |
| I go to school | Main school jaata hoon |
| This is a good day | Yeh ek accha din hai |

