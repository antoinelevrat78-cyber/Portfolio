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


# Work Experience (For index.html)
- **Internship:** Framatome 6 months april to september 2026 | thermo mecanical ingeneer
  - **Main achivements:**
    - Developed a modeling approach to simulate concentration evolutions in
    coupled media using Finite Element (FEM) and Finite Volume (FVM)
    methods.
    - Optimized and accelerated core simulation codes, implementing
    high-order integration schemes, mesh refinement, adaptive time-stepping,
    to drastically reduce computation time.
    - Designed innovative numerical solutions to overcome convergence issues
    and improve solver stability.
    - Verified numerical models

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

# PROJECT 0: Coupled Media Concentration Transport & Solver Acceleration (For Project_0.html)
- **Subtitle/Role:** R&D Numerical Simulation Intern at Framatome | Multiphysics & Scientific Computing
- **Date:** April 2026 – September 2026
- **Card Thumbnail (for index.html):** `Project_0/Pictures/Logo_framatome.png`
- Due to the fact that this project was confidential all pictures etc are ai generated in order to give some visuals. put one sentence to say this in the begining of the project page
- **Tools Used:** Python, Finite Element Method (FEM), Finite Volume Method (FVM), ParaView, Salomé
- **Problem/Goal:** Accurately simulate transient species concentration evolutions across coupled multiphysics media while overcoming severe solver convergence bottlenecks and high computational costs inherent to multi-scale interface coupling.
- **What I Did (Bullet points for the page):**
  - Developed a hybrid numerical modeling framework coupling Finite Element (FEM) and Finite Volume (FVM) discretizations to capture species transport and continuity across heterogeneous media interfaces.
  - Accelerated core simulation routines by implementing high-order time/space integration schemes, localized mesh refinement, and adaptive time-stepping strategies.
  - Engineered custom numerical stabilization and preconditioning techniques to resolve non-linear convergence stalls at steep concentration gradients and interface boundaries.
  - Benchmarked and validated simulation outputs against experimental datasets to ensure physical fidelity, mass conservation, and predictive accuracy.
- **Results:**
  - Drastically reduced overall simulation wall-clock execution time while preserving high-order spatial and temporal accuracy across complex coupled geometries.
  - Eliminated solver divergence issues on stiff, coupled test cases, ensuring robust convergence across varying physical regimes.
  - Achieved close quantitative agreement between numerical predictions and real-world experimental measurements, validating the framework for engineering applications.
- **Gallery Images & Captions:**
  - `Project_0/Pictures/fig_1_ai_generated_solid_solid_radionuclide_diffusion_simulation.jpg` — 
  - `Project_0/Pictures/fig_2_ai_generated_adaptative_mesh_visualisation.jpg` —  

---

# PROJECT 1: Heat Distribution Optimization: Control Theory on the Heat Equation (For Project_1.html)
- **Subtitle/Role:** Personal Project | PDE-Constrained Optimization
- **Date:** February 2026
- **Card Thumbnail (for index.html):** `Project_1/Pictures/constrained_3d_heat_distribution_plot.png`
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
  - `Project_1/Pictures/constrained_3d_heat_distribution_plot.png`: 3D heat distribution obtained under admissible control bounds ($0 \le u(x) \le 6$).
  - `Project_1/Pictures/computation_time_armijo_vs_barzilai_borwein_log_plot.png`: Computation time comparison across mesh resolutions between standard Armijo backtracking and the Barzilai-Borwein method.
  - `Project_1/Pictures/l2_error_mesh_refinement_convergence_h2_slope.png`: $L^2$ error decay across mesh refinements validating alignment with the theoretical $h^2$ convergence slope.
  - `Project_1/Pictures/advection_diffusion_converged_heatmap_iter30.png`: ParaView thermal distribution visualization at iteration 30 for the extended PDE model with an advection term.
- **pdf of the project:**
  - `Project_1/2026_Perso_Project_Heat_Optimization.pdf`

---

