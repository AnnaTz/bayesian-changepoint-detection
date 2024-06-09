
This project was developed for the 'Uncertainty Assessment and Bayesian Computation' course, part of the MSc in Data Analytics at the University of Glasgow in 2023. It showcases statistical change-point detection and analysis on the UK coal mining disaster data from 1851 to 1962. It utilizes Bayesian optimization modeling to identify significant shifts in the rate of these disasters, offering insights into the dynamics of industrial accidents over time. 

## Key Components

- **Statistical Modelling & Inference**: The counts of annual mining disasters were modelled as observations from a Poisson process, with Gamma priors on the rate parameters and discrete uniform priors on the years in between change-points. The posterior and posterior predictive distributions, as well as the model marginals, were analytically produced, and then approximated by Sequential Monte Carlo sampling leveraging the PyMC library.
- **Model Selection**: Models with varying complexity were fitted and evaluated to estimate the optimal number of change-points.

## Project Structure

- `code.ipynb`: Implements the Bayesian modeling and posterior sampling for the change-point detection, produces inference results and extracts the models' marginals to evaluate their performance.
- `report.ipynb`: Provides a thorough examination of the Bayesian change-point detection process, including the statistical models, inference techniques, and analysis of the results.
- `plots/`: Contains all figures and plots generated and captioned by `code.ipynb`, and presented in `report.ipynb`.

## Usage Instructions

To reproduce the analysis and results:
1. Ensure that Python 3.8+ is installed along with Jupyter Notebook or JupyterLab.
2. Clone the repository:
   ```bash
   git clone https://github.com/AnnaTz/bayesian-changepoint-detection.git
   ```
3. Navigate to the cloned directory and install the required packages:
   ```bash
   pip install -r requirements.txt
   ```
4. Launch Jupyter Notebook or JupyterLab, and run `code.ipynb` followed by `report.ipynb`.
