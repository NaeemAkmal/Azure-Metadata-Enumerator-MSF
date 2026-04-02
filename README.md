🛡️ Azure Cloud VM Metadata Enumerator (Metasploit Module)
📖 Overview
This is a Custom Metasploit Auxiliary Module developed to perform post-exploitation reconnaissance on Azure Cloud Infrastructure. The module specifically targets the Azure Instance Metadata Service (IMDS) to extract sensitive metadata about a Virtual Machine from an internal perspective.

✨ Key Features (Information Gathered)
The module automates the extraction of the following critical data points:

VM Identification: Virtual Machine Name & Unique Instance ID.

Network Infrastructure: Public & Private IP Addresses.

Geographical Data: Specific Azure Region/Location of the resource.

System Specs: VM Size (SKU) and Operating System details.

🚀 Deployment & Installation (Kali Linux)
1. Install Required Ruby SDK
The module utilizes Azure-specific Ruby libraries to parse cloud metadata. Install them using the following commands:

Bash
sudo gem install azure_mgmt_compute
sudo gem install azure_mgmt_resources
2. Module Directory Setup
Create a dedicated directory within the Metasploit framework and move the module file:

Bash
# Navigate to the auxiliary modules directory
cd /usr/share/metasploit-framework/modules/auxiliary/

# Create a custom category folder
sudo mkdir cloudy

# Copy the module file (azure_vm_enum.rb) into this folder
sudo cp azure_vm_enum.rb /usr/share/metasploit-framework/modules/auxiliary/cloudy/
3. Initialize & Reload Metasploit
Launch the Metasploit console and force a reload of the module database:

Bash
msfconsole
msf6 > reload_all
🛠️ Usage & Execution
Once the module is loaded, configure the target parameters and execute the scan:

Bash
# Select the custom module
msf6 > use auxiliary/cloudy/azure_vm_enum

# Set the Target IP (Azure VM Internal/Public IP)
msf6 auxiliary(cloudy/azure_vm_enum) > set RHOSTS <Target_IP>

# Execute the enumeration
msf6 auxiliary(cloudy/azure_vm_enum) > run
📊 Proof of Concept (PoC)
The following output demonstrates a successful metadata extraction from a target instance:

👨‍💻 Author
Naeem Akmal

Computer Science Student | The University of Lahore

Focus: Offensive Security & Infrastructure Hardening (Purple Teaming)

GitHub: github.com/NaeemAkmal

LinkedIn: linkedin.com/in/naeemakmal15

⚠️ Disclaimer
This tool is intended for educational purposes and authorized security auditing only. Unauthorized access to cloud infrastructure is illegal.

Naeem bhai, bas isay copy karke paste karein. Ab ye bilkul professional headings aur boxes ke saath nazar aaye ga!
