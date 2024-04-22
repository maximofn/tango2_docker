# Tango 2 docker

Dockerization of the [Hugging Face Tango 2 Space](https://huggingface.co/spaces/declare-lab/tango2)

 * Paper: [Tango 2: Aligning Diffusion-based Text-to-Audio Generations through Direct Preference Optimization](https://arxiv.org/abs/2404.09956)
 * Model card: [declare-lab/tango2](https://huggingface.co/declare-lab/tango2)
 * Space: [declare-lab/tango2](https://huggingface.co/spaces/declare-lab/tango2)

## Requisites

[Docker](https://docs.docker.com/desktop/) and [nvidia container toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html) must be installed.

## Usage

### Download the image from the Docker Hub

You can download the image and run it

```bash
docker pull maximofn/tango2:latest
./run_app.sh
```

### Build the image

Or you can build the image and run it

```bash
./build_docker_image.sh
./run_app.sh
```
