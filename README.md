# PPFID-IoMT:
# PPFID-IoMT

Privacy-preserving federated intrusion detection for IoMT-enabled healthcare environments using knowledge distillation, pseudo-data generation, and dynamic Pareto optimization.

## 🔎 Overview

Connected Internet of Medical Things (IoMT) devices support healthcare services but also introduce security and privacy challenges. Federated learning (FL) enables healthcare institutions to collaboratively train an intrusion detection model without exchanging raw data. However, keeping data local does not eliminate the risk of information leakage through federated communication.

PPFID-IoMT addresses four key challenges:

- **Privacy risks:** Exposure to membership inference attacks (MIAs) and data reconstruction attacks (DRAs).
- **Resource constraints:** Limited computational capacity, memory, and energy on IoMT devices.
- **Data heterogeneity:** Differences in traffic patterns and attack distributions across healthcare institutions.
- **Privacy–performance trade-off:** Maintaining effective intrusion detection while incorporating privacy-preserving mechanisms.

## ⚙️ Proposed Framework

PPFID-IoMT integrates the following components:

- **Two-stage federated training:** Coordinates learning across participating hospital-edge servers.
- **Knowledge distillation:** Transfers knowledge to a lightweight student model for deployment on resource-constrained IoMT devices.
- **Pseudo-data generation:** Supports student-model training under heterogeneous local data distributions.
- **Dynamic Pareto optimization (DPO):** Adaptively balances competing privacy and detection objectives during training.
- **Federated communication:** Exchanges the framework's designated components without transmitting updated teacher or student model parameters.

## 📂 Project Structure

Suggested organization:

| Folder or file | Contents |
|---|---|
| `Data/` | Dataset placement instructions and preprocessing resources |
| `Client/` | Local training at hospital-edge servers |
| `Server/` | Cloud-side coordination and aggregation |
| `Models/` | Teacher, student, and generator architectures |
| `DPO/` | Dynamic Pareto optimization |
| `Experiments/` | Training configurations and experiment scripts or notebooks |
| `Evaluation/` | Detection, privacy, and computational efficiency evaluation |
| `Utils/` | Shared utilities and data-partitioning functions |
| `requirements.txt` | Required Python packages |
| `README.md` | Project documentation |

## 🛠️ Installation and Usage

### 1. Install dependencies

After preparing the Python environment, install the required packages:

```bash
pip install -r requirements.txt
```

### 2. Prepare the datasets

Obtain the IoMT-TrafficData and MedSec-25 datasets from their official sources, subject to their access and licensing conditions.

Update the dataset paths in the relevant configuration files or notebooks.

### 3. Preprocess and partition the data

Run the preprocessing and partitioning code to prepare the local datasets for the participating hospital-edge servers.

The experiments consider different numbers of participants and non-IID settings controlled by the parameter α.

### 4. Run federated training

Run the experiment scripts or notebooks for the selected dataset to execute the two training stages.

**Add the exact filenames and execution commands here before publishing.**

### 5. Evaluate the framework

Run the corresponding evaluation scripts or notebooks to assess detection performance, privacy resilience, and computational efficiency.

**Add the exact evaluation commands here before publishing.**

## 📊 Datasets

The framework is evaluated on:

| Dataset | Access |
|---|---|
| IoMT-TrafficData | Add the official dataset URL and preparation instructions |
| MedSec-25 | Add the official dataset URL and preparation instructions |

Dataset files should be obtained separately unless their redistribution is permitted.

## 🧪 Experiments

The experimental evaluation covers:

- **Intrusion detection:** F1-score, accuracy, precision, and recall.
- **Data heterogeneity:** Comparisons across different non-IID partitioning settings.
- **Scalability:** Evaluation with different numbers of participating hospital-edge servers.
- **Optimization strategies:** Comparison of DPO with Fixed Weights, MGDA, PCGrad, and CAGrad.
- **Membership inference attacks:** Attack accuracy and sample-level privacy-risk scores.
- **Data reconstruction attacks:** Reconstruction fidelity measured using MSE and cosine similarity.
- **Computational efficiency:** Teacher–student comparisons of inference time, FLOPs, parameter count, memory consumption, and inference energy.
- **Generator ablation:** Comparison of PPFID-IoMT with and without the generator.

Privacy results provide empirical evidence under the evaluated attack settings.

## 🔁 Reproducibility

For each experiment, document:

- Python and package versions.
- Hardware configuration.
- Dataset preprocessing and train/test splits.
- Random seeds.
- Number of hospital-edge servers and non-IID partitioning parameter.
- Communication rounds, local epochs, batch sizes, and learning rates.
- Model architectures and optimization settings.
- Attack configurations and evaluation procedures.

## 📄 Citation

Add the paper's citation and BibTeX entry when available.

## 📜 License

Add the chosen code license in a `LICENSE` file.
Dataset licenses and access conditions apply separately.
