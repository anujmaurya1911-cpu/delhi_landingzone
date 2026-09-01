# 🌐 Delhi Landing Zone 🚀

Welcome to the **Delhi Landing Zone** repository! This project manages Azure Cloud Infrastructure as Code (IaC) using **Terraform**, providing a scalable, secure, and automated foundation for cloud workloads. ☁️🛡️

---

## 📑 Table of Contents

- [📌 Overview](#-overview)
- [🏗️ Infrastructure & Resources](#️-infrastructure--resources)
- [📂 Project Structure](#-project-structure)
- [📋 Prerequisites](#-prerequisites)
- [⚡ Quick Start Guide](#-quick-start-guide)
- [🛠️ Terraform Workflow](#️-terraform-workflow)
- [🔐 Best Practices](#-best-practices)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 📌 Overview

The **Delhi Landing Zone** serves as the baseline environment for deploying cloud services in Azure. It leverages Terraform to automate provisioning, enforce naming conventions, maintain consistent tagging, and enable seamless environment scaling. 🏢✨

### 🌟 Key Highlights:
- ⚡ **Automated Provisioning:** Infrastructure declared as code for repeatable deployments.
- 📍 **Multi-Region Ready:** Defaulted to `Central India` 🇮🇳.
- 🔒 **Security First:** Consistent resource grouping and access isolation.

---

## 🏗️ Infrastructure & Resources

The landing zone currently manages the following Azure components:

| 🏷️ Resource Type | 🏷️ Resource Name | 📍 Location | 📄 File Reference |
| :--- | :--- | :--- | :--- |
| `azurerm_resource_group` | `abc` | `central india` | [`rg.tf`](file:///d:/devops%20_batch%2018/delhi_landingzone/rg.tf) |

---

## 📂 Project Structure

```bash
📦 delhi_landingzone
├── 📄 .gitignore        # Git ignore rules for Terraform & IDE files 🙈
├── 📄 rg.tf             # Resource Group definitions 🏛️
└── 📄 README.md         # Project documentation & guidelines 📖
```

---

## 📋 Prerequisites

Before running Terraform commands, ensure you have the following installed and configured:

1. 💻 **[Terraform CLI](https://developer.hashicorp.com/terraform/downloads)** (`>= 1.0.0`)
2. ☁️ **[Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)** (`az cli`)
3. 🔑 **Active Azure Subscription** with appropriate permissions (e.g., Contributor / Owner)

---

## ⚡ Quick Start Guide

### 1️⃣ Authenticate to Azure 🔐
```bash
az login
```
*(Optional) If you have multiple subscriptions, select your active subscription:*
```bash
az account set --subscription "<SUBSCRIPTION_ID_OR_NAME>"
```

---

## 🛠️ Terraform Workflow

### 2️⃣ Initialize Terraform 📦
Initialize the working directory and download necessary Azure provider plugins:
```bash
terraform init
```

### 3️⃣ Format & Validate Code 🧹
Ensure code adheres to standards and has no syntax issues:
```bash
terraform fmt
terraform validate
```

### 4️⃣ Preview Changes (Plan) 🔍
Generate and review the execution plan before creating resources:
```bash
terraform plan
```

### 5️⃣ Apply Configuration (Deploy) 🚀
Provision resources to your Azure environment:
```bash
terraform apply
```

### 6️⃣ Cleanup Resources (Destroy) 🧹
To remove all provisioned infrastructure:
```bash
terraform destroy
```

---

## 🔐 Best Practices

- 🛡️ **Remote State:** Configure Azure Blob Storage for remote backend state locking (`azurerm` backend).
- 🏷️ **Tagging Strategy:** Tag all resources with `Environment`, `Owner`, and `Project` for cost tracking.
- 🔒 **Secrets Management:** Avoid hardcoding secrets; utilize Azure Key Vault or environment variables (`TF_VAR_*`).
- 🌿 **Branch Strategy:** Follow Git Flow and run plans via CI/CD pipelines (GitHub Actions / Azure DevOps).

---

## 🤝 Contributing

Contributions, feedback, and suggestions are welcome! 🎉
1. 🍴 Fork the repository
2. 🌿 Create your feature branch (`git checkout -b feature/awesome-feature`)
3. 💾 Commit your changes (`git commit -m '✨ Add awesome feature'`)
4. 🚀 Push to the branch (`git push origin feature/awesome-feature`)
5. 📬 Open a Pull Request

---

<div align="center">
  <sub>Built with ❤️ and ☕ for DevOps Batch 18</sub>
</div>