## Installing the NVIDIA Container Toolkit and NVIDIA Docker 2

https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#installing-with-apt


# Installing with Apt
```bash
curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg \
  && curl -s -L https://nvidia.github.io/libnvidia-container/stable/deb/nvidia-container-toolkit.list | \
    sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | \
    sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list


sudo apt-get update

sudo apt-get install -y nvidia-container-toolkit nvidia-docker2
```


### docker info | grep -i runtime
 Runtimes: io.containerd.runc.v2 nvidia runc
 Default Runtime: runc


# Commands to interact with nvidia gpu
# nvidia-smi -l 1
This will refresh the GPU usage statistics every second, showing memory usage, processes running on the GPU, and more

# Grafana Dashboard
https://grafana.com/grafana/dashboards/12239-nvidia-dcgm-exporter-dashboard/
