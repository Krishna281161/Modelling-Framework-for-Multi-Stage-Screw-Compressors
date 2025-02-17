This repository contains the Python-based modelling and optimization framework developed for the analysis and optimization of multi-stage screw compressors. The framework integrates physics-based thermodynamic models with machine learning and Bayesian optimization techniques to enhance the design, efficiency, and performance of multi-stage screw compressors.

Overview
The framework provides a structured methodology for optimizing screw compressor parameters using batch file execution and simulation environments such as SCORG and GT-SUITE. It employs advanced optimization techniques like:

Bayesian Optimization
Evolutionary Algorithms
Repetitive Parameter Sweeps
It also features a Graphical User Interface (GUI) for interactive use.

Features
✅ Modular Python Code: Easily adaptable to different optimization scenarios.
✅ Automated Batch Execution: Interfaces with SCORG & GT-SUITE simulations.
✅ Advanced Optimization Algorithms: Implements Bayesian Optimization and Differential Evolution.
✅ Performance Metric Extraction: Reads outputs, processes results, and visualizes optimization progress.
✅ Graphical User Interface (GUI): Tkinter-based GUI for user-friendly input handling and execution.

Installation
Clone the repository
bash
Copy
Edit
git clone https://github.com/your-username/Modelling-Framework-Multi-Stage-Screw-Compressors.git
Navigate into the repository
bash
Copy
Edit
cd Modelling-Framework-Multi-Stage-Screw-Compressors
Install required dependencies
bash
Copy
Edit
pip install -r requirements.txt
Usage
1️⃣ Running the Optimization Framework
You can run the Python script directly using:

bash
Copy
Edit
python main.py
This will:

Accept input parameters
Modify batch files for SCORG/GT-SUITE
Execute the simulation
Optimize parameters using Bayesian Optimization and Evolutionary Algorithms
2️⃣ Running the GUI
The Tkinter-based GUI can be launched with:

bash
Copy
Edit
python gui.py
This interface allows users to:

Select batch and output files
Define target optimization values
Choose between Bayesian Optimization and Evolutionary Algorithms
View results interactively
Optimization Methods Implemented
🔹 Bayesian Optimization

Utilizes Gaussian Process Regression (GPR) with a Matern kernel to optimize compressor parameters with minimal iterations.
🔹 Evolutionary Algorithm (Differential Evolution)

Performs a global search to find the optimal compressor parameters using population-based iterative improvement.
🔹 Repetitive Parameter Sweeps

Used to enhance robustness by refining optimization results across multiple runs.
Code Structure
📂 src/

main.py → Core optimization script
bayesian_optimizer.py → Implements Bayesian Optimization
evolutionary_optimizer.py → Implements Differential Evolution
utils.py → Helper functions for batch execution and parsing
📂 gui/

gui.py → Tkinter GUI for user interaction
📂 docs/

Thesis documentation and explanation of methodology
📂 results/

Stores logs and output files from optimization runs
Example: Running Bayesian Optimization
python
Copy
Edit
from bayesian_optimizer import bayesian_optimization

bounds = [(1.0, 10.0), (100.0, 500.0), (50.0, 300.0)]  # Parameter bounds
optimal_params, min_error = bayesian_optimization(bounds, n_iter=20)
print(f"Optimal Parameters: {optimal_params}, Minimum Error: {min_error}")
Graphical User Interface (GUI)
A Tkinter-based GUI is included for users who prefer an interactive experience.
It supports:

File selection for batch execution
Target parameter input
Real-time optimization using Bayesian & Evolutionary methods
Visualization of results
Applications
🔹 Optimizing compressor parameters such as oil injection pressure, temperature, and angle.
🔹 Performing design exploration by iterating over geometry and profile parameters.
🔹 Comparing optimization algorithms for efficiency and performance.
🔹 Generating insights into parameter sensitivity and trade-offs in design.

