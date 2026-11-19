# AI INSTRUCTIONS & GOAL
- **Goal:** Customize this engineering portfolio template with my personal projects, academics, and skills.
- **Rules for Copilot:** 
  1. Keep all existing HTML structure, CSS classes, and JS scripts intact.
  2. Match the exact image paths listed below. Do not invent file names.
  3. Keep the tone professional, technical, and concise.

---

# PERSONAL INFO (For index.html)
- **Full Name:** Antoine LEVRAT
- **Headline/Title:** Simulation Engineer | Modeling Specialist
- **Short Bio:** do it yourself
- **Email:** [antoinelevrat78@gmail.com]
- **LinkedIn:** [www.linkedin.com/in/antoine-levrat-151843265]
- **GitHub:** [https://github.com/antoinelevrat78-cyber]
- **Profile Photo:** `assets/Antoine_LEVRAT_Headshot.jpeg`
- **Resume/CV PDF:** `assets/Antoine_LEVRAT_CV.pdf`

---

# ACADEMICS & SKILLS (For index.html)
- **Degree:** Master 2 in Applied Mathematics: Analysis, Modeling, and Simulation (AMS) — Université Paris-Saclay / UVSQ (2026)
- **Relevant Coursework:** [Finite Element Method, Finite Volume Method, Boundary Element Method, Moment Method, POD Galerkin, Hybrid Method...]
- **Programming & tools:** Python, C++, MATLAB, SolidWorks, Fusion 360
- **Main Courses:** 
 -Parallel Scientific Computing, 
 -PDE-Constrained Optimization, 
 -Variational Methods for Non-Coercive Problems , 
 -Derivative-Free Optimization, 
 -Moment Methods Derived from a Kinetic Equation, 
 -From Integral Equations to Neural Networks, 
 -Hybrid Methods for High-Frequency Diffraction, 
 -Mesh Generation and Adaptation for Scientific Computing, 
 -Reduced Basis Methods for Solving Parameter-Dependent PDEs.

---

# PROJECT 0: [Name of internship] (For Project_0.html)
- **Subtitle/Role:** [Internship]
- **Date:** [e.g., Fall 2025]
- **Card Thumbnail (for index.html):** `Project_1/thumb.jpg`
- **Tools Used:** []
- **Problem/Goal:** []
- **What I Did (Bullet points for the page):**
  - 
  - 
  - 
- **Gallery Images & Captions:**
  - `Project_1/` — 
  - `Project_1/` — 
  - `Project_1/` — 

---

# PROJECT 1: Heat Distribution Optimization: Control Theory on the Heat Equation (For Project_1.html)
- **Subtitle/Role:** Personal Project | PDE-Constrained Optimization
- **Date:** February 2026
- **Card Thumbnail (for index.html):** Nothing here do not fill
- **Tools Used:** Python, FEniCS, MPI, Matplotlib, ParaView
- **Problem/Goal:** Determine an optimal heating distribution $u$ that minimizes the deviation from a target temperature $y_d$ under physical constraints governed by steady-state Poisson, advection-diffusion, and time-dependent heat PDEs.
- **What I Did (Bullet points for the page):**
  - Formulated and solved the PDE-constrained optimization problem using the adjoint state method and a projected gradient algorithm with Armijo backtracking line search.
  - Accelerated solver convergence by implementing the Barzilai-Borwein (quasi-Newton secant) step-size strategy and resolving FEniCS symbolic expression tree crashes via solution interpolation.
  - Extended the mathematical formulation and backward Euler time-stepping solver to handle advection-diffusion and transient (time-dependent) thermal models.
  - Conducted mesh refinement validation, strong/weak MPI parallel scaling benchmarks, and 3D/temporal field visualizations in ParaView and Matplotlib.
- **Results:**
  - Reduced convergence iterations from ~800 (standard Armijo) to fewer than 5 iterations using the Barzilai-Borwein method, cutting computation time on a $32^2$ mesh from ~28.55s to ~0.43s.
  - Verified numerical accuracy across mesh refinements (from $32^2$ to $512^2$), achieving an $L^2$ error reduction from $1.02 \times 10^{-2}$ to $4.04 \times 10^{-5}$ in alignment with the theoretical $h^2$ convergence slope.
  - Benchmarked MPI parallel execution, reaching a peak strong-scaling speedup of ~1.45x on 2 processes.
- **Gallery Images & Captions:**
  - this i will do do not fill

---

# PROJECT 2: Extended Physics-Informed Neural Networks (XPINN) for Fluid Dynamics (For Project_2.html)
- **Subtitle/Role:** Personnal Project (Neural Networks and Data Assimilation)
- **Date:** May 2026
- **Card Thumbnail (for index.html):** 
- **Tools Used:** Python, FEniCS, PyTorch/Deep Learning Libraries, GPU Acceleration (CUDA)
- **Problem/Goal:** Standard Physics-Informed Neural Networks (PINNs) fail to converge when modeling viscous fluid flow across sharp, discontinuous interfaces in porous media (governed by the Brinkman equation with a 9-order-of-magnitude permeability jump). The goal was to develop a ground-up Extended PINN (XPINN) architecture capable of accurately reconstructing velocity and pressure fields across these complex multi-domain transitions.
- **What I Did (Bullet points for the page):**
  - Built a coupled Finite Element Method (FEM) reference solver in Python using FEniCS on a $128^2$ mesh (2.795s solve time) to simulate steady-state incompressible Brinkman flow across a sharp permeability transition ($10^{-6}$ to $10^3\text{ m}^2$).
  - Developed and benchmarked progressive neural solvers (1D verification, 2D constant-permeability PINN, and 2D discontinuous PINN), migrating execution to a GPU to reduce memory footprint from 40% CPU usage down to 2% GPU memory.
  - Engineered a hybrid optimization strategy combining Adam for rapid initial loss reduction with L-BFGS for high-precision convergence, alongside pressure normalization and dynamic loss weighting to enforce strict boundary conditions.
  - Implemented a custom multi-domain XPINN architecture splitting the geometry into two non-overlapping sub-networks coupled via interface average solution continuity and PDE residual continuity terms.
- **Results:** Successfully overcame local optima caused by the 9-order-of-magnitude permeability jump where standard PINNs failed, achieving stable loss convergence and accurate velocity and pressure field reconstruction across the porous-free flow interface using sparse FEM reference data.
- **Gallery Images & Captions:**
  -

---

# PROJECT 3: High-Performance Parallel PDE & FEM Solver (For Project_3.html)
- **Subtitle/Role:** Academic Team Project
- **Date:** 2025
- **Card Thumbnail (for index.html):** 
- **Tools Used:** C++, MPI (OpenMPI/MPICH), HPC Cluster (Cholesky), Finite Difference & Finite Element Methods (FDM/FEM)
- **Problem/Goal:** Accelerating the numerical resolution of large-scale 2D and 3D Partial Differential Equations (such as the Laplace and heat equations) by distributing computational workloads and memory across multi-core processors and HPC clusters.
- **What I Did (Bullet points for the page):**
  - Developed sequential and parallel 2D/3D Finite Difference solvers in C++ using Jacobi and Red-Black Gauss-Seidel iterative methods, verifying spatial second-order convergence ($O(h^2)$) against analytical solutions.
  - Optimized inter-process communication using non-blocking MPI routines (`MPI_Isend`, `MPI_Irecv`, `MPI_Waitall`) to overlap computation with data exchange, flattening multi-dimensional grids into 1D contiguous vectors.
  - Built a custom 2D and 3D meshing tool paired with a Finite Element Method (FEM) solver implementing domain decomposition methods (both with and without overlap) to partition unstructured meshes across multiple CPUs.
  - Conducted strong and weak scaling benchmarks up to 20 processors on both local multi-core architectures and the Cholesky HPC cluster to evaluate speedup, parallel efficiency, and hardware bottlenecks.
- **Results:** Achieved over 70% weak scaling efficiency at 8 cores on the Cholesky HPC cluster (outperforming local hardware benchmarks by >20%) and reached an error tolerance below $10^{-5}$ with Red-Black Gauss-Seidel in 37% fewer iterations than standard Jacobi.
- **Gallery Images & Captions:**
  -

---

# PROJECT 4.1: Adaptive 2D Delaunay Meshing & Image Compression (For Project_4.html)
- **Subtitle/Role:** Academic Project (Scientific Computing - MS14)
- **Date:** March - April 2026
- **Card Thumbnail (for index.html):** 
- **Tools Used:** C, VIZIR4, Computational Geometry, Hash Tables, Delaunay Triangulation
- **Problem/Goal:** Develop high-performance mesh connectivity data structures and a 2D Delaunay triangulation kernel from scratch, then apply adaptive meshing to compress grayscale images while preserving high visual fidelity in high-contrast regions.
- **What I Did (Bullet points for the page):**
  - Implemented geometric mesh quality metrics ($Q_1$ and $Q_2$) and replaced a naive $O(N^2)$ neighbor-search algorithm with a custom hash table structure, reducing connectivity and boundary-edge detection complexity to quasi-linear time $O(N)$.
  - Benchmarked multiple hashing key strategies ($i+j$, $\min(i,j)$, and $i+j \times 1000$) across complex aerospace geometries (`naca`, `ls89`, `hlcrm` up to 355,000 triangles), minimizing average hash collisions to ~1.94.
  - Built a 2D Delaunay insertion kernel using cavity computation (Bowyer-Watson approach) and signed-area point localization, outperforming an initial edge-flipping triangulation kernel in both triangle regularity ($Q_1 < 3$) and CPU execution time (~2s vs. 11s for 3,000 points).
  - Applied the Delaunay kernel to grayscale image compression using barycentric coordinate interpolation and an iterative Peak Signal-to-Noise Ratio (PSNR) error-driven refinement loop to dynamically densify the mesh around sharp features.
- **Results:** 
  - Achieved superior image reconstruction quality using PSNR-guided adaptive meshing with 1,000 points compared to random Delaunay point insertion with 5,000 points (5x fewer vertices required to capture fine details like eyes, mouth, and hands), reaching ~28 dB PSNR on benchmark tests.
- **Gallery Images & Captions:**
  -

---

# PROJECT 4.2: PDE Constrained Optimization — Master Course Lecture Notes (For Project_4.html)
- **Subtitle/Role:** Academic Publication & Co-Author (with Prof. Grégoire Allaire, École Polytechnique)
- **Date:** August 2026
- **Card Thumbnail (for index.html):**
- **Tools Used:** LaTeX, BibTeX, Mathematical Typesetting, HAL Open Science
- **Problem/Goal:** Prof. Grégoire Allaire's M2 course on PDE Constrained Optimization at Institut Polytechnique de Paris and Sorbonne Université existed solely as handwritten blackboard notes, lacking a structured digital reference. My goal was to transcribe, formalize, and typeset the complete theoretical and numerical curriculum into a rigorous, publication-ready LaTeX document.
- **What I Did (Bullet points for the page):**
  - Transcribed and formalized 77 pages of advanced mathematical lectures covering convex analysis, calculus of variations, adjoint-state methods, and numerical optimization algorithms (Projected Gradient, Newton, Uzawa, Optimality Criteria).
  - Typeset complex mathematical proofs, variational formulations, and multi-physics applications across linear/non-linear elliptic, parabolic, and hyperbolic PDEs, as well as optimal control and data assimilation.
  - Collaborated directly with Prof. Grégoire Allaire through iterative proofreading and technical revisions to ensure mathematical rigor and clarity.
  - Published the finalized manuscript on the HAL Open Science archive (`hal-05719433`), making the resource publicly accessible to graduate students and researchers.
- **Results:** Published a 77-page open-access academic reference on HAL (`hal-05719433`) for the M2 Master program at Institut Polytechnique de Paris and Sorbonne Université.
- **Gallery Images & Captions:**
  -

---

# PROJECT 4.3: 2D Helmholtz Boundary Element Method (BEM) Solver (For Project_4.html)
- **Subtitle/Role:** Academic Team Project
- **Date:** Fall 2025
- **Card Thumbnail (for index.html):**
- **Tools Used:** Python, NumPy, SciPy, Matplotlib, VIZIR4 (INRIA)
- **Problem/Goal:** Solving 2D wave diffraction around obstacles via the Boundary Element Method generates dense linear systems with high memory and $O(N^3)$ computational costs. The goal was to develop a fast BEM solver accelerated by Hierarchical Matrices (H-matrices) and Adaptive Cross Approximation (ACA) to achieve quasi-linear $O(N \log N)$ complexity.
- **What I Did (Bullet points for the page):**
  - Derived the analytical trace solution and built a 2D BEM solver using Galerkin discretization, Gauss-Legendre quadrature, and semi-analytical integration to handle Green's function diagonal singularities.
  - Benchmarked low-rank matrix compression methods (Truncated SVD, Complete ACA, and Partial ACA), selecting Partial ACA for its superior $O(k(m+n))$ factorization speed (0.005s vs. 0.252s for SVD).
  - Implemented spatial binary trees (geometric and balanced partitioning) with an admissibility criterion coupled to a GMRES iterative solver, reducing assembly and solve complexity from $O(N^2)/O(N^3)$ to $O(N \log N)$.
  - Extended the solver beyond circular disks to complex 2D geometries (square, ellipse, boomerang, star, and non-convex shapes) and visualized 2D diffracted wave fields across 20,000-triangle meshes in VIZIR4.
- **Results:** Achieved a memory compression ratio down to 12.43% (at $N=1600$) and over 10x faster matrix assembly compared to dense solvers while maintaining high numerical accuracy against analytical solutions.
- **Gallery Images & Captions:**
  -

---

# PROJECT 4.4: Periodic Homogenization via Finite Element Method (FEM) (For Project_4.html)
- **Subtitle/Role:** Academic Project
- **Date:** 2025
- **Card Thumbnail (for index.html):** 
- **Tools Used:** Python, NumPy, SciPy, Matplotlib, Finite Element Method (FEM)
- **Problem/Goal:** Implement a 2D Finite Element solver from scratch to approximate partial differential equations with rapidly oscillating periodic coefficients, comparing the exact micro-scale solution against the homogenized macro-scale model.
- **What I Did (Bullet points for the page):**
  - Developed a 2D P1 Finite Element solver in Python supporting Dirichlet, Neumann, and periodic boundary conditions via projection matrices ($P_{per}$).
  - Verified solver convergence against analytical solutions, achieving the theoretical order 2 convergence rate in $L^2$ norm.
  - Computed cell correctors ($w_i$) on the unit periodicity cell to derive the homogenized effective diffusion tensor ($A^{eff}$).
  - Simulated and compared the oscillating solution ($u^\epsilon$) against the homogenized macro-scale solution ($u^0$) across varying $\epsilon$ scales in $L^2$ and $H^1$ norms.
- **Results:** Validated the numerical effective tensor ($A^{eff}_{11} \approx 1.7765$) against the theoretical value ($\sqrt{3} \approx 1.7321$) and confirmed the asymptotic convergence of the homogenized model as $\epsilon \to 0$.
- **Gallery Images & Captions:**
  -

---

# PROJECT 4.5: Numerical Study of Demagnetizing Energy & iLLG Simulation (For Project_4.html)
- **Subtitle/Role:** Personnal Independent Research Project
- **Date:** Summer 2025
- **Card Thumbnail (for index.html):**
- **Tools Used:** Python (NumPy, SciPy, Matplotlib)
- **Problem/Goal:** Numerically compute the demagnetizing (stray field) energy in ferromagnetic materials using 4D spherical harmonics and develop a finite-difference solver to simulate ultrafast inertial magnetization dynamics via the inertial Landau-Lifshitz-Gilbert (iLLG) equation.
- **What I Did (Bullet points for the page):**
  - Implemented the Arrar & Boulmezaoud analytical-numerical method using 4D spherical harmonics, iterative Chebyshev polynomials, and Gauss-Legendre quadrature to compute stray field energy.
  - Validated the demagnetizing energy solver on a unit sphere ($R=1$), matching literature benchmark values to 6 decimal places (0.0769663 vs. 0.07696625 reference).
  - Formulated and coded a 1D semi-implicit finite-difference scheme with Neumann boundary conditions and matrix inversion to simulate the inertial Landau-Lifshitz-Gilbert (iLLG) equation.
  - Analyzed numerical stability, discretization sensitivity, and magnetization norm preservation by benchmarking simulated mean magnetization trajectories against theoretical damped oscillations.
- **Results:** Successfully validated the demagnetizing energy calculation method against published benchmarks and built a functional prototype solver for the iLLG equation, identifying key discretization and stability constraints for future implicit schemes.
- **Gallery Images & Captions:**
  -

---

# PROJECT 4.6: Numerical Approximation of Wave Diffraction via Geometrical Optics (For Project_4.html)
- **Subtitle/Role:** Academic Team Project (Pair Programming)
- **Date:** 2026
- **Card Thumbnail (for index.html):**
- **Tools Used:** Python (curves, pyff), FreeFem++, ParaView
- **Problem/Goal:** Approximate high-frequency 2D plane wave diffraction around a convex obstacle using the Geometrical Optics method, and validate its accuracy against a high-order Finite Element Method (FEM) reference solution.
- **What I Did (Bullet points for the page):**
  - Implemented a ray-tracing solver in Python (`Geometric_optic.py`) to compute reflected rays, solving the eikonal equation for phase $S$ and the transport equation via characteristic tubes for amplitude $a_0$.
  - Built a 2D reference solver in FreeFem++ (`fem_with_PML.edp`) utilizing a Perfectly Matched Layer (PML) to truncate the unbounded domain and P4 finite elements to minimize numerical pollution at high wavenumbers.
  - Bridged Python geometric data to FreeFem++ using the `pyff` module and visualized wave fields, characteristic rays, and absolute error distributions in ParaView.
- **Results:**
  - Achieved strong visual and numerical agreement in the illuminated zone, reducing the relative $L^2$ error from 5.17% at $k=10$ down to 3.98% at $k=20$, matching theoretical $O(k^{-1})$ asymptotic convergence.
  - Demonstrated the physical limitations of standard Geometrical Optics in the shadow zone (due to missing diffracted rays and Sommerfeld radiation condition violations at the shadow-light boundary) as well as FEM numerical pollution limits at $k=30$ (4.82% error) under memory constraints.
- **Gallery Images & Captions:**
  -

---

# PROJECT 4.7: Proof & Visualization of Sard's Theorem (For Project_4.html)
- **Subtitle/Role:** Academic Team Project (L3 Mathematics - Semester 6)
- **Date:** Spring 2025
- **Card Thumbnail (for index.html):**
- **Tools Used:** LaTeX, GeoGebra, Differential Calculus, Measure Theory
- **Problem/Goal:** Study, prove, and illustrate Sard's Theorem in differential topology, which establishes that the set of critical values of a smooth function between Euclidean spaces has a Lebesgue measure of zero.
- **What I Did (Bullet points for the page):**
  - Constructed a complete, rigorous mathematical proof of Sard's Theorem by induction on dimension $m$, covering all critical point subsets ($m < n$, $C \setminus C_1$, $C_i \setminus C_{i+1}$, and $C_k$ for $k > \frac{m}{n} - 1$).
  - Applied foundational analytical tools including Taylor's theorem with integral remainder, Fubini's theorem, the Implicit Function Theorem, and the Local Inversion Theorem.
  - Analyzed theoretical base cases ($m=n=1$ and $m=2, n=1$) and modeled practical geometric examples—such as $f(x)=(x^2, x+1)$ and $g(x)=\frac{\sin(x)}{x}$—using 2D and 3D plots to visualize how infinite critical points still yield zero-measure image sets.
  - Authored and typeset the complete 8-page technical report in LaTeX under the supervision of Prof. Luc Robbiano, referencing Milnor's *Topology from the Differentiable Viewpoint*.
- **Gallery Images & Captions:**
  -

---

# PROJECT 4.8: Hyperbolic Quadrature Method of Moments (HyQMOM) — Literature Synthesis (For Project_4.html)
- **Subtitle/Role:** Academic Literature Synthesis | Applied Mathematics
- **Date:** January 2026
- **Card Thumbnail (for index.html):**
- **Tools Used:** LaTeX, Mathematical Analysis, Orthogonal Polynomials
- **Problem/Goal:** Making the 2022 Fox & Laurent research paper on arbitrary-order ($2n+1$) moment closures for 1-D kinetic equations accessible by distilling complex proofs into a structured, clear mathematical guide.
- **What I Did (Bullet points for the page):**
  - Synthesized the core mathematical framework of the Hyperbolic Quadrature Method of Moments (HyQMOM), contrasting arbitrary-order closures against earlier 4th-order limitations.
  - Broken down the change-of-variable proofs using centered and standardized moments to demonstrate translation and scaling invariance.
  - Clarified the characteristic polynomial factorization ($P_{2n+1}(X) = Q_n(X)R_{n+1}(X)$) and summarized the global hyperbolicity proof via orthogonal polynomial root separation and the Christoffel-Darboux formula.
  - Documented the simplified direct closure algorithm (using the Reverse Chebyshev method) that operates directly on raw moments $M_{2n}$ without intermediate standardization steps.
- **Gallery Images & Captions:**
  -