# PROJECT 2: Extended Physics-Informed Neural Networks (XPINN) for Fluid Dynamics (For Project_2.html)
- **Subtitle/Role:** Personnal Project (Neural Networks and Data Assimilation)
- **Date:** May 2026
- **Card Thumbnail (for index.html):** `Project_2/Pictures/fig_3_xpinn_final_velocity_pressure_fields.png`
- **Tools Used:** Python, FEniCS, PyTorch/Deep Learning Libraries, GPU Acceleration (CUDA)
- **Problem/Goal:** Standard Physics-Informed Neural Networks (PINNs) fail to converge when modeling viscous fluid flow across sharp, discontinuous interfaces in porous media (governed by the Brinkman equation with a 9-order-of-magnitude permeability jump). The goal was to develop a ground-up Extended PINN (XPINN) architecture capable of accurately reconstructing velocity and pressure fields across these complex multi-domain transitions.
- **What I Did (Bullet points for the page):**
  - Built a coupled Finite Element Method (FEM) reference solver in Python using FEniCS on a $128^2$ mesh (2.795s solve time) to simulate steady-state incompressible Brinkman flow across a sharp permeability transition ($10^{-6}$ to $10^3\text{ m}^2$).
  - Developed and benchmarked progressive neural solvers (1D verification, 2D constant-permeability PINN, and 2D discontinuous PINN), migrating execution to a GPU to reduce memory footprint from 40% CPU usage down to 2% GPU memory.
  - Engineered a hybrid optimization strategy combining Adam for rapid initial loss reduction with L-BFGS for high-precision convergence, alongside pressure normalization and dynamic loss weighting to enforce strict boundary conditions.
  - Implemented a custom multi-domain XPINN architecture splitting the geometry into two non-overlapping sub-networks coupled via interface average solution continuity and PDE residual continuity terms.
- **Results:** Successfully overcame local optima caused by the 9-order-of-magnitude permeability jump where standard PINNs failed, achieving stable loss convergence and accurate velocity and pressure field reconstruction across the porous-free flow interface using sparse FEM reference data.
- **Gallery Images & Captions:**
  - `Project_2/Pictures/fig_1_fem_ground_truth_velocity_pressure.png`: Ground-truth velocity ($u$) and pressure ($p$) fields computed via the FEniCS FEM solver across the porous media interface at $x=0.5$.
  - `Project_2/Pictures/fig_2_standard_pinn_convergence_failure.png`: Standard single-domain PINN failure after 10,000 Adam iterations, falling into local optima due to the 9-order-of-magnitude permeability jump.
  - `Project_2/Pictures/fig_3_xpinn_final_velocity_pressure_fields.png`: Custom multi-domain XPINN reconstruction of velocity and normalized pressure fields across the discontinuous permeability interface using sparse FEM reference points.
  - `Project_2/Pictures/fig_4_xpinn_multidomain_loss_convergence.png`: Training loss evolution over 10,000 Adam epochs showing stable convergence across both sub-networks (Loss M1, Loss M2) and the total coupled loss.
- **pdf of the project:**
  - `Project_2/Project_PINN_Doc.pdf`

---

# PROJECT 3: High-Performance Parallel PDE & FEM Solver (For Project_3.html)
- **Subtitle/Role:** Academic Team Project
- **Date:** 2025
- **Card Thumbnail (for index.html):** `Project_3/Pictures/fig_5_fem_2d_mesh_domain_decomposition.png`
- **Tools Used:** C++, MPI (OpenMPI/MPICH), HPC Cluster (Cholesky), Finite Difference & Finite Element Methods (FDM/FEM)
- **Problem/Goal:** Accelerating the numerical resolution of large-scale 2D and 3D Partial Differential Equations (such as the Laplace and heat equations) by distributing computational workloads and memory across multi-core processors and HPC clusters.
- **What I Did (Bullet points for the page):**
  - Developed sequential and parallel 2D/3D Finite Difference solvers in C++ using Jacobi and Red-Black Gauss-Seidel iterative methods, verifying spatial second-order convergence ($O(h^2)$) against analytical solutions.
  - Optimized inter-process communication using non-blocking MPI routines (`MPI_Isend`, `MPI_Irecv`, `MPI_Waitall`) to overlap computation with data exchange, flattening multi-dimensional grids into 1D contiguous vectors.
  - Built a custom 2D and 3D meshing tool paired with a Finite Element Method (FEM) solver implementing domain decomposition methods (both with and without overlap) to partition unstructured meshes across multiple CPUs.
  - Conducted strong and weak scaling benchmarks up to 20 processors on both local multi-core architectures and the Cholesky HPC cluster to evaluate speedup, parallel efficiency, and hardware bottlenecks.
