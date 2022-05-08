# Induction-Motor-Faults-Detection-with-Stacking-Ensemble-Method-and-Deep-Learning
This is a induction motor faults detection project implemented with Tensorflow. We use Stacking Ensembles method (with Random Forest, Support Vector Machine, Deep Neural Network and Logistic Regression) and Machinery Fault Dataset dataset available on kaggle.

## Machinery Fault Dataset
This database is composed of 1951 multivariate time-series acquired by sensors on a SpectraQuest's Machinery Fault Simulator (MFS) Alignment-Balance-Vibration (ABVT). The 1951 comprises six different simulated states: normal function, imbalance fault, horizontal and vertical misalignment faults and, inner and outer bearing faults. This section describes the database. For more info please check : http://www02.smt.ufrj.br/~offshore/mfs/page_01.html
<p align="center">
<a href="https://github.com/mo26-web/Induction-Motor-Faults-Detection-with-Stacking-Ensemble-Method-and-Deep-Learning/blob/main/image/motor.jpg"><img src="https://github.com/mo26-web/Induction-Motor-Faults-Detection-with-Stacking-Ensemble-Method-and-Deep-Learning/blob/main/image/motor.jpg" align="center"></a>
</p>

## Visualization of Some Features
<p align="center">
<a href="https://github.com/mo26-web/Induction-Motor-Faults-Detection-with-Stacking-Ensemble-Method-and-Deep-Learning/blob/main/image/results1.png"><img src="https://github.com/mo26-web/Induction-Motor-Faults-Detection-with-Stacking-Ensemble-Method-and-Deep-Learning/blob/main/image/results1.png" align="center"></a>
</p>

<p align="center">
<a href="https://github.com/mo26-web/Induction-Motor-Faults-Detection-with-Stacking-Ensemble-Method-and-Deep-Learning/blob/main/image/results2.png"><img src="https://github.com/mo26-web/Induction-Motor-Faults-Detection-with-Stacking-Ensemble-Method-and-Deep-Learning/blob/main/image/results2.png" align="center"></a>
</p>

## Data Pre-Process
### FFT Transform (convolution)
FFT convolution uses the principle that multiplication in the frequency domain corresponds to convolution in the time domain. The input signal is transformed into the frequency domain using the DFT, multiplied by the frequency response of the filter, and then transformed back into the time domain using the Inverse DFT.
<p align="center">
<a href="https://docs.scipy.org/doc/scipy/_images/scipy-signal-fftconvolve-1_00.png"><img src="https://docs.scipy.org/doc/scipy/_images/scipy-signal-fftconvolve-1_00.png" align="center"></a>
</p>

## Stacking Ensemble Method
Stacking or Stacked Generalization is an ensemble machine learning algorithm. It uses a meta-learning algorithm to learn how to best combine the predictions from two or more base machine learning algorithms.The benefit of stacking is that it can harness the capabilities of a range of well-performing models on a classification or regression task and make predictions that have better performance than any single model in the ensemble.
The architecture of a stacking model involves two or more base models, often referred to as level-0 models, and a meta-model that combines the predictions of the base models, referred to as a level-1 model.

Level-0 Models (Base-Models): Models fit on the training data and whose predictions are compiled.
Level-1 Model (Meta-Model): Model that learns how to best combine the predictions of the base models.
The meta-model is trained on the predictions made by base models on out-of-sample data. That is, data not used to train the base models is fed to the base models, predictions are made, and these predictions, along with the expected outputs, provide the input and output pairs of the training dataset used to fit the meta-model.

The outputs from the base models used as input to the meta-model may be real value in the case of regression, and probability values, probability like values, or class labels in the case of classification.
