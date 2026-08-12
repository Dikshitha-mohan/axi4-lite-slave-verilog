# AXI4-Lite Slave using Verilog HDL

## 📌 Project Overview

This project implements a simple **AXI4-Lite Slave interface** using Verilog HDL.

The design supports memory-mapped register read and write operations through the AXI4-Lite protocol. The project focuses on understanding AXI channels, VALID/READY handshaking, register mapping, response generation, and RTL verification.

This project is part of my **10-Project RTL Design Journey**.

---

## 🎯 Objectives

- Understand the AXI4-Lite communication protocol
- Implement AXI write transactions
- Implement AXI read transactions
- Implement VALID/READY handshaking
- Design memory-mapped registers
- Generate write responses
- Generate read responses
- Handle invalid addresses
- Verify RTL functionality using a testbench
- Analyze simulation waveforms

---

## 🧩 Block Diagram

### AXI4-Lite Slave Architecture

> **Add your block diagram image below this section.**

<br>

<img width="1536" height="1024" alt="axi_block_diagram" src="https://github.com/user-attachments/assets/ee814223-ca9b-436d-9aeb-2bf2d8620b18" />


<br>

---

## 🔹 AXI4-Lite Interface

### Write Address Channel

| Signal | Description |
|--------|-------------|
| AWADDR | Write address |
| AWVALID | Indicates valid address |
| AWREADY | Slave ready for address |

### Write Data Channel

| Signal | Description |
|--------|-------------|
| WDATA | Write data |
| WSTRB | Byte write enable |
| WVALID | Indicates valid data |
| WREADY | Slave ready for data |

### Write Response Channel

| Signal | Description |
|--------|-------------|
| BRESP | Write response |
| BVALID | Response is valid |
| BREADY | Master ready for response |

### Read Address Channel

| Signal | Description |
|--------|-------------|
| ARADDR | Read address |
| ARVALID | Indicates valid address |
| ARREADY | Slave ready for address |

### Read Data Channel

| Signal | Description |
|--------|-------------|
| RDATA | Read data |
| RRESP | Read response |
| RVALID | Data is valid |
| RREADY | Master ready for data |

---

## 🗂️ Register Map

| Address | Register | Description |
|--------:|----------|-------------|
| `0x0` | REG0 | 32-bit Read/Write Register |
| `0x4` | REG1 | 32-bit Read/Write Register |
| `0x8` | REG2 | 32-bit Read/Write Register |
| `0xC` | REG3 | 32-bit Read/Write Register |

---

## ⚙️ Design Features

- 32-bit data width
- 4-bit address width
- Four memory-mapped registers
- AXI4-Lite write interface
- AXI4-Lite read interface
- VALID/READY handshake mechanism
- Byte write enable using `WSTRB`
- Write response generation
- Read response generation
- Invalid address detection
- Active-low reset
- RTL-based implementation

---

## 🧪 Verification

A dedicated Verilog testbench was developed to verify the AXI4-Lite Slave.

### Write Tests

The following values are written into the registers:

```text
Address 0x0 → 12345678
Address 0x4 → AABBCCDD
Address 0x8 → DEADBEEF
Address 0xC → CAFEBABE



👨‍💻 Author

Dikshitha M

Electronics & Communication Engineering
RTL / VLSI Design Enthusiast

🔗 LinkedIn

https://www.linkedin.com/in/dikshitha-m-34355b308/
