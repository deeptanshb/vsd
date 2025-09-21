
# RISC-V Reference SoC Tapeout Program VSD

## Tools Installation

#### <ins>All the instructions for installation of required tools can be found here:</ins>

### **System Requirements**
- 6 GB RAM
- 50 GB HDD
- Ubuntu 20.04 or higher
- 4 vCPU



### **TOOL CHECK**

#### <ins>**Yosys**</ins>
```bash
$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make               # If make is not installed
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
# Yosys build depends on a Git submodule called abc, which hasn't been initialized yet. You need to run the following command before running make
$ git submodule update --init --recursive
$ make 
$ sudo make install
```
<img width="797" height="279" alt="Screenshot from 2025-09-21 03-11-43" src="https://github.com/user-attachments/assets/b6881f45-f9f9-4828-ab14-09ee17609e4c" />


#### <ins>**Iverilog**</ins>
```bash
$ sudo apt-get update
$ sudo apt-get install iverilog
```
<img width="786" height="675" alt="Screenshot from 2025-09-21 03-22-12" src="https://github.com/user-attachments/assets/100f0312-0002-4151-a79e-b4ac588a3e87" />


#### <ins>**gtkwave**</ins>
```bash
$ sudo apt-get update
$ sudo apt install gtkwave
```
<img width="775" height="91" alt="image" src="https://github.com/user-attachments/assets/49ec6f5b-2bf0-4f23-a1f8-5092ef3638e1" />

#### <ins>**Ngspice**</ins>
```bash
$ tar -zxvf ngspice-37.tar.gz
$ cd ngspice-37
$ mkdir release && cd release
$ ../configure --with-x --with-readline=yes --disable-debug
$ make
$ sudo make install
```
<img width="806" height="260" alt="Screenshot from 2025-09-21 03-29-49" src="https://github.com/user-attachments/assets/eb04d383-d026-47d7-b776-8172ddb7cb75" />

#### <ins>**Magic**</ins>
```bash
$ sudo apt install -y m4 tcsh csh libx11-dev tcl-dev tk-dev \
  libcairo2-dev mesa-common-dev libglu1-mesa-dev libncurses-dev

$ git clone https://github.com/RTimothyEdwards/magic
$ cd magic
$ ./configure
$ make
$ sudo make install
```
<img width="833" height="80" alt="Screenshot from 2025-09-21 03-36-59" src="https://github.com/user-attachments/assets/87b9b235-a45a-43e5-a041-1104437ffa08" />

#### <ins>**Docker**</ins>
```bash
$ sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
  sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

$ echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] \
$ https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
$ sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

$ sudo apt update
$ sudo apt install -y docker-ce docker-ce-cli containerd.io

$ sudo docker run hello-world
```
<img width="833" height="619" alt="Screenshot from 2025-09-21 03-43-39" src="https://github.com/user-attachments/assets/a4cb50a1-3cf0-4f38-8348-63579dace989" />

#### <ins>**OpenLane**</ins>
```bash
$ sudo apt update && sudo apt upgrade -y
$ sudo apt install -y build-essential python3 python3-venv python3-pip make git

$ cd $HOME
$ git clone https://github.com/The-OpenROAD-Project/OpenLane
$ cd OpenLane
$ make
$ make test
```
<img width="1246" height="990" alt="Screenshot from 2025-09-21 18-45-40" src="https://github.com/user-attachments/assets/0edf35f5-afec-49f2-b438-0671a2be7e3b" />

