# Simpsons Character Classifier: Perceptron from Scratch

A multi-class perceptron, written from scratch in Python, that classifies images of 10 Simpsons characters from the [Simpsons-MNIST](https://github.com/alvarobartt/simpsons-mnist) dataset using a one-vs-rest strategy.

## What I built
- Binary perceptron with the classic perceptron learning rule, extended to 10 classes with one-vs-rest
- Training loop with per-epoch shuffling and two stopping criteria (fixed epochs vs error threshold)
- Hyperparameter tuning over learning rate, normalisation and weight initialisation
- Evaluation with accuracy, precision, recall, F1 and confusion matrices, for both RGB (2,352 features) and grayscale (784 features)

## Findings
- **Colour matters:** RGB inputs outperformed grayscale in every configuration. For one character, precision jumped from 0.27 in grayscale to 0.95 in RGB.
- A single-layer linear model hits a ceiling on this task. This motivated the move to neural networks in my FashionMNIST neural network project.

## Run it
1. Download Simpsons-MNIST and place the `dataset/` folder under `data/`.
2. `pip install -r requirements.txt`
3. Open `simpsons_perceptron.ipynb` and run all cells.

*Built for CSC2042S Machine Learning, University of Cape Town (2025).*
