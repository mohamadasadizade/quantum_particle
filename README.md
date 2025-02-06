# Quantum Particle in a 3D Box

The Schrödinger equation is solved for a particle in a 3D box using the separation of variables method to visualize the probability of finding the particle at different locations inside the box. 
The wave function is separated into three one-dimensional equations for each x, y, and z spatial dimensions.
The code generates a 3D plot where each point in the box has a certain color intensity, corresponding to that location's probability density.

### **Schrödinger Equation**

The time-independent Schrödinger equation is given by for a particle in a 3D box:

$$
\hat{H} \psi(x, y, z) = E \psi(x, y, z)
$$

-  \( $\hat{H}$ \) is the Hamiltonian operator (representing the total energy).
-  \( $\psi(x, y, z)$ \) is the wavefunction of the particle.
-  \( $E$ \) is the energy eigenvalue.


The Hamiltonian is the kinetic energy of the particle:

$$
\hat{H} = -\frac{\hbar^2}{2m} \nabla^2
$$

Where:

- \( $\hbar$ \) is the reduced Planck constant.
- \( $m$ \) is the mass of the particle.
- \( $\nabla^2$ \) is the Laplacian operator (the second spatial derivatives).



The wavefunction is separated into functions for each dimension:

$$
\psi(x, y, z) = \psi_x(x) \psi_y(y) \psi_z(z)
$$

Each of these functions satisfies a one-dimensional particle-in-a-box problem:

$$
-\frac{\hbar^2}{2m} \frac{\partial^2 \psi_x}{\partial x^2} = E_x \psi_x
$$

$$
-\frac{\hbar^2}{2m} \frac{\partial^2 \psi_y}{\partial y^2} = E_y \psi_y
$$

$$
-\frac{\hbar^2}{2m} \frac{\partial^2 \psi_z}{\partial z^2} = E_z \psi_z
$$

Each of these equations has solutions of the form:

$$
\psi_x(x) = \sqrt{\frac{2}{L}} \sin\left(\frac{n_x \pi x}{L}\right)
$$

Where \( $n_x, n_y, n_z$ \) are quantum numbers for each dimension.


### **Energy Eigenvalues**

The energy corresponding to each solution is given by:

$$
E_{n_x, n_y, n_z} = \frac{\hbar^2 \pi^2}{2mL^2} \left( n_x^2 + n_y^2 + n_z^2 \right)
$$

### **Probability Density**

The probability density function is given by the square of the wavefunction:

$$
\rho(x, y, z) = |\psi(x, y, z)|^2
$$

Since the wavefunction is separable, the probability density can be written as:

$$
\rho(x, y, z) = \psi_x(x)^2 \cdot \psi_y(y)^2 \cdot \psi_z(z)^2
$$

This probability density function is used to visualize where the particle is most likely to be found within the box.

### **Quantum Numbers**

The quantum numbers \( $n_x, n_y, n_z$ \) correspond to the energy levels in each dimension. The energy increases as the quantum numbers increase.

- **Ground state**: \( $n_x = 1, n_y = 1, n_z = 1$ \)
- **First excited state**: \( $n_x = 2, n_y = 1, n_z = 1$ \)
- **Second excited state**: \( $n_x = 2, n_y = 2, n_z = 1$ \)
- **Third excited state**: \( $n_x = 3, n_y = 2, n_z = 1$ \)


#### **The code can be executed in Google Colab through the link below.**

https://colab.research.google.com/drive/1a2npem0Ea-pFHGyCMPCDx1AAF1FlpC-i?usp=sharing
