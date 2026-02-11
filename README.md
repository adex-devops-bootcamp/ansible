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

## Lab 2

### Module
- Small program that runs on Target Nodes
- Does one specific job
- Example: install a package, copy a file, create user, etc.
- Module Example: apk, copy, file, user, etc.
- Why to use instead of `command: apk add nginx`

### Facts
- Data collected from the remote system (worker) by Ansible
- Examples: `ansible_hostname`, `ansible_default_ipv4.address`, `ansible_os_family`
- Source: The worker OS
- Need info about the system itself (IP, hostname, memory, OS type, etc.)
- Gathered with: `gather_facts: true`
- Variables will always replace Facts (Facts are the lowest priority variables)

### Variables
- Task level variables always take precedence.
- Variables passed in CLI takes next priority. `-e`
- Then comes `vars` in playbooks' top hierarchy (not to confuse with tasks)
- `var_files` used in playbook comes next.
- Lastly comes the facts gathered.

<!--
1. Introduction & Architecture
2. Installation & Setup
3. Inventory (static & dynamic)
4. Modules (file, command, package, service, etc.)
5. Variables (inline, files, host_vars, group_vars, CLI)
6. Facts (gather_facts & custom facts)
7. Templates (Jinja2)
8. Tasks & Plays
9. Handlers
10. Conditionals (`when`)
11. Loops (`with_items`, `loop`)
12. Roles & Role Directory Structure
13. Includes & Imports (`include_tasks`, `import_tasks`)
14. Tags
15. Handlers & Notifications
16. Ansible Vault (encrypting secrets)
17. Registering Variables & Using Output
18. Precedence & Scope of Variables
19. Dynamic Inventory
20. Delegation (`delegate_to`) & Local Actions
21. `set_fact` & Runtime Variables
22. Error Handling (`ignore_errors`, `failed_when`)
23. Blocks & Rescue / Always
24. Callbacks & Logging
25. Ansible Galaxy (using & creating roles)
26. Advanced Modules (docker, cloud, kubernetes, etc.)
27. Performance & Strategies (serial, forks, async)
28. CI/CD Integration (GitHub Actions, Jenkins, GitLab)
29. Ansible Collections
30. Best Practices & Project Layout
-->