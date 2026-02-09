## Ansible

### What is Ansible?
- Agentless Automation Tool
- Configuring servers, deploying apps, running repeatable tasks

### How does it work?
- Control Node is your laptop or CI Runner
- Managed Nodes are Servers you control (VMs, bare metal, cloud instances)
- Connection methods is SSH for Linux and WinRM for Windows OS
- Once again, Agentless. No software/tool needed on target machines

### Inventory
- Static is maintained in YAML and ini
- Also supports Dynamic Inventory (cloud providers etc.)