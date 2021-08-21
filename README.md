# QuantumHackEarth
My contribution to Qiskit in HackEarth

An hybrid Quantum-Classical Neural Network application for image classification!
Motivated by the task of classifying eliptical from spyral galaxies.

The classifier takes a dataset of MNISTimages (in this case), then donwscale it into a dataset of nxn size images with values inside (0,1) in pytorch tensor form.

The data is then labeled with booleans (0,1).

The classical data is entered in a CircuitQNN [See Qiskit Tutorials](https://qiskit.org/documentation/machine-learning/tutorials/05_torch_connector.html)
This uses a ZZFeatureMap which encodes the data of (N_pixels) in N Qbits storing information in the amplitudes.

The optimizer and loss function choosen are the ones suggested by Qiskit Tutorials in this case. Botch coming from pytorch frameork.

Optimizer:LBGS
Loss fucntion: CrossEntropy
We found that the loss functions is not really optimized, it takes an ill path at some point of its iterations.


The output of the QNN is 0 and 1. This should match the labels in the test images.

## If we hadn't run out of time, we would:
- Try different optimizers an loss function.
- Measure when does the loss function takes an ill path.
- Increase the number of qbits (pixels)
- Try to encode bigger images in less qbits with NEQR for example.
- For train, more tests, for measurements.
