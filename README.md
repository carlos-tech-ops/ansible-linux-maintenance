# ansible-linux-maintenance

Automated Linux maintenance with Ansible.  
Includes tasks for system updates, information gathering, and report logging.

---

## Phase 2: First Ansible Playbook Execution (Completed)

**Project:** `ansible-linux-maintenance`  
**Objective:** Automate Fedora system maintenance from macOS via Ansible.

### ✅ Tasks Achieved:
- Connected from macOS to Fedora using SSH key-based authentication.
- Created inventory, configuration, and playbook structure using GitHub web interface.
- Wrote and executed first Ansible playbook with `--ask-become-pass`:
  - Updated all Fedora packages.
  - Gathered system facts.
  - Logged system info to `/var/log/system_info.log`.

### ⚙️ Tools Used:
- macOS (Controller Node)
- Fedora 41 (Managed Node)
- Ansible 2.18.4
- GitHub

---

**Next Steps (Planned)**: Integrate this automation into a centralized controller using AWX (Ansible Tower) or Git-triggered cron jobs — milestones for later phases in my automation roadmap.


## Phase 3: Ansible Role Execution — User Provisioning (Complete)

This phase focused on building and executing an Ansible playbook with modular `roles/` structure to automate the creation of a Linux user (`devops_user`) remotely on a Fedora machine via SSH.

### Highlights:
- Fixed a critical silent misfire caused by incorrect folder naming (`task` → `tasks`)
- Used `ansible.cfg` to correctly resolve `roles_path`
- Successfully executed the role using `--ask-become-pass` for privilege escalation
- Verified user creation with `/etc/passwd` on the target Fedora node
- Maintained strict playbook modularity using `playbooks/main.yml` + `roles/user_provision/`

### Skills Demonstrated:
- Role-based playbook structuring
- Remote user provisioning
- SSH key-based automation
- Privilege escalation via Ansible
- Debugging Ansible project architecture

**Status:** Complete  
**Next Phase:** Multi-role automation for system updates, logging, cron jobs, and service management.
