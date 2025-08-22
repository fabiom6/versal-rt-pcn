# VersalEdge-GNNs: Accelerating Point Cloud Networks for Real-Time Particle Physics
Particle accelerators produce extremely large amounts of data, making it infeasable to save data for each collision event happening in the accelerator. 
To deal with this constraint, particle accelerators use a multi-tiered trigger system to decide wether or not an event is interesting enough to keep for further analysis. The first of these triggers, the so called level 1 trigger is implemented in hardware to ensure compliance with the strict throughput and latency requirements. 

## Previous Work
**TODO** INSERT CITATIONS FOR MARC PAPER, TILL THESIS

## Hardware Requirements
This project is designed to run on the AMD Versal™ VCK190 Evaluation Kit, as well as second computer (in our case a Raspberry Pi 3B+) to run the visualization.
The Versal board and the visualization computer need to be connected to the same network.

## Software Requirements
- Python 3.11.6
- Vitis 2024.2

## Project Structure
<img src="https://github.com/user-attachments/assets/c2d94b17-88a5-4ce7-b181-c7c418e165f5" width=50% />

- [ext](https://github.com/fabiom6/versal-rt-pcn/tree/main/ext): Contains external libraries
- [fpga](https://github.com/fabiom6/versal-rt-pcn/tree/main/fpga): Contains the hardware accelerator
- [visualization](https://github.com/fabiom6/versal-rt-pcn/tree/main/visualization): Contains the Python visualization of the ECL

## Setup

1. **Clone the repository**
    ```bash
    git clone --recurse-submodules <repository_url>
    cd <repository_url>
    ```
1. **Setup the environment**
    ```bash
    source <Vitis_install_path>/Vitis/<version>/settings64.csh
    setenv PLATFORM_REPO_PATHS $XILINX_VITIS/base_platforms
    source visualization/vis_venv/bin/activate
    ```
1. **Build the hardware (TODO)**
    ```bash
    make hardware
    ```
1. **Build the host executable (TODO)**
    ```bash
    make host
    ```
1. **Write binaries to board (TODO)**
    ```bash
    TODO
    ```
1. **Prepare the visualization (TODO)**
    ```bash
    python visualization/build_mesh.py
    ```
1. **Run the demonstrator (TODO)**
    ```bash
    chmod +x demonstrator.sh
    ./demonstrator.sh
    ```

## Results
