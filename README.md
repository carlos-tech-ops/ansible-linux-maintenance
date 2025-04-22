# ansible-linux-maintenance

Modular Ansible automation for Linux systems. SSH-based execution, role-driven structure, and sudo privilege escalation. Built for precision, auditability, and DevSecOps readiness.
---

## Phase 2 – First Ansible Playbook Execution ✅  
**Status:** Complete

### Objective  
Automate Fedora maintenance tasks via SSH from macOS using a single Ansible playbook.

### Tasks Achieved  
- SSH key-based authentication (macOS → Fedora)
- Created GitHub-based structure: `inventories/`, `playbooks/`, `ansible.cfg`
- Wrote and executed first Ansible playbook with `--ask-become-pass`:
  - Updated system packages with `dnf`
  - Gathered system facts
  - Logged system info to `/var/log/system_info.log`

### Tools Used  
- macOS (controller node)  
- Fedora 41 (managed node)  
- Ansible 2.18.4  
- GitHub Web UI

---

## Phase 3A – Role-Based Automation: `user_provision` ✅  
**Status:** Complete

### Objective  
Create a Linux user (`devops_user`) using a dedicated Ansible role.

### Highlights  
- Fixed silent failure caused by wrong folder name (`task` → `tasks`)
- Set `roles_path` in `ansible.cfg` for correct role resolution
- Used `--ask-become-pass` for sudo access
- Verified user creation with `id devops`

### Skills Demonstrated  
- Role structure: `roles/user_provision/{tasks, handlers, vars}`  
- Remote provisioning via SSH  
- Privilege escalation with Ansible  
- Linux user creation

---

## Phase 3B – Multi-Role Execution via Tags ✅  
**Status:** Complete

### Objective  
Execute multiple Ansible roles from one playbook with tag-based precision.

### Roles  
- `user_provision`: Creates Linux user  
- `file_ops`: Creates `/opt/ops.txt` and sets permissions

### Achievements  
- SSH key-based login for `devops` user  
- Passwordless sudo enabled via `/etc/sudoers`  
- Used `--tags` to execute roles independently  
- Centralized playbook: `playbooks/main.yml`

### Execution Commands  
```bash
ansible-playbook playbooks/main.yml --tags user --ask-become-pass
ansible-playbook playbooks/main.yml --tags file --ask-become-pass
```
---

## About the Author

**Carlos Semeao** is a Cloud Security and DevOps learner with a zero-fluff approach to automation.  
From cleaning trains to orchestrating Linux systems with Ansible, his work reflects tactical discipline, remote-first design, and real-world readiness.

- **GitHub:** [carlos-tech-ops](https://github.com/carlos-tech-ops)  
- **LinkedIn:** [Carlos Semeão](https://www.linkedin.com/in/carlos-semeao-04938a357/)  
- **Toolset:** macOS, Fedora, Ansible, GitHub, SSH, YAML  
- **Mission:** Cloud automation mastery. No shortcuts. No noise. Just execution.

---