- **Results:** Achieved over 70% weak scaling efficiency at 8 cores on the Cholesky HPC cluster (outperforming local hardware benchmarks by >20%) and reached an error tolerance below $10^{-5}$ with Red-Black Gauss-Seidel in 37% fewer iterations than standard Jacobi.
- **Gallery Images & Captions:**
  - `Project_3/Pictures/fig_1_laplace_2d_3d_surface_solution.png` | 3D surface visualization of the numerical solution for the 2D Laplace equation on a $128 \times 128$ regular grid.
  - `Project_3/Pictures/fig_2_jacobi_vs_gauss_seidel_convergence.png` | Iterative convergence comparison (max error vs. iterations) demonstrating the superior speed of Red-Black Gauss-Seidel over Jacobi.
  - `Project_3/Pictures/fig_3_hpc_cholesky_strong_weak_scaling.png` | Strong scaling (speedup) and weak scaling (efficiency) benchmarks measured up to 20 processors on the Cholesky HPC cluster.
  - `Project_3/Pictures/fig_4_3d_jacobi_execution_time_vs_mesh_size.png` | Computational cost scaling: execution time growth relative to the total number of grid points in the parallelized 3D solver.
  - `Project_3/Pictures/fig_5_fem_2d_mesh_domain_decomposition.png` | Unstructured 2D triangular mesh partitioned into 4 subdomains for parallel Finite Element Method (FEM) resolution.
- **pdf of the project:**
  - `Project_3/Report_Parallel_Calculus.pdf`

---

# PROJECT 4.1: Adaptive 2D Delaunay Meshing & Image Compression (For Project_4.html)
- **Subtitle/Role:** Academic Project (Scientific Computing - MS14)
- **Date:** March - April 2026
- **Card Thumbnail (for index.html):** `Project_4/Project_1/Pictures/fig_5_adaptive_psnr_delaunay_compression_1000_points.png`
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
  - `Project_4/Project_1/Pictures/fig_1_hash_table_vs_naive_cpu_complexity_benchmark.png` — CPU execution time comparison on a log-log scale showing quasi-linear $O(N)$ scaling with the custom hash table versus quadratic $O(N^2)$ scaling for naive neighbor search across meshes up to 355,000 triangles.
  - `Project_4/Project_1/Pictures/fig_2_mesh_quality_comparison_before_after_edge_flip.png` — Side-by-side comparison of geometric triangle quality ($Q_1$, log scale) on a $[0,1]^2$ domain with 50 random points before (left) and after (right) applying convex edge-flipping optimization.
  - `Project_4/Project_1/Pictures/fig_3_delaunay_kernel_mesh_quality_q1.png` — Resulting triangulation quality ($Q_1$, log scale) generated by the 2D Bowyer-Watson Delaunay insertion kernel on the same 50-point test domain, achieving high element regularity ($Q_1 < 3$) across the interior.
  - `Project_4/Project_1/Pictures/fig_4_image_compression_random_delaunay_5000_points.png` — Baseline grayscale image reconstruction using random Delaunay point insertion with $N = 5,000$ vertices, serving as the reference benchmark (~28 dB PSNR).
  - `Project_4/Project_1/Pictures/fig_5_adaptive_psnr_delaunay_compression_1000_points.png` — Final adaptive image compression using PSNR error-driven point insertion with only $N = 1,000$ vertices, dynamically densifying the mesh along high-contrast features (eyes, mouth, hands) to outperform the 5,000-point random baseline.
- **pdf of the project:**
  - `Project_4/Project_1/Report_Adaptative_Meshing_Method.pdf`

