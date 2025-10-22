### 🧠 Overview

I built this project from scratch to model and fit real-world height distribution data using a **custom Gaussian fitting algorithm** implemented with **gradient descent**.
Rather than relying on existing ML libraries, I wrote the full optimization logic myself: including analytic derivatives, loss calculation, and visualization.

This project demonstrates:

* A deep understanding of **mathematical modeling**
* Proficiency with **NumPy** and **Matplotlib**
* Ability to implement **optimization algorithms manually**
* Skill in visualizing and interpreting data convergence

---

### ⚙️ Project Goal

To **fit a Gaussian model** to empirical data (heights) by minimizing the difference between the model prediction and observed frequencies using **steepest descent optimization**.

---

### 🧩 Core Concepts Implemented

1. **Gaussian Probability Density Function (PDF):**
   [
   f(x;\mu,\sigma) = \frac{1}{\sqrt{2\pi},\sigma} \exp!\left(-\frac{(x-\mu)^2}{2\sigma^2}\right)
   ]

2. **Analytic Derivatives:**
   Computed (\partial f / \partial \mu) and (\partial f / \partial \sigma) by hand to guide optimization.

3. **Chi-Squared Objective Function:**
   [
   \chi^2 = \sum_i (y_i - f(x_i;\mu,\sigma))^2
   ]
   Measures how well the model fits the data.

4. **Steepest Descent Algorithm:**
   Iteratively updates parameters in the direction of the negative gradient:
   [
   [\mu, \sigma] \leftarrow [\mu, \sigma] - \text{learning rate} \times \nabla \chi^2
   ]

5. **Parameter Path Visualization:**
   Tracks the optimization journey in ((\mu, \sigma))-space and visualizes convergence.

---

### 🧮 Technologies Used

* **Python 3.10+**
* **NumPy** for numerical computation
* **Matplotlib** for visualization
* (Optional) custom helper functions for plotting data and contours

---

### 🧠 What I Built (and Why)

| Component             | Description                      | Why It Matters                          |
| --------------------- | -------------------------------- | --------------------------------------- |
| `f(x, μ, σ)`          | Gaussian model function          | Represents the theoretical distribution |
| `dfdmu` / `dfdsig`    | Analytical derivatives           | Enables gradient-based optimization     |
| `steepest_step()`     | Custom gradient descent function | Optimizes parameters manually           |
| Visualization scripts | Plots histogram, contour path    | Shows convergence and model accuracy    |

---

### 📈 Results

* The optimizer successfully converges toward parameters that closely match the empirical distribution.
* Visual plots show the Gaussian curve aligning with the data histogram.
* The contour visualization reveals a smooth and well-behaved loss surface.


Would you like me to make it more **technical (for data science roles)** or more **storytelling (for recruiters / portfolio use)**?
I can tailor the tone and section structure to match either style.
