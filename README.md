# membership-functions-fuzzy-systems-
A fuzzy set A in a universe of discourse X is characterized by a membership function μ_A(x) : X → [0, 1], which assigns to each element x ∈ X a degree of membership in A. 
Unlike classical (crisp) sets where membership is strictly binary (0 or 1), fuzzy sets allow partial membership — enabling the modeling of gradual, imprecise, or linguistic concepts such as 'tall', 'hot', or 'fast'. Key terminologies associated with a membership function are:
• Core: The region of the universe where μ_A(x) = 1 (full membership).
• Support: The region where μ_A(x) > 0 (any non-zero membership). 
• Crossover Points: Values of x where μ_A(x) = 0.5.
• Height: The maximum value of μ_A(x) across the universe (≤ 1). The five standard types of membership functions are:
• Triangular MF — defined by three parameters (a, b, c): rises linearly from a to b (peak), then falls to c. Simple and computationally efficient. 
• Trapezoidal MF — defined by four parameters (a, b, c, d): linear rise from a to b, flat top (full membership) from b to c, linear fall from c to d. 
• Gaussian MF — defined by mean (c) and standard deviation (σ): smooth symmetric bell curve. Differentiable, ideal for adaptive neuro-fuzzy systems. 
• Sigmoidal MF — defined by slope (a) and inflection point (c): monotonically increasing (or decreasing). Suitable for open-ended boundary conditions. 
• Generalized Bell MF — defined by width (a), slope (b), center (c): symmetric smooth bell with independently controllable width and slope.

<img width="1021" height="209" alt="image" src="https://github.com/user-attachments/assets/4278536e-f3e3-40ef-88d6-e36c5f3feb1d" />

  Algorithm: 
  Step 1:  Import NumPy for numerical computation and Matplotlib for plotting.
  Step 2:  Define the universe of discourse x as a NumPy linspace array over [0, 10]. 
  Step 3:  Define each membership function as a Python function: Step 3.1: triangular(x, a, b, c)  — with division-by-zero guard using np.where.
  Step 3.2: trapezoidal(x, a, b, c, d)  — with np.minimum and np.maximum clipping. Step 3.3: gaussian(x, c, sigma)  — using np.exp. Step 3.4: sigmoidal(x, a, c)  — using np.exp with slope and center. Step 3.5: bell(x, a, b, c)  — using np.abs with exponent. 
  Step 4:  Compute membership values by calling each function over array x. 
  Step 5:  Create a figure using plt.figure() and plot all five functions. 
  Step 6:  Label x-axis as 'Universe of Discourse', y-axis as 'Degree of Membership μ(x)'. 
  Step 7:  Add title, legend, grid, and set y-axis limits to [-0.05, 1.1]. 
  Step 8:  Save the figure using plt.savefig() and display with plt.show(). 
  Step 9:  Vary parameters (e.g., change σ in Gaussian) and re-run to observe shape changes.
  Step 10: Stop. 
