#  About:
This script is a quick non-general implementation of the Implicit Runge-Kutta method of fifth order (RADAU5).

It solves the differential equation dy/dt= f(y, t) for the given example Hamiltonian of the form:


```math
\begin{align}
  \MC{H}(t) &= \hbar\big(\omega_0\,\sigma^z + \omega_1\left(\cos(\omega t)\,\sigma^x + \sin(\omega t)\,\sigma^y\right)\big) \\
  &= \hbar\begin{pmatrix} \omega_0 & \omega_1 e^{-\iu \omega t} \\ \omega_1 e^{\iu \omega t} & -\omega_0 \end{pmatrix} \quad 
\label{equation: zeeman.hamiltonian}
\end{align}
```

With the frequencies defined as $`\hbar\omega_0 = \MuB B_0`$ and $`\hbar\omega_1 = \MuB B_1`$. 

The initial state vector is [Mx, My, Mz] = [0 0 -1].

This Hamiltonian has an exact solution, which the script plots against the numerically obtained one.


# Method references:
[1] Butcher, J.C.The numerical analysis of ordinary differential equations: Runge-Kutta andgeneral linear methods(Wiley-Interscience, 1987).

# Input:
Change the input parameters from the line:
`w0, w1, w, integration_time, N = 10.0, 5.0, 15.0, 1, 100`

# Run:

`python radau5.py`

