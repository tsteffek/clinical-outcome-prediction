FROM pytorch/pytorch:1.8.1-cuda11.1-cudnn8-devel

ENV PYTHONIOENCODING=utf-8
ENV SKLEARN_ALLOW_DEPRECATED_SKLEARN_PACKAGE_INSTALL=True

WORKDIR /experiments/
COPY requirements.txt .

RUN pip install --no-cache -r requirements.txt

COPY configs/ ./configs/
COPY custom_models/ ./custom_models/

COPY utils.py .
COPY doc_classification.py .
COPY hpo_doc_classification.py .
COPY outcome_pretraining.py .
COPY metrics.py .
