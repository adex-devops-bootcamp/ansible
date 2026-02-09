# Ansible

## Lab 1

### What is Ansible?
- Agentless Automation Tool
- Configuring servers, deploying apps, running repeatable tasks
- Can be installed with `pip` (python package manager) or `apt` as well.
- https://docs.ansible.com/

### How does it work?
- Control Node is your laptop or CI Runner
- Managed Nodes are Servers you control (VMs, bare metal, cloud instances)
- Connection methods is SSH for Linux and WinRM for Windows OS
- Once again, Agentless. No software/tool needed on target machines

### Inventory
- Static is maintained in YAML and ini
- Also supports Dynamic Inventory (cloud providers etc.)

### Playbook
- YAML only
- Hosts to be executed in
- Tasks to be executed
- Order of Execution (Imperative)
