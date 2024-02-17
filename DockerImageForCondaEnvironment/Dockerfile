# docker build -t lwc-python-linux:2 .
# winpty docker run --gpus all -it lwc-python-linux:2
FROM mcr.microsoft.com/azureml/openmpi4.1.0-cuda11.8-cudnn8-ubuntu22.04
WORKDIR /lwc_docker
COPY conda.yml .
RUN conda init
RUN conda env create -f conda.yml
RUN echo "conda activate lwc_python" >> ~/.bashrc