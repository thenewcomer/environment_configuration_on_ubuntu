# environment_configuration_on_ubuntu

How to quickly and successfull configure the environment of Ubuntu to make the Learning easier?
1. Environment need for running Pytorch on GPU
  -GPU driver
  -CUDA
  
  For the GPU Driver and CUDA version Match, please refer this page: https://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html
    Table 1. CUDA Toolkit and Compatible Driver Versions CUDA Toolkit 	Linux x86_64 Driver Version 	Windows x86_64 Driver Version
    CUDA 11.0.3 Update 1 	>= 450.51.06 	>= 451.82
    CUDA 11.0.2 GA 	>= 450.51.05 	>= 451.48
    CUDA 11.0.1 RC 	>= 450.36.06 	>= 451.22
    CUDA 10.2.89 	>= 440.33 	>= 441.22
    CUDA 10.1 (10.1.105 general release, and updates) 	>= 418.39 	>= 418.96
    CUDA 10.0.130 	>= 410.48 	>= 411.31
    CUDA 9.2 (9.2.148 Update 1) 	>= 396.37 	>= 398.26
    CUDA 9.2 (9.2.88) 	>= 396.26 	>= 397.44
    CUDA 9.1 (9.1.85) 	>= 390.46 	>= 391.29
    CUDA 9.0 (9.0.76) 	>= 384.81 	>= 385.54
    CUDA 8.0 (8.0.61 GA2) 	>= 375.26 	>= 376.51
    CUDA 8.0 (8.0.44) 	>= 367.48 	>= 369.30
    CUDA 7.5 (7.5.16) 	>= 352.31 	>= 353.66
    CUDA 7.0 (7.0.28) 	>= 346.46 	>= 347.62
  For the CUDA and Pytorch version Match, please see this page:
  https://pytorch.org/
  I think above cuda-9.2 now still can suport the lastest Pytorch version(1.6)
  
  For the GPU driver installation, many people don't 
  sudo add-apt-repository ppa:graphics-drivers/ppa  
  sudo apt-get update
  sudo apt-get install nvidia-xxx(nvidia-418)
  sudo reboot
  
  After the installation, chekc the installed GPU driver version:
  grep "X Driver" /var/log/Xorg.0.log
  
  Then install CUDA, still, don't use the .run file,  recommend to use the .deb file
  For example, when I am doing the installation I choose Driver 418 and CUDA-10.0, so I use these commands to install cuda:
  https://developer.nvidia.com/cuda-10.0-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1604&target_type=deblocal
  After the installation of the CUDA, reboot your engine to make your life easier. Or you may encounter some problems when you type nvidia-smi. 
  
  Then we can start to install Pytorch. 
  
  
  
  
