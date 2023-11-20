## Linux building

1. Install libgmp-dev
2. Install CUDA 11.0
 
 - Or pass them as variables to `make` command.
 - Install libgmp: ```sudo apt install -y libgmp-dev```


    ```make
    CUDA       = /usr/local/cuda-11.0
    CXXCUDA    = /usr/bin/g++
    ```
 - To build CPU-only version (without CUDA support):
    ```sh
    $ make all
    ```
 - To build with CUDA: pass CCAP value according to your GPU compute capability
    ```sh
    $ cd Rotor-Cuda
    $ make gpu=1 CCAP=75 all
    ```

