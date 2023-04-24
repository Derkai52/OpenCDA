# Docker Deployment Configuration

## Server Configuration
Make sure your computer is connected to the `The Real Internet`   beforehand, as there are some relatively large packages that need to be downloaded during the build process.

The image build also includes `Carla` and `SUMO` components for optional installation (installed by default)

For more information about the configuration of the docker image, see
[Dockerfile](Dockerfile)  

### Install Vulkan SDK
[Download the Vulkan SDK](https://vulkan.lunarg.com/sdk/home#linux)
```shell
# Dependencies
sudo apt-get install cmake git gcc g++ mesa-* libwayland-dev libxrandr-dev
sudo apt-get install libvulkan1 mesa-vulkan-drivers vulkan-utils libxcb-keysyms1-dev
sudo apt-get install libxcb1-dev libx11-dev

# Download Vulkan SDK
mkdir vulkan && cd vulkan
wget -c https://sdk.lunarg.com/sdk/download/1.3.239.0/linux/vulkansdk-linux-x86_64-1.3.239.0.tar.gz
tar xf vulkansdk-linux-x86_64-1.3.239.0.tar.gz

# Compile
cd 1.3.239.0/source/shaderc
python3 update_shaderc_sources.py 
cd ../../ && bash vulkansdk

# Update Vulkan environment variables
source setup-env.sh

# Verify vulkan version
vulkaninfo
```

### Install NVIDIA-Docker Component
 1. [Install Docker](https://docs.docker.com/engine/install/) on your system.
 2. If you are using an Nvidia graphics card, [install the Nvidia Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html#installation-guide). It exposes your Nvidia graphics
 card to Docker containers.
 3. In the Dockerfile directory, run
 ```shell
 docker build -t opencda_container .
 ```
 4. Build Docker Container
 ```shell
 docker run --privileged --gpus all --network=host -e DISPLAY=$DISPLAY -v /usr/share/vulkan/icd.d:/usr/share/vulkan/icd.d -it opencda:latest /bin/bash
 ```


Note:
It is recommended that you restart your computer after completing the installation of the above two graphical interface components to ensure that it takes effect.

### Example
You can test some of the [examples provided by OpenCDA](https://opencda-documentation.readthedocs.io/en/latest/md_files/getstarted.html)

Note: You need to make sure that the `Carla server` is running.

## Local Client Configuration
Install the `Same Version` of the package component as on the `Server`.

### Python Env
**(option)**  It is highly recommended to use **Python environment management tools** such as `Conda` , It makes your expansion and development more concise.

```shell
# Download miniconda3
wget -c https://repo.anaconda.com/miniconda/Miniconda3-py38_23.1.0-1-Linux-x86_64.sh

# Install
sudo bash ./Miniconda3-py38_23.1.0-1-Linux-x86_64.sh

# Build Python Env
conda create -n opencda python=3.8

conda activate opencda

# Go to the root directory of the OpenCDA project
pip3 install -r requirements.txt
```
For more information about `Conda`, you can refer to [here](https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html)


## Remote Client Configuration
TODO