---

# PROJECT 4.2: PDE Constrained Optimization — Master Course Lecture Notes (For Project_4.html)
- **Subtitle/Role:** Academic Publication & Co-Author (with Prof. Grégoire Allaire, École Polytechnique)
- **Date:** August 2026
- **Card Thumbnail (for index.html):** `Project_4/Project_2/Pictures/fig_1_hal_publication_title_page.png`
- **Tools Used:** LaTeX, BibTeX, Mathematical Typesetting, HAL Open Science
- **Problem/Goal:** Prof. Grégoire Allaire's M2 course on PDE Constrained Optimization at Institut Polytechnique de Paris and Sorbonne Université existed solely as handwritten blackboard notes, lacking a structured digital reference. My goal was to transcribe, formalize, and typeset the complete theoretical and numerical curriculum into a rigorous, publication-ready LaTeX document.
- **What I Did (Bullet points for the page):**
  - Transcribed and formalized 77 pages of advanced mathematical lectures covering convex analysis, calculus of variations, adjoint-state methods, and numerical optimization algorithms (Projected Gradient, Newton, Uzawa, Optimality Criteria).
  - Typeset complex mathematical proofs, variational formulations, and multi-physics applications across linear/non-linear elliptic, parabolic, and hyperbolic PDEs, as well as optimal control and data assimilation.
  - Collaborated directly with Prof. Grégoire Allaire through iterative proofreading and technical revisions to ensure mathematical rigor and clarity.
  - Published the finalized manuscript on the HAL Open Science archive (`hal-05719433`), making the resource publicly accessible to graduate students and researchers.
- **Results:** Published a 77-page open-access academic reference on HAL (`hal-05719433`) for the M2 Master program at Institut Polytechnique de Paris and Sorbonne Université.
- **Gallery Images & Captions:**
  - `Project_4/Project_2/Pictures/fig_1_hal_publication_title_page.png` — Official HAL Open Science publication cover and title page (`hal-05719433`), 
  - `Project_4/Project_2/Pictures/fig_2_authors_title_page.png` — co-authored with Prof. Grégoire Allaire at Institut Polytechnique de Paris.
  - `Project_4/Project_2/Pictures/fig_3_latex_mathematical_typesetting_sample.png` — Excerpt of the typeset LaTeX manuscript showcasing variational formulations, adjoint-state derivations, and optimization algorithms.
- **pdf of the project:**
  - `Project_4/Project_2/pdeoptim.pdf`

---

# PROJECT 4.3: 2D Helmholtz Boundary Element Method (BEM) Solver (For Project_4.html)
- **Subtitle/Role:** Academic Team Project
- **Date:** Fall 2025
- **Card Thumbnail (for index.html):** `Project_4/Project_3/Pictures/fig_1_2d_wave_diffraction_square_geometry.png`
- **Tools Used:** Python, NumPy, SciPy, Matplotlib, VIZIR4 (INRIA)
- **Problem/Goal:** Solving 2D wave diffraction around obstacles via the Boundary Element Method generates dense linear systems with high memory and $O(N^3)$ computational costs. The goal was to develop a fast BEM solver accelerated by Hierarchical Matrices (H-matrices) and Adaptive Cross Approximation (ACA) to achieve quasi-linear $O(N \log N)$ complexity.
- **What I Did (Bullet points for the page):**
  - Derived the analytical trace solution and built a 2D BEM solver using Galerkin discretization, Gauss-Legendre quadrature, and semi-analytical integration to handle Green's function diagonal singularities.
  - Benchmarked low-rank matrix compression methods (Truncated SVD, Complete ACA, and Partial ACA), selecting Partial ACA for its superior $O(k(m+n))$ factorization speed (0.005s vs. 0.252s for SVD).
  - Implemented spatial binary trees (geometric and balanced partitioning) with an admissibility criterion coupled to a GMRES iterative solver, reducing assembly and solve complexity from $O(N^2)/O(N^3)$ to $O(N \log N)$.
  - Extended the solver beyond circular disks to complex 2D geometries (square, ellipse, boomerang, star, and non-convex shapes) and visualized 2D diffracted wave fields across 20,000-triangle meshes in VIZIR4.
