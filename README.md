# Solution of Laplace’s Equation in a Rectangular Tube

## Overview

This project presents the numerical solution and visualization of the electric potential $$\Phi(x,y,z)$$ inside an infinite rectangular tube by solving Laplace’s equation using the method of separation of variables.

The code is implemented in Mathematica and generates an animation that shows how the potential evolves spatially along the longitudinal axis of the tube.

---

## Problem Statement

We consider a metallic tube with rectangular cross-section extending infinitely along the (x)-direction. The boundary conditions are:

* $$\Phi = 0$$ on the walls:

  * (y = 0)
  * (y = a)
  * (z = 0)
  * (z = b)

* At the entrance of the tube ((x = 0)):
  $$\Phi(0,y,z) = \Phi_0(y,z)$$

* As $$x \to \infty$$:
  $$\Phi \to 0$$

The goal is to determine the potential $$\Phi(x,y,z)$$ throughout the interior of the tube.

---

## Theoretical Background

The problem is governed by Laplace’s equation:

$$\nabla^2 \Phi = 0$$

Using separation of variables, the solution can be expressed as a double Fourier series:

$$
\Phi(x,y,z) = \sum_{n=1}^{\infty} \sum_{m=1}^{\infty}
C_{n,m}
,e^{-\pi \sqrt{(n/a)^2+(m/b)^2},x}
\sin\left(\frac{n\pi y}{a}\right)
\sin\left(\frac{m\pi z}{b}\right)
$$

where the coefficients $$C_{n,m}$$ are determined from the boundary condition $$\Phi_0(y,z)$$.

---

## Physical Interpretation

Each term in the series represents a spatial mode that decays exponentially along the (x)-direction.

Higher-frequency modes (large (n) and (m)) decay more rapidly, causing the potential to become progressively smoother as one moves deeper into the tube.


---

## Computational Implementation

The Mathematica code performs:

1. Computation of Fourier coefficients via numerical integration
2. Construction of the truncated series solution
3. Visualization using:

   * 3D surface plots of the potential
   * Heat maps of the transverse cross-section
4. Generation of an animation as a function of (x)
5. Automatic export of the result as a video file

---

## Repository Structure

* `Code.nb`
  Mathematica notebook containing the full implementation

* `Animation.mp4`
  Generated animation of the potential

---

## Requirements

* Wolfram Mathematica (recent version recommended)
* Sufficient computational resources for numerical integration

---

## Usage

1. Open the `.nb` file in Mathematica
2. Evaluate all cells
3. Wait for the frame generation process to complete
4. Visualize the animation
5. Check the automatically exported output file

---

## Results

The main result is an animation showing the evolution of the electric potential inside the tube.

It illustrates how the initial structure imposed at the entrance gradually attenuates, highlighting the role of dominant modes in the solution.

---

## Author

Alejandro García López

---

## License

This project is intended for academic and educational use.

