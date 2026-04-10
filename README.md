# 📡 Bandwidth Measurement using Mininet & iperf

## 📌 Overview

This project demonstrates how to measure network bandwidth using Mininet. Different network topologies are created and tested using the `iperf` tool to observe throughput between hosts.

---

## 🎯 Objective

* Create virtual networks using Mininet
* Test connectivity using ping
* Measure bandwidth using iperf
* Demonstrate working network behavior

---

## 🛠️ Tools Used

* Ubuntu (WSL)
* Mininet
* Open vSwitch
* iperf

---

## ⚙️ Setup Steps

```bash
sudo apt update
sudo apt install mininet -y
sudo apt install openvswitch-switch -y
sudo apt install iperf -y
```

---

## 🌐 Topology 1: Linear

### Run:

```bash
sudo mn --topo linear,2
```

### Test Connectivity:

```bash
pingall
```

### Run Bandwidth Test:

```bash
h1 iperf -s &
h2 iperf -c h1
```

---

## 🌐 Topology 2: Single Switch

### Run:

```bash
sudo mn --topo single,3
```

### Test:

```bash
pingall
```

### Run:

```bash
h1 iperf -s &
h3 iperf -c h1
```

---

## 🌐 Topology 3: Tree

### Run:

```bash
sudo mn --topo tree,depth=2,fanout=2
```

### Check Nodes:

```bash
nodes
```

### Test:

```bash
pingall
```

### Run:

```bash
h1 iperf -s &
h4 iperf -c h1
```

---

## 📸 Output Screenshots

### 🔹 Linear Topology

<img width="239" height="85" alt="image" src="https://github.com/user-attachments/assets/f88315ab-8f51-43b9-9284-346d72f4ff92" />
<img width="745" height="226" alt="image" src="https://github.com/user-attachments/assets/82f0026a-f248-49a9-941b-079e6d333b84" />



### 🔹 Single Topology

 <img width="683" height="199" alt="image" src="https://github.com/user-attachments/assets/1719edbd-d22b-468b-b632-fdb0cafdc00b" />


### 🔹 Tree Topology
<img width="392" height="134" alt="image" src="https://github.com/user-attachments/assets/14c1a283-994d-4c24-9124-68221a80a67b" />

<img width="918" height="269" alt="image" src="https://github.com/user-attachments/assets/e52bc3a7-94c4-47af-8fd4-2bbf26fd6a8a" />




---

## 📂 Commands Used

```bash
sudo mn --topo linear,2
h1 iperf -s &
h2 iperf -c h1

sudo mn --topo single,3
h1 iperf -s &
h3 iperf -c h1

sudo mn --topo tree,depth=2,fanout=2
h1 iperf -s &
h4 iperf -c h1
```

---

## 📚 Conclusion

This project successfully demonstrates bandwidth measurement in different network topologies using Mininet and iperf.

---