- **Results:** Achieved a memory compression ratio down to 12.43% (at $N=1600$) and over 10x faster matrix assembly compared to dense solvers while maintaining high numerical accuracy against analytical solutions.
- **Gallery Images & Captions:**
  - `Project_4/Project_3/Pictures/fig_1_2d_wave_diffraction_square_geometry.png` — Total diffracted wave fields ($\text{Re}(u_{\text{total}})$) simulated across various 2D obstacle geometries ($N=800$, $k=10$).
  - `Project_4/Project_3/Pictures/fig_2_hierarchical_matrix_block_compression_structure.png` — Hierarchical matrix structure ($400 \times 400$) distinguishing dense near-field blocks (red) from low-rank ACA-compressed far-field blocks (green).
  - `Project_4/Project_3/Pictures/fig_3_computational_complexity_benchmark_dense_vs_hmatrix.png` — Log-log runtime benchmark demonstrating the reduction from $O(N^2)/O(N^3)$ dense complexity to quasi-linear $O(N \log N)$ assembly and GMRES solve times.
- **pdf of the project:**
  - `Project_4/Project_3/Report_Frontier_Element_Method_Pt1.pdf`
  - `Project_4/Project_3/Report_Frontier_Element_Method_Pt2.pdf`
  - `Project_4/Project_3/Report_Frontier_Element_Method_Pt3.pdf`
  - `Project_4/Project_3/Report_Frontier_Element_Method_Pt4.pdf`

---

# PROJECT 4.4: Periodic Homogenization via Finite Element Method (FEM) (For Project_4.html)
- **Subtitle/Role:** Academic Project
- **Date:** 2025
- **Card Thumbnail (for index.html):** `Project_4/Project_4/Pictures/fig_2_cell_corrector_w1_3d.png`
- **Tools Used:** Python, NumPy, SciPy, Matplotlib, Finite Element Method (FEM)
- **Problem/Goal:** Implement a 2D Finite Element solver from scratch to approximate partial differential equations with rapidly oscillating periodic coefficients, comparing the exact micro-scale solution against the homogenized macro-scale model.
- **What I Did (Bullet points for the page):**
  - Developed a 2D P1 Finite Element solver in Python supporting Dirichlet, Neumann, and periodic boundary conditions via projection matrices ($P_{per}$).
  - Verified solver convergence against analytical solutions, achieving the theoretical order 2 convergence rate in $L^2$ norm.
  - Computed cell correctors ($w_i$) on the unit periodicity cell to derive the homogenized effective diffusion tensor ($A^{eff}$).
  - Simulated and compared the oscillating solution ($u^\epsilon$) against the homogenized macro-scale solution ($u^0$) across varying $\epsilon$ scales in $L^2$ and $H^1$ norms.
- **Results:** Validated the numerical effective tensor ($A^{eff}_{11} \approx 1.7765$) against the theoretical value ($\sqrt{3} \approx 1.7321$) and confirmed the asymptotic convergence of the homogenized model as $\epsilon \to 0$.
- **Gallery Images & Captions:**
  - `Project_4/Project_4/Pictures/fig_1_3d_periodic_fem_solution.png`: **3D Periodic Solution:** Finite element approximation of the test function $\sin(\pi x)\sin(2\pi y)$ validating the periodic boundary projection matrix $P_{per}$.
  - `Project_4/Project_4/Pictures/fig_2_cell_corrector_w1_3d.png`: Micro-Scale Cell Corrector ($w_1$): 3D visualization of the periodic corrector function computed on the unit cell to capture micro-scale oscillations and derive the effective diffusion tensor $A^{eff}$.
  - `Project_4/Project_4/Pictures/fig_3_homogenization_error_vs_epsilon.png`: Homogenization Convergence: Evolution of the relative $L^2$ error between the micro-scale oscillating solution ($u^\epsilon$) and the homogenized macro-scale solution ($u^0$) as a function of $\ln(\epsilon)$. 
