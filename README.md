# 🌐 Hub and Spoke Network Architecture on Azure

## 🔰 Overview

The **Hub and Spoke Architecture** in Azure is a cloud networking design that enables centralized network management, security enforcement, and resource optimization. This architecture consists of a central **Hub Virtual Network (VNet)** that connects to one or more **Spoke VNets**, allowing streamlined communication, enhanced security, and scalable infrastructure deployment.

This project demonstrates the implementation of the Hub-and-Spoke model using Azure Firewall, Virtual Network Peering, Route Tables, and Network Security Groups (NSGs), ideal for modern enterprise cloud networking.

---

## 🚀 Project Objective

> “To centralize and secure the network infrastructure of a distributed IT environment using Azure’s Hub and Spoke model—enhancing control, visibility, and scalability.”

---

## 🧩 Architecture Design

### 🔸 Components

| Component | Name | IP Range | Description |
|----------|------|----------|-------------|
| Hub VNet | `aka-Vnetwork` | `10.0.0.0/16` | Centralized network for firewall and shared services |
| Spoke VNet 1 | `prod1-spoke-vnetwork` | `10.1.0.0/16` | VNet for workload 1 |
| Spoke VNet 2 | `prod2-spoke-vnetwork` | `10.2.0.0/16` | VNet for workload 2 |
| Subnet | `Each for Vnets` | — | Reserved for Azure Firewall |
| NetSecurityGroups | `For all Vnets` | — | Provide Security for The vnet |
| Azure Firewall | `aka-firewall` | — | Inspects and controls all traffic |
| VMs | `Spoke1-VM`, `Spoke2-VM` | — | For testing connectivity and firewall policies |

---

## ⚙️ Technologies Used

- Microsoft Azure
- Azure Virtual Networks
- Azure Firewall
- Network Security Groups (NSGs)
- Virtual Machines
- Route Tables (UDRs)
- Azure Resource Manager (ARM)

---

## 📋 Prerequisites

- Active [Azure Subscription](https://portal.azure.com/)
- Azure CLI or Azure Portal Access
- Contributor role or higher for resource creation
- Basic knowledge of VNets, subnets, NSGs, and firewalls

---

## 📐 Implementation Stages

### ✅ Stage 1: Deploying the Hub-Spoke Virtual Networks

### ✅ Stage 2: Creating Peering Between the Hub and Spoke Networks

### ✅ Stage 3: Creating the Azure Firewall Service

### ✅ Stage 4: Creating and Updating Routing Tables

### ✅ Stage 5: Deploying VMs in the Spoke Virtual Networks

### ✅ Stage 6: Updating Firewall Rules & NSG Rules

### ✅ Stage 7: Configuring a Site-to-Site VPN

---

## 🛠️ How to Run

1. **Login to Azure Portal** and create a new resource group.
2. **Create VNets**:
   - `HubVNet` with `AzureFirewallSubnet`
   - `SpokeVNet1` and `SpokeVNet2` with `WorkloadSubnet`
3. **Deploy Azure Firewall** in `HubVNet`.
4. **Create VNet Peering** between Hub and each Spoke.
5. **Deploy VMs** in Spokes for connectivity testing.
6. **Configure Route Tables** to route all traffic from Spokes through the Azure Firewall.
7. **Add NSGs** to limit public access and allow only specific traffic.
8. **Set Firewall Rules**:
   - Allow RDP/SSH from admin IP
   - Deny internet except specific whitelisted URLs/IPs

---

## 🧪 Testing and Validation

- ✅ Ping from Spoke1 VM to Spoke2 VM (via Hub)
- ✅ Test RDP/SSH access via Firewall
- ✅ Verify NSG and UDR enforcement
- ✅ Check Firewall Logs in Azure Monitor
- ✅ Block unauthorized internet access

---

## 📊 Monitoring & Logs

- Azure Monitor: Diagnostic Settings enabled for Firewall, NSGs
- Network Watcher: Packet capture, topology, and connection troubleshoot enabled
- Log Analytics Workspace connected for deep inspection

---

## ✅ Outcome

- 🎯 Centralized security via Azure Firewall
- 🔐 Controlled traffic routing using UDRs and NSGs
- 🌐 Secure and scalable network for multi-region, multi-tenant deployment
- 📡 Full monitoring visibility using Azure-native tools

---

## 📚 References

- [Hub and Spoke Model – Microsoft Learn](https://learn.microsoft.com/en-us/azure/architecture/networking/architecture/hub-spoke?tabs=cli)
- [Shruti Pal - Medium Blog](https://medium.com/@shrutipal700/hub-and-spoke-architecture-on-azure-23f86f05c299)
- [How to Create Hub-and-Spoke with Virtual Network Manager](https://learn.microsoft.com/en-us/azure/virtual-network-manager/how-to-create-hub-and-spoke)

---

## 🏁 Author

**Akash Shinde**  
Celebal Summer Internship | DevOps | CT_CSI_DV_4920
Email: akashshide2601@email.com 
GitHub: https://github.com/akascaptain

---
