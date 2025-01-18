# Resisting Poisoning Attacks in Federated Learning via Dual-Domain Distance and Trust Assessment

This repository contains the project files and resources for the research paper titled **"Resisting Poisoning Attacks in Federated Learning via Dual-Domain Distance and Trust Assessment"**.

All experimental results and detailed analyses can be found in the following document:  
[Results PDF](https://github.com/Aquarids/Flmpid-pub/blob/main/doc/result.pdf)

A sample dataset for the Flmpid framework is provided for demonstration purposes. ~~You can download the example dataset file from the following link:  
[Example Dataset (RAR)](https://github.com/Aquarids/Flmpid-pub/blob/main/doc/example.rar)~~

The dataset file is too large to be hosted here. Please contact the maintainer for access.

## The File Structure
output_dir/
├── task_id/                     # If compare=True
│   └── clients_params.h5        # Client parameters
│   └── global_params.h5         # Global parameters
└── dist/attack/results_task_id/ # Default directory (if compare=False)
    └── clients_params.h5        # Client parameters
    └── global_params.h5         # Global parameters

### `clients_params.h5`

- **Description**: Stores parameters for each client in a federated learning setup.
- **Contains**:
  - Model weights for each client (`weights`).
  - Model updates for each client (`updates`).
  - Client attributes:
    - `tag`: Unique identifier for the client.
    - `type`: Indicates if the client is malicious (`True` or `False`).
    - `workload`: Workload assigned to the client.

### `global_params.h5`

- **Description**: Stores global model parameters in a federated learning setup.
- **Contains**:
  - Global model weights before aggregation (`before_weights`).
  - Global model weights after aggregation (`after_weights`).
  - Base updates applied to the global model (`base_updates`).
  - Global model attribute:
    - `base_workload`: Base workload of the global model.