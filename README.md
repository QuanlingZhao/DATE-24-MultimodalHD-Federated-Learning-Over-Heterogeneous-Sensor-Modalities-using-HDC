# MultimodalHD: Federated Learning Over Heterogeneous Sensor Modalities using Hyperdimensional Computing [DATE'24]

Code for the DATE 2024 paper: MultimodalHD: Federated Learning Over Heterogeneous Sensor Modalities using Hyperdimensional Computing

## Overview

MultimodalHD combines hyperdimensional computing (HDC), attention-based multimodal fusion, and federated learning to support clients with heterogeneous sensor modalities.

Supported datasets:

- HAR
- MHEALTH
- Opportunity (OPP)

## Repository Structure

```text
MultimodalHD/
├── configs/
├── src/
├── run.py
└── run.bat

data/
├── har/
├── mhealth/
└── opp/
```

## Requirements

```bash
pip install numpy scipy pandas scikit-learn matplotlib seaborn torch
```

## Data

The preprocessed `.mat` files used by the original experiments are available here:

https://drive.google.com/drive/folders/16q46GZiVYXgXBGvh36ApS8u_GJiyOaBz

Place the corresponding dataset file under `data/har/`, `data/mhealth/`, or `data/opp/`, then run the provided partition script inside each dataset's `*_client/` directory.

Example:

```bash
cd data/har/har_client
python partition_har_client_data.py
```

## Run Experiments

From the `MultimodalHD` directory:

```bash
mkdir results

python run.py configs/har.config
python run.py configs/mhealth.config
python run.py configs/opp.config
```

The provided config files contain the experiment settings used by the released implementation.
