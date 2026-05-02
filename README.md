# **`README.md`**

# A Motif-Based Framework for Decomposing Risk Spillovers

<!-- PROJECT SHIELDS -->
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![arXiv](https://img.shields.io/badge/arXiv-2604.25406-b31b1b.svg)](https://arxiv.org/abs/2604.25406)
[![Journal](https://img.shields.io/badge/Journal-ArXiv%20Preprint-003366)](https://arxiv.org/abs/2604.25406)
[![Year](https://img.shields.io/badge/Year-2026-purple)](https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover)
[![Discipline: Econometrics](https://img.shields.io/badge/Discipline-Quantile%20Econometrics-00529B)](https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover)
[![Discipline: Network Science](https://img.shields.io/badge/Discipline-Computational%20Network%20Science-00529B)](https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover)
[![Discipline: Topology](https://img.shields.io/badge/Discipline-Combinatorial%20Topology-00529B)](https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover)
[![Data Sources](https://img.shields.io/badge/Data-Investing.com%20%7C%20Commodity%20%26%20Equity%20Futures-lightgrey)](https://www.investing.com/)
[![Core Method: QVAR](https://img.shields.io/badge/Method-QVAR%20%7C%20GFEVD-orange)](https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover)
[![Core Method: Joint Connectedness](https://img.shields.io/badge/Method-Joint%20Connectedness-orange)](https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover)
[![Core Method: Disparity Filter](https://img.shields.io/badge/Method-Disparity%20Filter-orange)](https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover)
[![Core Method: Motifs](https://img.shields.io/badge/Method-Triadic%20Motifs%20%7C%20Orbits-orange)](https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover)
[![Optimization](https://img.shields.io/badge/Optimization-MSP%20Portfolio-red)](https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Type Checking: mypy](https://img.shields.io/badge/type%20checking-mypy-blue)](http://mypy-lang.org/)
[![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=flat&logo=numpy&logoColor=white)](https://numpy.org/)
[![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=flat&logo=scipy&logoColor=white)](https://scipy.org/)
[![NetworkX](https://img.shields.io/badge/NetworkX-%2300529B.svg?style=flat)](https://networkx.org/)
[![Statsmodels](https://img.shields.io/badge/Statsmodels-%233F51B5.svg?style=flat)](https://www.statsmodels.org/)
[![YAML](https://img.shields.io/badge/YAML-%23CB171E.svg?style=flat&logo=yaml&logoColor=white)](https://yaml.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-%23F37626.svg?style=flat&logo=Jupyter&logoColor=white)](https://jupyter.org/)
[![Open Source](https://img.shields.io/badge/Open%20Source-%E2%9D%A4-brightgreen)](https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover)

**Repository:** `https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover`

**Owner:** 2026 Craig Chirinda (Open Source Projects)

This repository contains an **independent**, professional-grade Python implementation of the research methodology from the 2026 paper entitled **"A Motif-Based Framework for Decomposing Risk Spillovers"** by:

*   **Ying-Hui Shao**
*   **Yan-Hong Yang**
*   **Yun Zhang**

The project provides a complete, end-to-end computational framework for replicating the paper's findings. It delivers a modular, highly optimized pipeline that executes the entire research workflow: from the rigorous ingestion of high-dimensional financial time series and the estimation of state-dependent Quantile Vector Autoregressions (QVAR), to the extraction of multiscale topological backbones and the exact isomorphism-backed enumeration of directed triadic motifs. The pipeline culminates in the construction of the Minimum Structural Similarity Portfolio (MSP), demonstrating that local triadic topology carries portfolio-relevant information that aggregate connectedness measures systematically miss.

## Table of Contents

- [Introduction](#introduction)
- [Theoretical Background](#theoretical-background)
- [Features](#features)
- [Methodology Implemented](#methodology-implemented)
- [Core Components (Notebook Structure)](#core-components-notebook-structure)
- [Key Callable: `execute_master_research_pipeline`](#key-callable-execute_master_research_pipeline)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Input Data Structure](#input-data-structure)
- [Usage](#usage)
- [Output Structure](#output-structure)
- [Project Structure](#project-structure)
- [Customization](#customization)
- [Contributing](#contributing)
- [Recommended Extensions](#recommended-extensions)
- [License](#license)
- [Citation](#citation)
- [Acknowledgments](#acknowledgments)

## Introduction

This project provides a Python implementation of the analytical framework presented in Shao, Yang, & Zhang (2026). The core of this repository is the iPython Notebook `framework_for_decomposing_risk_spillovers_draft.ipynb`, which contains a comprehensive suite of orchestrated tasks to replicate the paper's findings.

The pipeline addresses a foundational vulnerability in systemic risk analysis: the reliance on aggregate connectedness measures (like the Total Connectedness Index) which obscure the local interaction patterns that actually generate systemic risk. 

The codebase operationalizes the proposed solution—a **Mesoscopic Structural Risk-Navigation System**:
-   **Anchors** risk measurement in state-dependent dynamics via Quantile Vector Autoregression (QVAR) and an $R^2$-grounded Extended Joint Connectedness framework.
-   **Enforces** topological sparsification using the Disparity Filter algorithm, isolating the robust structural "skeleton" of the market from stochastic micro-fluctuations.
-   **Propagates** the analysis to the mesoscopic level by enumerating 13 directed triadic motifs and 30 unique node orbits using exact graph isomorphism, identifying statistically significant building blocks of risk transmission against degree-preserving null models.
-   **Evaluates** the representation's utility through the Minimum Structural Similarity Portfolio (MSP), which diversifies across local network roles rather than return covariances, yielding superior risk-adjusted performance in tail states.

## Theoretical Background

The implemented methods combine techniques from Advanced Quantile Econometrics, Computational Network Science, and Combinatorial Topology.

**1. Quantile-Based Joint Connectedness:**
Traditional mean-based models fail to capture heavy-tailed distributions. The framework utilizes a $p$-order QVAR model transformed via the Wold Theorem to compute the Generalized Forecast Error Variance Decomposition (GFEVD). This is normalized using an $R^2$-grounded joint framework to ensure bounded, mathematically rigorous spillover metrics:
$$ S_{i\leftarrow \bullet}^{jnt,from}(H) = \frac{\sum_{h=0}^{H-1} e'_i \Psi_{h,t}(\tau) \Sigma_t(\tau) M_i (M'_i \Sigma_t(\tau) M_i)^{-1} M'_i \Sigma_t(\tau) \Psi'_{h,t}(\tau) e_i}{\sum_{h=0}^{H-1} e'_i \Psi_{h,t}(\tau) \Sigma_t(\tau) \Psi'_{h,t}(\tau) e_i} $$

**2. Multiscale Backbone Extraction (Disparity Filter):**
To prevent the destruction of multiscale properties inherent in global thresholding, the framework evaluates edge significance from both the transmitter's and receiver's local perspectives:
$$ \alpha_{ij,t}^{out}(\tau) = 1 - (k_{i,t}^{out}(\tau) - 1) \int_0^{w_{ij,t}(\tau)/s_{i,t}^{out}(\tau)} (1-x)^{k_{i,t}^{out}(\tau)-2} dx $$

**3. Mesoscopic Topology and Positional Diversity:**
The framework shifts the analytical unit from individual nodes to 13 directed triadic motifs and 30 orbits. An asset's structural role dispersion is quantified using Shannon entropy (Positional Diversity):
$$ d_{i,t} = - \sum_{j=1}^{30} p_{ij,t} \ln p_{ij,t} $$

**4. Minimum Structural Similarity Portfolio (MSP):**
The topological insights are operationalized into Modern Portfolio Theory by substituting the return covariance matrix with the motif-based structural similarity matrix $H_t$:
$$ \omega_{S,t} = \frac{H_t^{-1} \mathbf{1}}{\mathbf{1}' H_t^{-1} \mathbf{1}} $$

Below is a diagram which summarizes the proposed approach:

<div align="center">
  <img src="https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover/blob/main/framework_for_decomposing_risk_spillover_ipo_main_six.png" alt="Mesoscopic Risk Framework Architecture" width="100%">
</div>

## Features

The provided iPython Notebook implements the full research pipeline, including:

-   **Strict Econometric Diagnostics:** Enforces synchronous time-series integrity by rejecting non-finite matrices prior to Augmented Dickey-Fuller (ADF) and Jarque-Bera (JB) testing.
-   **Look-Ahead Bias Prevention:** Restricts VAR lag selection (BIC) strictly to a pre-sample training window.
-   **Tikhonov Regularization:** Automatically applies ridge penalties ($\epsilon \mathbf{I}$) to singular residual covariance matrices during high-dimensional equation-by-equation QVAR estimation.
-   **Exact Graph Isomorphism:** Replaces brittle structural heuristics with `networkx.is_isomorphic` to guarantee 100% topological accuracy during motif enumeration and orbit assignment.
-   **Rigorous Null Model Aggregation:** Computes aggregate Z-scores by comparing time-averaged observed counts to pooled null variances, preventing the mathematical distortion of averaging daily Z-scores.
-   **Configuration-Driven Design:** All study parameters, topological thresholds ($\alpha$), and hierarchical taxonomies are managed in an external `config.yaml` file, ensuring strict methodological reproducibility.

## Methodology Implemented

The core analytical steps directly implement the methodology from the paper:

1.  **Data Preprocessing (Tasks 1-5):** Ingests raw futures data. Enforces strict temporal monotonicity, cross-sectional completeness ($N=39$), and calendar alignment.
2.  **Econometric Estimation (Tasks 6-12):** Selects optimal lags, defines rolling windows ($w=200$), estimates the QVAR across quantiles ($\tau \in \{0.05, 0.50, 0.95\}$), and computes the Wold moving-average representation.
3.  **Connectedness Modeling (Tasks 13-21):** Computes the GFEVD, scales it via the Joint Connectedness framework, and derives directional (TO, FROM, NET), decomposed (Internal/External), and aggregate spillovers.
4.  **Topological Sparsification (Tasks 22-27):** Applies the Disparity Filter to extract the multiscale weighted ($A_t$) and binary ($B_t$) backbones.
5.  **Mesoscopic Analysis (Tasks 28-38):** Enumerates 13 motifs and 30 orbits, generates degree-preserving null networks via parallelized Markov Chains, computes Z-scores, and constructs the Structural Similarity Matrix ($H_t$).
6.  **Portfolio Engineering (Tasks 39-43):** Solves for optimal weights (MVP, MCP, MCoP, MSP), computes out-of-sample risk-adjusted returns (Sharpe, CVaR), and aggregates sector exposures.
7.  **Validation & Audit (Tasks 44-49):** Generates publication-ready tables and figures, conducts robustness checks ($w=250$), and programmatically audits the empirical outputs against the manuscript's core findings.

## Core Components (Notebook Structure)

The notebook is structured as a logical pipeline with modular orchestrator functions for each of the 49 major tasks. All functions are self-contained, fully documented with strict type hints and comprehensive docstrings, and designed for professional-grade execution.

## Key Callable: `execute_master_research_pipeline`

The project is designed around a single, top-level user-facing interface function:

-   **`execute_master_research_pipeline`:** This apex orchestrator function runs the entire automated research pipeline from end-to-end. A single call to this function reproduces the entire computational portion of the project, managing data validation, QVAR estimation, topological sparsification, motif enumeration, portfolio optimization, robustness checks, and the final reproduction audit.

## Prerequisites

-   Python 3.10+
-   Core Python dependencies: `numpy`, `pandas`, `scipy`, `statsmodels`, `networkx`, `joblib`, `matplotlib`, `seaborn`, `pyyaml`.

## Installation

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover.git
    cd framework_for_decomposing_risk_spillover
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install Python dependencies:**
    ```sh
    pip install numpy pandas scipy statsmodels networkx joblib matplotlib seaborn pyyaml
    ```

## Input Data Structure

The pipeline requires a strictly formatted `pandas.DataFrame` (`df_raw`) containing the following columns:
-   `date`: `datetime64[ns]` (Strictly aligned common business days).
-   `ticker`: `category` (Must match the 39-asset universe exactly).
-   `asset_class`: `category` (Commodity or Equity).
-   `sector`: `category` (7-class taxonomy: Energy, Grains_Oilseeds, etc.).
-   `four_class_sector`: `category` (4-class taxonomy).
-   `log_returns`: `float64` (Decimal logarithmic returns, $r_t = \ln(P_t/P_{t-1})$).
-   `price_source_flag`: `category` (e.g., 'Investing.com').
-   `is_common_business_day`: `bool` (Alignment flag).

*Note: The pipeline includes a high-fidelity synthetic data generator that simulates heavy-tailed, stationary returns for testing purposes.*

## Usage

The notebook provides a complete, step-by-step guide. The primary workflow is to execute the final cell, which demonstrates how to load the configuration, generate synthetic benchmark data, and use the top-level orchestrator to execute the pipeline:

```python
import pandas as pd
import numpy as np
import yaml
from typing import Dict, Any, List, Tuple

# ==============================================================================
# Step 1: Synthetic Data Generation (df_raw)
# ==============================================================================
# Initialize random seed for strict reproducibility
np.random.seed(12345)

def generate_synthetic_futures_data(
    start_date: str = "2010-04-16",
    end_date: str = "2025-09-05"
) -> pd.DataFrame:
    """
    Generates a synthetic, high-fidelity DataFrame of 39 futures contracts.
    Simulates heavy-tailed (Student's t, df=5), stationary log-returns to 
    satisfy the strict econometric diagnostic requirements (ADF and JB tests).
    """
    if pd.Timestamp(start_date) >= pd.Timestamp(end_date):
        raise ValueError("start_date must be strictly before end_date.")

    dates: pd.DatetimeIndex = pd.date_range(start=start_date, end=end_date, freq='B')
    T: int = len(dates)

    # Strict hierarchical taxonomy mapping
    taxonomy_map: Dict[str, Tuple[str, str, str]] = {
        "WTI": ("Energy", "Energy", "Commodity"), "NGS": ("Energy", "Energy", "Commodity"),
        "HOL": ("Energy", "Energy", "Commodity"), "GAL": ("Energy", "Energy", "Commodity"),
        "COL": ("Energy", "Energy", "Commodity"),
        "CRN": ("Grains_Oilseeds", "Agriculture", "Commodity"), "WHT": ("Grains_Oilseeds", "Agriculture", "Commodity"),
        "SBN": ("Grains_Oilseeds", "Agriculture", "Commodity"), "RIC": ("Grains_Oilseeds", "Agriculture", "Commodity"),
        "OAT": ("Grains_Oilseeds", "Agriculture", "Commodity"), "SBM": ("Grains_Oilseeds", "Agriculture", "Commodity"),
        "SBO": ("Grains_Oilseeds", "Agriculture", "Commodity"),
        "SGR": ("Softs", "Agriculture", "Commodity"), "COF": ("Softs", "Agriculture", "Commodity"),
        "CCA": ("Softs", "Agriculture", "Commodity"), "CTN": ("Softs", "Agriculture", "Commodity"),
        "OJC": ("Softs", "Agriculture", "Commodity"), "LUM": ("Softs", "Agriculture", "Commodity"),
        "LCT": ("Livestock", "Agriculture", "Commodity"), "FCT": ("Livestock", "Agriculture", "Commodity"),
        "HOG": ("Livestock", "Agriculture", "Commodity"), "MLK": ("Livestock", "Agriculture", "Commodity"),
        "GLD": ("Precious_Metals", "Metals", "Commodity"), "SLV": ("Precious_Metals", "Metals", "Commodity"),
        "PLD": ("Precious_Metals", "Metals", "Commodity"), "PLT": ("Precious_Metals", "Metals", "Commodity"),
        "ALM": ("Industrial_Metals", "Metals", "Commodity"), "CPR": ("Industrial_Metals", "Metals", "Commodity"),
        "ZNC": ("Industrial_Metals", "Metals", "Commodity"), "LED": ("Industrial_Metals", "Metals", "Commodity"),
        "NKL": ("Industrial_Metals", "Metals", "Commodity"), "TIN": ("Industrial_Metals", "Metals", "Commodity"),
        "SPX": ("Equity", "Equity", "Equity"), "ESX": ("Equity", "Equity", "Equity"),
        "UKX": ("Equity", "Equity", "Equity"), "NKI": ("Equity", "Equity", "Equity"),
        "ASX": ("Equity", "Equity", "Equity"), "IBV": ("Equity", "Equity", "Equity"),
        "CSI": ("Equity", "Equity", "Equity")
    }

    tickers: List[str] = list(taxonomy_map.keys())
    N: int = len(tickers)
    records: List[Dict[str, Any]] = []

    for date in dates:
        # Simulate heavy-tailed returns
        daily_returns: np.ndarray = np.random.standard_t(df=5, size=N) * 0.015
        for i, ticker in enumerate(tickers):
            sector_7, sector_4, asset_class = taxonomy_map[ticker]
            records.append({
                "date": date, "ticker": ticker, "asset_class": asset_class,
                "sector": sector_7, "four_class_sector": sector_4,
                "log_returns": np.float64(daily_returns[i]),
                "price_source_flag": "Investing.com", "is_common_business_day": True
            })

    df_raw: pd.DataFrame = pd.DataFrame(records)
    df_raw["date"] = df_raw["date"].astype("datetime64[ns]")
    df_raw["ticker"] = df_raw["ticker"].astype("category")
    df_raw["asset_class"] = df_raw["asset_class"].astype("category")
    df_raw["sector"] = df_raw["sector"].astype("category")
    df_raw["four_class_sector"] = df_raw["four_class_sector"].astype("category")
    df_raw["log_returns"] = df_raw["log_returns"].astype("float64")
    df_raw["price_source_flag"] = df_raw["price_source_flag"].astype("category")
    df_raw["is_common_business_day"] = df_raw["is_common_business_day"].astype(bool)

    return df_raw

df_raw = generate_synthetic_futures_data()

# ==============================================================================
# Step 2: Loading the Configuration (config.yaml)
# ==============================================================================
def load_study_configuration(filepath: str = "config.yaml") -> Dict[str, Any]:
    """Loads the deterministic hyperparameters and taxonomies."""
    if not isinstance(filepath, str):
        raise TypeError(f"filepath must be a string, got {type(filepath)}.")
    try:
        with open(filepath, "r") as file:
            config: Dict[str, Any] = yaml.safe_load(file)
        print(f"\nSuccessfully loaded configuration from {filepath}")
        return config
    except FileNotFoundError:
        print(f"\nWarning: {filepath} not found. Please ensure the file exists.")
        return {}
    except yaml.YAMLError as e:
        print(f"\nError parsing YAML file {filepath}: {e}")
        raise

study_config: Dict[str, Any] = load_study_configuration()

# ==============================================================================
# Step 3: Executing the Pipeline
# ==============================================================================
if __name__ == "__main__":
    if not df_raw.empty and study_config:
        print("\nInitiating Motif-Based Risk Decomposition Pipeline...")
        
        # Execute the master orchestrator
        # Note: execute_master_research_pipeline is defined in the Jupyter Notebook
        master_artifacts: Dict[str, Any] = execute_master_research_pipeline(
            df_raw=df_raw,
            config=study_config,
            main_output_dir_str="./study_outputs/main_execution"
        )
        
        print("\n" + "="*80)
        print("STUDY EXECUTION COMPLETE")
        print("="*80)
        
        # Accessing Main Results
        main_execution_results = master_artifacts["task_47_results"]["main_execution"]
        if main_execution_results.success:
            print("\n[Core Publication Tables]")
            core_tables = main_execution_results.tables
            print("\nTable 6: Portfolio Performance (Preview):")
            print(core_tables.table_6_portfolio.head())
            
            print("\n[Core Publication Figures]")
            core_figures = main_execution_results.figures
            print(f"Generated {len(core_figures.motif_portfolio_figs)} Motif & Portfolio Figures.")
            
        # Accessing Robustness Results
        print("\n[Robustness Analysis]")
        robustness_results = master_artifacts["task_48_results"]
        print(f"Traditional TCI Series Count: {len(robustness_results.tci_traditional_w200)}")

        # Printing the Final Audit Report Status
        print("\n" + "="*80)
        print("FINAL REPRODUCTION AUDIT")
        print("="*80)
        
        validation_status: bool = master_artifacts["task_49_validation_status"]
        if validation_status:
            print("STATUS: PASSED.")
            print("The empirical outputs perfectly reproduced the manuscript's core findings.")
        else:
            print("STATUS: FAILED. Empirical outputs deviated from manuscript findings.")
    else:
        print("Error: Missing data or configuration. Cannot proceed.")
```

## Output Structure

The pipeline returns a master dictionary and serializes artifacts to an `output_dir` containing:
-   **`aligned_returns_matrix.pkl`**: The cleansed, C-contiguous $T \times N$ return matrix.
-   **`qvar_coefficients.pkl` & `innovation_covariances.pkl`**: The state-dependent QVAR parameters.
-   **`jSOT.pkl` & `CT_t_tau.pkl`**: The dense joint connectedness matrices.
-   **`backbone_matrices.pkl`**: The multiscale weighted ($A_t$) and binary ($B_t$) backbones.
-   **`motif_counts.pkl` & `random_motif_counts.pkl`**: Empirical and null motif statistics.
-   **`H_t_matrices.pkl`**: The raw and regularized Structural Similarity Matrices.
-   **`portfolio_weights.pkl` & `portfolio_returns.pkl`**: The optimized MSP weights and out-of-sample performance.

## Project Structure

```
framework_for_decomposing_risk_spillover/
│
├── framework_for_decomposing_risk_spillovers_draft.ipynb    # Main implementation notebook
├── config.yaml                                              # Master configuration file
├── requirements.txt                                         # Python package dependencies
│
├── LICENSE                                                  # MIT Project License File
└── README.md                                                # This file
```

## Customization

The pipeline is highly customizable via the `config.yaml` file. Users can modify study parameters such as:
-   **Econometric Settings:** Adjust the `rolling_window_width_main` or the `candidate_lags` for the QVAR estimation.
-   **Topological Thresholds:** Modify the `significance_thresholds` ($\alpha$) for the Disparity Filter to test structural sensitivity.
-   **Null Model Rigor:** Increase the `iterations_R` for the degree-preserving randomization to achieve tighter confidence intervals on motif Z-scores.
-   **Portfolio Constraints:** Adjust the `ridge_epsilon` for Tikhonov regularization or modify the `cvar_confidence_level` for tail-risk benchmarking.

## Contributing

Contributions are welcome. Please fork the repository, create a feature branch, and submit a pull request with a clear description of your changes. Adherence to PEP 8, strict type hinting, and the 1:1 inline comment-to-code-line ratio is required.

## Recommended Extensions

Future extensions, as suggested by the authors, could include:
-   **Dynamic Community Detection:** Replacing fixed sector labels with data-driven partitions derived from community detection on the backbone itself.
-   **Temporal Motifs:** Moving from static triadic configurations to higher-order temporal motifs to model how specific subgraphs emerge, persist, or dissolve across consecutive trading sessions.
-   **Higher-Order Moment Optimization:** Linking the motif-based approach with higher-order moment risk analysis to optimize portfolios under severe non-normal return distributions.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Citation

If you use this code or the methodology in your research, please cite the original paper:

```bibtex
@article{shao2026motif,
  title={A Motif-Based Framework for Decomposing Risk Spillovers},
  author={Shao, Ying-Hui and Yang, Yan-Hong and Zhang, Yun},
  journal={arXiv preprint arXiv:2604.25406},
  year={2026}
}
```

For the implementation itself, you may cite this repository:
```
Chirinda, C. (2026). A Motif-Based Framework for Decomposing Risk Spillovers.
GitHub repository: https://github.com/chirindaopensource/framework_for_decomposing_risk_spillover
```

## Acknowledgments

-   Credit to **Ying-Hui Shao, Yan-Hong Yang, and Yun Zhang** for the foundational research that forms the entire basis for this computational replication.
-   This project is built upon the exceptional tools provided by the open-source community. Sincere thanks to the developers of the scientific Python ecosystem, particularly the **NumPy**, **Pandas**, **Statsmodels**, and **NetworkX** contributors.

--

*This README was generated based on the structure and content of the `framework_for_decomposing_risk_spillovers_draft.ipynb` notebook and follows best practices for research software documentation.*
