# install-terraform-proxmox-provider

```
Install:
ansible-galaxy install nikobraz.install_terraform_proxmox_provider
cat > install.yml <<EOL
---
- hosts: all
  roles:
  - role: nikobraz.install_terraform_proxmox_provider
EOL
```

# Write terraform
```
cat > main.tf <<EOL
terraform {
  required_providers {
    proxmox = {
      source  = "local/provider/proxmox"
      version = ">=1.0.0"
    }
  }
  required_version = ">= 0.13"
}
EOL


```
