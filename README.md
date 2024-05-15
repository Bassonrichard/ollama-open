# Ollama

## Getting Started

### Prerequisites

- Docker
- Docker Compose
- Nvidia Container Toolkit (Optional)
- Nvidia GPU (Optional)

### GPU Acceleration

Install the Nvidia toolkit to enable GPU acceleration.

#### Nvidia container toolkit

[Nvidia container toolkit docs ](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#installation)

1. Get the GPG keys

    ```bash
    curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg \
    && curl -s -L https://nvidia.github.io/libnvidia-container/stable/deb/nvidia-container-toolkit.list | \
        sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | \
        sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list
    ```
2. Update packages

    ```bash
    sudo apt-get update

    ```
3. Install the NVIDIA Container Toolkit packages

    ```bash
    sudo apt-get install -y nvidia-container-toolkit
    ```

### Running the the compose file 

```bash
docker compose up -d
```

