FROM nvcr.io/nvidia/cuda:11.8.0-cudnn8-devel-ubuntu22.04

RUN apt-get update \
    && apt-get install -y git git-lfs python3 python3-pip \
    && curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | bash \
    && git lfs install \
    && rm cuda-keyring_1.0-1_all.deb \
    && ln -s /usr/bin/python3 /usr/bin/python \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install --no-cache-dir torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118 \
    && git clone --depth 1 https://huggingface.co/spaces/declare-lab/tango2 \
    && cd tango2 && pip3 install --no-cache-dir -r requirements.txt \
    && sed -i '/def gradio_generate/a\    if not guidance: guidance = 3\n    if not steps: steps = 100' app.py

WORKDIR /tango2