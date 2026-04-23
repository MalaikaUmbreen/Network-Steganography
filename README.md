# 🔍 A Transformer-Based Detector for Network Steganography

##  Overview

This project presents a deep learning–based approach to detect **network steganography** using a **Transformer architecture**. The system analyzes network traffic behavior and identifies covert communication hidden within standard protocols such as **ICMP, TCP, UDP, and DNS**.

The goal is to enhance cybersecurity by detecting hidden data exfiltration techniques that bypass traditional security mechanisms.


<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/92a7f334-8dbc-41f2-b12f-4e7cddc74ebe" />


---

##  Key Features

* 🔹 Detection of covert network traffic
* 🔹 Supports multiple protocols: **ICMP, TCP, UDP, DNS**
* 🔹 Transformer-based deep learning model
* 🔹 Flow-level feature extraction (225+ features)
* 🔹 Binary classification (Normal vs Covert)
* 🔹 Multi-class classification of steganography techniques:

  * Header Manipulation
  * Timing Obfuscation
  * Flow Blending

---

## Project Architecture

### 🔄 Workflow

<img width="1089" height="738" alt="image" src="https://github.com/user-attachments/assets/33e20248-3d51-4b75-a125-fd4509373ecb" />

1. **Data Generation (Lab Setup)**

   * Covert traffic generated using tools (e.g., ptunnel, dnscat2)
   * Normal traffic collected from regular applications

<img width="546" height="368" alt="image" src="https://github.com/user-attachments/assets/a0d734df-936d-48f2-a23c-63ca259064b2" />

2. **Data Collection**

   * Packet capture using Wireshark
   * Traffic aggregation into flow-based datasets

<img width="1091" height="718" alt="image" src="https://github.com/user-attachments/assets/d719e807-da53-4a2f-afa4-93d6833708a8" />

3. **Feature Categorization**

   * Three Covert Techniques Features
   * Header Manipulation, Flow Blending , Timing Obfuscation
   * 225 Input features total
   * Three labels (label_technique, label_protocol , label_binary)
     
<img width="1092" height="725" alt="image" src="https://github.com/user-attachments/assets/3a68f9f3-61c7-4faa-bbe2-f427da5ce9aa" />


4. **Preprocessing Pipeline**

   * Data Cleaning (remove duplicates, missing values)
   * Feature Scaling (StandardScaler)
   * Label Encoding
   * Train/Test Split (80/20)
   * Tensor Conversion (PyTorch/TensorFlow)

<img width="1088" height="715" alt="image" src="https://github.com/user-attachments/assets/532a012d-a84b-4ad9-9505-d82c281f12fb" />
     

5. **Model Development**

   * Transformer-based architecture
   * Multi-head attention mechanism
   * Behavioral learning from network flows

<img width="1320" height="1860" alt="image" src="https://github.com/user-attachments/assets/7b1cd56e-9aa8-45db-b3cd-c799f7de9d55" />


6. **Evaluation**

   * Accuracy, Precision, Recall, F1-score
   * Confusion Matrix

<img width="734" height="361" alt="image" src="https://github.com/user-attachments/assets/71a8f39d-27a9-42fe-b5eb-5544e840b318" />

---

## 🏗️ System Design

**Pipeline Flow:**

Attacker → Covert Traffic Generation → Network Channel (ICMP | TCP | UDP | DNS) → Organization Network → SOC Monitoring → Transformer-Based Detector → Output (Normal / Covert + Technique Classification)

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/9540f4ca-028e-4fea-b314-f09bb0d9e9ab" />

---

## Dataset Details

* Total Features: **228**


<img width="572" height="148" alt="image" src="https://github.com/user-attachments/assets/d5e407de-5e27-4adc-ab16-fe8d0a114c32" />


  * Input Features: **225**
  * Label Columns: **3**
* Protocols Included:

  * ICMP
  * TCP
  * UDP
  * DNS

<img width="544" height="364" alt="image" src="https://github.com/user-attachments/assets/c053c809-0d3b-4fc7-906b-7ad49765b8f2" />

---

## Technologies Used

* Python 
* PyTorch / TensorFlow
* Scikit-learn
* Wireshark
* kali-linux
* Ubuntu-VM
* Scapy (Packet manipulation)
* NumPy & Pandas


---

## 📂 Project Structure

```
├── data/
│   ├── raw/
│   ├── processed/
├── notebooks/
├── models/
├── src/
│   ├── preprocessing.py
│   ├── model.py
│   ├── training.py
│   └── evaluation.py
├── results/
├── diagrams/
├── README.md
```

---
---

---

## 📈 Results

* Achieved high accuracy in detecting covert traffic
* Successfully classified different steganography techniques
* Demonstrated effectiveness of Transformer models in cybersecurity

 <img width="1128" height="502" alt="image" src="https://github.com/user-attachments/assets/ed8fffe2-8fc7-40eb-9401-a9a9ef2debe5" />
 

---

## Applications

* Network Intrusion Detection Systems (NIDS)
* Security Operations Centers (SOC)
* Data Exfiltration Detection
* Enterprise Network Security

---

## Future Work

* Real-time deployment in SOC environments
* Integration with SIEM tools (e.g., Wazuh)
* Hybrid models (CNN + Transformer)
* Larger real-world datasets
* More Covert techniques used

---

##  Author

**Malaika Umbreen**
BS Information Technology – Final Year
Research Area: Cybersecurity & Artificial Intelligence

---

## 📜 License

This project is for Academic and Research purposes.

---
