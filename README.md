# 1D Time-Independent Quantum Mechanics Applet Using Python

This applet simulates the dynamics of a quantum particle inside a reshapable 1D time-independent potential of finite extent. The time evolution of this quantum mechanical particle is given by
$$| \psi(t) \rangle = U(t)| \psi(0) \rangle, $$
where $| \psi \rangle$ is the wavefunction vector ket of the particle and $U(t)$ is the unitary time evolution matrix. The matrix $U(t)$ can be numerically computed using the Cranck-Nicholson method. A derivation of this method is found in Exercise 9.9 of Mark Newman's Computational Physics for the free particle case. It is straightfoward to generalize this to a particle bounded in any energy-preserving potential.

The following modules are used: Numpy for numerical computation, Sympy for symbolic computation, Matplotlib for plotting, and Tkinter for implementing the GUI.

## Instructions:

Make sure you have the latest version of Python with Numpy, Matplotlib, Sympy, and Tkinter installed. The code for this applet can be obtained by cloning this repository or downloading it. Ensure that all source code are in the same directory. Now run `Applet.py` - you should see something like:

Here we see that our wavefunction $\psi(x)$ takes the form of a coherent state of the Simple Harmonic Oscillator potential. Now in the real world, the wavefunction $\psi(x)$ is physically unobservable. However, its probability density $|\psi(x)|^2$ is and you can switch to this view by clicking `View Probability Density`. To measure other observables, click on the `Measure Position`, `Measure Momentum`, and `Measure Energy` buttons. You can also enter a new wavefunction $\psi(x)$ or potential $V(x)$ in the `Enter Wavefunction` or `Enter Potential V(x)` text boxes. To alter the speed of the simulation, move the `Animation Speed slider`. To close the application, press `QUIT`.

If you just want a plain matplotlib animation, you can either run `Animation.py` directly or import it seperately, either through the command line or in a new file. If you import it, make sure you create an instance of the animation object first by running something like `Ani = QM_1D_Animation()`. You measure observables by entering `Ani.measure_energy()`, `Ani.measure_position()`, and `Ani.measure_momentum()`. To switch between a view of the wavefunction itself or its probability density, use the `QM_1D_Animation` methods `display_probability()` or `display_wavefunction()`. To change the wavefunction or potential, use the methods `set_wavefunction(new wavefunction)` and `set_unitary(new_potential)`.

You can also work directly with the class implementation of the wavefunction and the unitary operator, which are `Wavefunction_1D` and `Unitary_Operator_1D` respectively. These are in the file `QM_1D_TI.py`.