- **pdf of the project:**
  - `Project_4/Project_4/Report_Periodic_Homogenization.pdf`

---

# PROJECT 4.5: Numerical Study of Demagnetizing Energy & iLLG Simulation (For Project_4.html)
- **Subtitle/Role:** Personnal Independent Research Project
- **Date:** Summer 2025
- **Card Thumbnail (for index.html):** `Project_4/Project_5/Pictures/fig_0_title_and_author.png`
- **Tools Used:** Python (NumPy, SciPy, Matplotlib)
- **Problem/Goal:** Numerically compute the demagnetizing (stray field) energy in ferromagnetic materials using 4D spherical harmonics and develop a finite-difference solver to simulate ultrafast inertial magnetization dynamics via the inertial Landau-Lifshitz-Gilbert (iLLG) equation.
- **What I Did (Bullet points for the page):**
  - Implemented the Arrar & Boulmezaoud analytical-numerical method using 4D spherical harmonics, iterative Chebyshev polynomials, and Gauss-Legendre quadrature to compute stray field energy.
  - Validated the demagnetizing energy solver on a unit sphere ($R=1$), matching literature benchmark values to 6 decimal places (0.0769663 vs. 0.07696625 reference).
  - Formulated and coded a 1D semi-implicit finite-difference scheme with Neumann boundary conditions and matrix inversion to simulate the inertial Landau-Lifshitz-Gilbert (iLLG) equation.
  - Analyzed numerical stability, discretization sensitivity, and magnetization norm preservation by benchmarking simulated mean magnetization trajectories against theoretical damped oscillations.
- **Results:** Successfully validated the demagnetizing energy calculation method against published benchmarks and built a functional prototype solver for the iLLG equation, identifying key discretization and stability constraints for future implicit schemes.
- **Gallery Images & Captions:**
  - `Project_4/Project_5/Pictures/fig_1_literature_benchmark_damped_oscillations.png` | Theoretical benchmark from literature showing the expected damped oscillations of mean magnetization components ($\langle m_1 \rangle$ and $\langle m_2 \rangle$) over time.
  - `Project_4/Project_5/Pictures/fig_2_python_solver_mean_magnetization_output.png` | Simulation output from the custom Python semi-implicit finite-difference solver showing the time evolution of mean magnetization ($\langle m_1 \rangle$), highlighting numerical stability and discretization sensitivity.
- **pdf of the project:**
  - `Project_4/Project_5/2025_Perso_Project_Micromagnetism.pdf`

---

# PROJECT 4.6: Numerical Approximation of Wave Diffraction via Geometrical Optics (For Project_4.html)
- **Subtitle/Role:** Academic Team Project (Pair Programming)
- **Date:** 2026
- **Card Thumbnail (for index.html):** `Project_4/Project_6/Pictures/fig_3_absolute_error_comparison_fem_vs_go.png`
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
  - `Project_4/Project_6/Pictures/fig_1_reflected_rays_characteristics.png`: Visualization of the eikonal equation characteristics (reflected rays) around the circular obstacle in ParaView.
  - `Project_4/Project_6/Pictures/fig_2_geometrical_optics_wave_solution_k10.png`: Real part of the diffracted wave field approximated via Geometrical Optics for wavenumber $k=10$.
  - `Project_4/Project_6/Pictures/fig_3_absolute_error_comparison_fem_vs_go.png`: Absolute error distribution between the Geometrical Optics approximation and the P4 FEM reference solution, highlighting accuracy in the illuminated zone and divergence in the shadow zone.
- **pdf of the project:**
  - `Project_4/Project_6/Report_Approximation_with_Geometric_Optic.pdf`

---

