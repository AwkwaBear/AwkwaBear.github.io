
>- ***NOTE: Needs to use WSL to get a linux backend for colab, or else all escaped terminal commands will need to be rewritten for windows equivalents. The best way to achieve this is with google's provided colab Docker image***
> - ## Install WSL Ubuntu
> - ## Set up Docker and Nvidia CUDA GPU support for WSL
	- Following (https://docs.nvidia.com/ai-enterprise/deployment-guide-vmware/0.1.0/docker.html)
		- Install docker:
			- https://docs.docker.com/engine/install/ubuntu/
		- Install Nvidia Container Toolkit
			- https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#installing-the-nvidia-container-toolkit
			- Do the Configure Docker section
				- https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#configuring-docker
	- `sudo docker run --gpus=all -p 127.0.0.1:9000:8080 us-docker.pkg.dev/colab-images/public/runtime`
	- copy given URL for localhost runtime
		- i.e `http://127.0.0.1:9000/?token=81bbec4a35d137775a6b3e1304ccb36110616b9bc3f7fbde`
> - Open Google Colab
> - Click Down arrow next to "Connect" in upper right corner
> - Connect To local runtime
> - Paste copied local runtime into field
> - Colab notebook can now run locally