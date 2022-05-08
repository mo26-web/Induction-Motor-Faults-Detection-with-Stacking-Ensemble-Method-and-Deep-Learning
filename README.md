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

## Data Pre process
### FFT Transform (convolution)
FFT convolution uses the principle that multiplication in the frequency domain corresponds to convolution in the time domain. The input signal is transformed into the frequency domain using the DFT, multiplied by the frequency response of the filter, and then transformed back into the time domain using the Inverse DFT.
<p align="center">
<a href="https://docs.scipy.org/doc/scipy/_images/scipy-signal-fftconvolve-1_00.png"><img src="https://docs.scipy.org/doc/scipy/_images/scipy-signal-fftconvolve-1_00.png" align="center"></a>
</p>