# PROJECT 4.7: Proof & Visualization of Sard's Theorem (For Project_4.html)
- **Subtitle/Role:** Academic Team Project (L3 Mathematics - Semester 6)
- **Date:** Spring 2025
- **Card Thumbnail (for index.html):** `Project_4/Project_7/Pictures/fig_1_3d_curve_zero_measure_plane.png`
- **Tools Used:** LaTeX, GeoGebra, Differential Calculus, Measure Theory
- **Problem/Goal:** Study, prove, and illustrate Sard's Theorem in differential topology, which establishes that the set of critical values of a smooth function between Euclidean spaces has a Lebesgue measure of zero.
- **What I Did (Bullet points for the page):**
  - Constructed a complete, rigorous mathematical proof of Sard's Theorem by induction on dimension $m$, covering all critical point subsets ($m < n$, $C \setminus C_1$, $C_i \setminus C_{i+1}$, and $C_k$ for $k > \frac{m}{n} - 1$).
  - Applied foundational analytical tools including Taylor's theorem with integral remainder, Fubini's theorem, the Implicit Function Theorem, and the Local Inversion Theorem.
  - Analyzed theoretical base cases ($m=n=1$ and $m=2, n=1$) and modeled practical geometric examples—such as $f(x)=(x^2, x+1)$ and $g(x)=\frac{\sin(x)}{x}$—using 2D and 3D plots to visualize how infinite critical points still yield zero-measure image sets.
  - Authored and typeset the complete 8-page technical report in LaTeX under the supervision of Prof. Luc Robbiano, referencing Milnor's *Topology from the Differentiable Viewpoint*.
- **Gallery Images & Captions:**
  - `Project_4/Project_7/Pictures/fig_1_3d_curve_zero_measure_plane.png` : Graphical representation of $f(x) = (x^2, x+1)$ in $\mathbb{R}^3$, illustrating how the image of a mapping from a lower-dimensional space lies entirely within the plane $z = x - 1$, yielding a Lebesgue measure of zero.
  - `Project_4/Project_7/Pictures/fig_2_2d_sinc_infinite_critical_values.png` : Infinite Critical Values of $g(x) = \frac{\sin(x)}{x}$:** 2D plot demonstrating a function with infinitely many local extrema (critical points) whose image set nonetheless maintains a Lebesgue measure of zero, visually confirming Sard's Theorem.
- **pdf of the project:**
  - `Project_4/Project_7/Sard_Theorem.pdf`

---

# PROJECT 4.8: Hyperbolic Quadrature Method of Moments (HyQMOM) — Literature Synthesis (For Project_4.html)
- **Subtitle/Role:** Academic Literature Synthesis | Applied Mathematics
- **Date:** January 2026
- **Card Thumbnail (for index.html):** `Project_4/Project_8/Pictures/fig_0_title_and_author.png`
- **Tools Used:** LaTeX, Mathematical Analysis, Orthogonal Polynomials
- **Problem/Goal:** Making the 2022 Fox & Laurent research paper on arbitrary-order ($2n+1$) moment closures for 1-D kinetic equations accessible by distilling complex proofs into a structured, clear mathematical guide.
- **What I Did (Bullet points for the page):**
  - Synthesized the core mathematical framework of the Hyperbolic Quadrature Method of Moments (HyQMOM), contrasting arbitrary-order closures against earlier 4th-order limitations.
  - Broken down the change-of-variable proofs using centered and standardized moments to demonstrate translation and scaling invariance.
  - Clarified the characteristic polynomial factorization ($P_{2n+1}(X) = Q_n(X)R_{n+1}(X)$) and summarized the global hyperbolicity proof via orthogonal polynomial root separation and the Christoffel-Darboux formula.
  - Documented the simplified direct closure algorithm (using the Reverse Chebyshev method) that operates directly on raw moments $M_{2n}$ without intermediate standardization steps.
- **Gallery Images & Captions:**
  - `Project_4/Project_8/Pictures/fig_1_hyqmom_closure_algorithm.png` — Direct raw-moment closure algorithm (Algorithm 1) computing $M_{2n+1}$ from $M_{2n}$ via the Reverse Chebyshev method without intermediate standardization.
- **pdf of the project:**
  - `Project_4/Project_8/Report_Moment_Method.pdf`

---

# Certifications:
this is a list of all certifications i got recently:
`Project_4/Certifications/learn-git-branching-certificate-antoine-levrat.png` - learn-git-branching
