# 🚀 RISC-V EDA Toolchain Installation Report

**Prepared By:** Paidipilli Purushotham
**Date:** September 20, 2025

---

### 🎯 **Objective**

This document serves as a comprehensive log and proof of the successful installation of the essential open-source Electronic Design Automation (EDA) toolchain for the **RISC-V SoC Tapeout Program**. Each tool's installation is detailed, followed by a verification snapshot.

---

### 💻 **System Specifications**

The entire toolchain was installed and configured on a system with the following key specifications:

-   🧠 **RAM:** 6 GB
-   💿 **Storage:** 50 GB
-   🖥️ **Operating System:** Ubuntu 20.04 (or higher)
-   ⚙️ **CPU:** 4 vCPUs

---

### ✅ **Installation & Verification Log**

The following sections detail the commands executed for each tool and provide dedicated space for verification screenshots.

#### **Tool 1: 🔬 Yosys (Synthesis Tool)**

Yosys, the core synthesis framework, was compiled and installed from its latest source code.

**📝 Commands Executed:**
```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git    //(https://github.com/YosysHQ/yosys.git)
cd yosys
sudo apt install make               # Ensure 'make' is available
sudo apt-get install -y build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
git submodule update --init --recursive # Crucial step for 'abc'
make 
sudo make install
````

**✔️ Yosys Verification Snapshot:**
Installation confirmed by running `yosys -v`.

> 📸 <img width="1301" height="403" alt="Image" src="https://github.com/user-attachments/assets/8653bc96-b60a-474d-ab81-f7c6a783ecdf" />

-----

#### **Tool 2: ▶️ Icarus Verilog (`iverilog`) (Simulator)**

Icarus Verilog, the RTL simulator, was installed directly via the package manager.

**📝 Commands Executed:**

```bash
sudo apt-get update
sudo apt-get install iverilog
```

**✔️ Icarus Verilog Verification Snapshot:**
Installation confirmed by running `iverilog -v`.

> 📸 <img width="1309" height="563" alt="Image" src="https://github.com/user-attachments/assets/42058c2a-a4fc-4d39-b29f-307039f3ca18" />

-----

#### **Tool 3: 📈 GTKWave (Waveform Viewer)**

GTKWave, for visualizing simulation waveforms, was installed via the package manager.

**📝 Commands Executed:**

```bash
sudo apt-get update
sudo apt install gtkwave
```

**✔️ GTKWave Verification Snapshot:**
Installation confirmed by running `gtkwave`.

> 📸 <img width="1298" height="114" alt="Image" src="https://github.com/user-attachments/assets/3d4ccd62-6a6c-4231-a887-5fb580d07840" />

**GTKWave Interface Snapshot:**
> 📸 <img width="1295" height="734" alt="Image" src="https://github.com/user-attachments/assets/b39fd79c-a3db-4c08-b271-668973c7341e" />
-----

### 🎉 **Conclusion**

The full open-source EDA toolchain, comprising Yosys, Icarus Verilog, and GTKWave, has been successfully installed and thoroughly verified. The environment is now fully prepared for the subsequent design and implementation phases of the RISC-V SoC Tapeout Program.

```
```
