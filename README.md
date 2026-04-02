# 🛡️ Azure Cloud VM Metadata Enumerator (Metasploit Module)

---

## 📖 Overview

This is a **Custom Metasploit Auxiliary Module** developed to perform post-exploitation reconnaissance on **Azure Cloud Infrastructure**.
The module targets the **Azure Instance Metadata Service (IMDS)** to extract sensitive metadata about a Virtual Machine from an internal perspective.

---

## ✨ Key Features (Information Gathered)

* **VM Identification:** Virtual Machine Name & Unique Instance ID
* **Network Infrastructure:** Public & Private IP Addresses
* **Geographical Data:** Azure Region / Location
* **System Specs:** VM Size (SKU) & Operating System details

---

## 🚀 Deployment & Installation (Kali Linux)

### 1️⃣ Install Required Ruby SDK

```bash
sudo gem install azure_mgmt_compute
sudo gem install azure_mgmt_resources
```

---

### 2️⃣ Module Directory Setup

```bash
# Navigate to the auxiliary modules directory
cd /usr/share/metasploit-framework/modules/auxiliary/

# Create a custom category folder
sudo mkdir cloudy

# Copy the module file
sudo cp azure_vm_enum.rb /usr/share/metasploit-framework/modules/auxiliary/cloudy/
```

---

### 3️⃣ Reload Metasploit

```bash
msfconsole
msf6 > reload_all
```

---

## 🛠️ Usage & Execution

```bash
# Select module
msf6 > use auxiliary/cloudy/azure_vm_enum

# Set target
msf6 auxiliary(cloudy/azure_vm_enum) > set RHOSTS <Target_IP>

# Run
msf6 auxiliary(cloudy/azure_vm_enum) > run
```

---

## 📊 Proof of Concept (PoC)

*Add your screenshot here*

```md
![Result](./Screenshots/your-image.png)
```

---

## 👨‍💻 Author

**Naeem Akmal**
BS Computer Science – University of Lahore

* GitHub: https://github.com/NaeemAkmal
* LinkedIn: https://linkedin.com/in/naeem-akmal-483282306

---

## ⚠️ Disclaimer

This tool is for **educational purposes** and **authorized testing only**.
Unauthorized use is illegal.
