# Task [03]: [CIFAR-10 Animals (4 Classes)]

**Student:** [Saira]  
**ID:** [S203]  
**Seed:** [20240203]

## Presentation
https://docs.google.com/presentation/d/1l3Az2QSwpFzTCJ5ZTZFkpA5wf6rysFjj/edit?usp=sharing&ouid=112930185061834755496&rtpof=true&sd=true

## Dataset
- **Name:** [CIFAR-10]
- **Classes:** [4 (Cat, Deer, Dog, Horse)]
- **Training samples:** [20,000 images]
- **Test samples:** [4,000 images]

## Model Architecture
- **Type:** [Custom CNN (3 Blocks)]
- **Convolutional layers:** [3 (32, 64, 128 filters)]
- **Fully connected layers:** [2 (128 units and 4 units output)]
- **Total parameters:** [~280,000 parameters]

## Training Comparison

### Version 1
- **Learning rate:** [0.001]
- **Batch size:** [64]
- **Optimizer:** [Adam]
- **Test accuracy:** [83.17]%

### Version 2
- **Learning rate:** [0.001]
- **Batch size:** [64]
- **Optimizer:** [SGD with Momentum (0.9)]
- **Test accuracy:** [77.72]%

### Best Result
- **Best version:** Version [1]
- **Final test accuracy:** [83.17]%
- **Target accuracy:** [85]%
- **Status:** ✓ Achieved within 2% below

## Analysis
- **Best performing class:** [Dog]
- **Worst performing class:** [Cat]
- **Key observations:** [1. Data Augmentation (təsadüfi çevirmələr) modelin əzbərləməsinin (overfitting) qarşısını aldı və 83% hədəfinə çatmağa kömək etdi. 2. Adam optimizatoru bu kiçik datasetdə SGD-yə nisbətən daha sürətli və stabil nəticə göstərdi. 3. OneCycleLR scheduler-dən istifadə etmək modelin ilk epochlarda səhv istiqamətə getməsinin qarşısını aldı.]

## Files
- `notebook.ipynb`: Complete implementation with both training runs
- `results/training_comparison.png`: Comparison of Version 1 vs Version 2
- `results/confusion_matrix.png`: Confusion matrix from best model
- `results/predictions.png`: Sample predictions
