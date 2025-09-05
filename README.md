# E-Science Tutorial

## Title: Large-scale Workflow Provenance Data Management in the AI Lifecycle using Flowcept

## Abstract. 

Developing large and complex AI models—such as large language models (LLMs)—that require high-performance computing (HPC) systems is a human-driven, resource-intensive process. AI scientists must continuously balance model accuracy with computational efficiency while navigating a vast and complex design space, where small adjustments to architecture, hyperparameters, or datasets can yield marginal accuracy gains at the cost of disproportionately large increases in computational expense. This challenge is further complicated by the need to integrate and analyze multiple interconnected workflows—including data preparation, training, evaluation, and inference phases—across the AI lifecycle. Workflow provenance techniques have demonstrated high potential to address such complexity. However, existing tools are often not tailored to the needs of HPC systems: they either impose high overheads or can only focus narrowly on a single aspect, neglecting the broader, multi-level nature of the AI lifecycle.

This tutorial introduces Flowcept, a data-centric framework that leverages workflow provenance for lifecycle-aware data analysis of AI workflows. Flowcept provides a broad, unified data view across the phases of the AI model development lifecycle, allowing for in-depth, runtime monitoring of computationally intensive phases, such as training large-scale models that require HPC. Participants will gain hands-on experience with managing provenance with Flowcept in a variety of AI workloads, including the development of LLMs. We will explore the types of provenance data at multiple levels, including workflow, task, model, and layer, as well as resource consumption data (e.g., GPU, storage). We will also provide practical guidance on processing collected data, analyzing it interactively with Jupyter Notebooks, and monitoring it in real time with Grafana. By the end of the tutorial, participants will be able to use collected data for reproducibility, end-to-end queries, and tradeoff analysis between model performance and resource utilization on HPC.

## Organizers:
- Amal Gueroudji (ANL) agueroudji@anl.gov – Contact person
- Renan Souza (ORNL) souzar@ornl.gov– Contact person
- Daniel Rosendo (ORNL) rosendod@ornl.gov
- Rafael Ferreira da Silva (ORNL) silvarf@ornl.gov
- Matthieu Dorier (ANL) mdorier@anl.gov

## Relevant website(s):
- Flowcept: https://github.com/ORNL/flowcept
- Running with Docker: https://github.com/ORNL/flowcept?tab=readme-ov-file#running-with-containers 
- Flowcept examples and notebooks: https://github.com/ORNL/flowcept/tree/main/notebooks
- Documentation: https://flowcept.readthedocs.org/

# Preparation Requirements

### Background Knowledge

- We expect the audience to be familiar with Python, Docker, and Docker Compose.
- Some familiarity with PyTorch models will be good to have.
- [W3C PROV](https://www.w3.org/TR/prov-overview/) terminology.

### Environment

- Python>=3.10+ with a fresh venv or conda environment. 
- Run this simple [example](https://github.com/ORNL/flowcept/blob/main/examples/start_here.py). Read the header message in that file to learn how to install & run Flowcept with minimum requirements.
- `make services-mongo` # This will download Redis and Mongo image.
- Optional extras for later sections as time allows: `pip install flowcept[dask,mlflow,mongo,telemetry]; pip install flowcept[ml_dev]`. 
- Optionally, get some familiarity with the [settings.yaml](https://github.com/ORNL/flowcept/blob/main/resources/sample_settings.yaml) file.
- Optionally, git clone the repository: https://github.com/ornl/flowcept and see the examples and notebooks directories.
